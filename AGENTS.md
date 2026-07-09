# Repository Guidelines

## Project Structure

- Dependency and tool configuration lives at `pyproject.toml`, `.pre-commit-config.yaml`, and `uv.lock`.
- LaTeX paper is in `paper/latex/`, including the `main.tex` manuscript, the `references.bib` BibTex, and any figure files.
- All LaTeX output/temp files go into `paper/latex/.output/`.
- Data are in `data/` and should not be committed.
- Code is in `code/`, including Jupyter notebooks Python scripts in `code/analysis/` and tests in `code/tests/`.
- Code should save any visualizations to be included in the paper as vector PDFs in `paper/latex/`.

## Commands

- Use `uv` for local Python and virtual environment.
- Use `uv add` to add every (non-standard library) package imported anywhere in the code to `pyproject.toml` dependencies.
- Run pre-commit hooks after any changes with `uv run prek run -a`.
- Run test suite with `uv run python -m pytest`.

## Version Control Guidelines

- Do not create or edit files unless the user explicitly tells you to do so.
- Work in git branches instead of `main`.
- Stage new files you create to ensure pre-commit hooks see them.
- Do not commit: allow the user to commit manually when they're ready.

## Code Guidelines

- Follow all code formatting and linting rules defined in the project config.
- Write human-maintainable and interpretable code.
- Do not over-engineer code: prefer simplicity and legibility.
- Use thorough code comments to explain "what" code does and "why" it does it that way.
- Use type annotations and complete numpy-style docstrings in all public and private functions.
- All code requires thorough unit tests.

## Paper Guidelines

- Use pdflatex to compile and natbib/bibtex for references.
- Keep any figures or other included files as siblings of the .tex file.
- Prefer `\autoref` to `\ref`.
- Use `\enquote` for quote marks and `\textit` for italics; avoid boldface.
- Use `\citet` and `\citep` for textual and parenthetical citations, respectively; avoid `\cite`.
- Use en dash (`--`) for ranges of values.
- Use em dash (`---`) to offset adjunctive phrases stronger than those in parentheses.
- Ensure table columns' values right-align on the decimal.
- Avoid system fonts, instead use texlive-provided font packages.
- Avoid importing other packages.
- Compile often, check log for warnings/errors, and resolve them.
- Run the pre-commit hooks to lint via `chktex`, and resolve any issues.

## Consistency

- Verify consistency of terminology, descriptions, and results across the paper and code.
- Verify paper's methods section text matches the analysis code: methods, units, calculations, equations, terminology, and data should match.
- Verify analysis code output matches the paper's reported numbers, tables, figures, equations, and units.
- Verify paper text's claims against the figures/tables' numbers, signs, rankings, labels, legends, captions.
