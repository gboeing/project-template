# Repository Guidelines

## Rules

- Do not make file edits or changes unless the user explicitly tells you to do so.

## Project Organization

- Dependency and tool configuration lives at the root in `pyproject.toml`, `.pre-commit-config.yaml`, and `uv.lock`.
- Code and analysis is in `code/`, including Jupyter notebooks and Python scripts.
- Code should save any visualizations to be included in the paper as vector PDFs in `paper/latex/`.
- LaTeX paper is in `paper/latex/`, including the `main.tex` manuscript, the `references.bib` BibTex, and figure files to include.
- All LaTeX output/temp files go into `paper/latex/.output/`.
- Data are in `data/` and should not be committed.

## Commands

- Use `uv` for local Python and virtual environment.
- Use `uv add` to add every (non-standard library) package imported anywhere in the code to `pyproject.toml` dependencies.
- Run pre-commit hooks after any changes with `uv run prek run -a`.
- Run test suite with `uv run python -m pytest`.

## Coding Guidelines

- Follow code formatting and linting rules defined in `pyproject.toml` and `.pre-commit-config.yaml`.
- Write human-maintainable and interpretable code.
- All code requires thorough unit tests.
- Do not over-engineer code: prefer simplicity and legibility.
- Use thorough code comments to explain "what" code does and "why" it does it that way.
- Use type annotations and complete numpy-style docstrings in all public and private functions.
- Verify that the paper's equations, terminology, methods descriptions, tables, figures, and in-text numerical results match the code's calculations/results and are internally consistent.

## Version Control Guidelines

- Work in git branches instead of `main`.
- Stage new files you create to ensure pre-commit hooks see them.
- Do not commit: allow the user to commit manually when they're ready.

## LaTeX Paper Guidelines

 - Use pdflatex instead of xelatex/lualatex for compatibility with arxiv/publishers.
 - Use natbib/bibtex instead of biblatex/biber for compatibility with arxiv/publishers.
 - Avoid subfolders: keep any figures or other included files as siblings of the .tex file.
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
