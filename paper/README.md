# LaTeX Template

A standard LaTeX template for starting research papers.

LaTeX is the secret to better scientific writing. It comes with a learning curve, but you'll soon be writing much faster, more flexible, and more beautifully typeset documents.


## LaTeX guidelines

This template loads a standard set of packages to get you up and running.

A few rules:

 - use pdflatex instead of xelatex/lualatex for compatibility with arxiv/publishers
 - use natbib/bibtex instead of biblatex/biber for compatibility with arxiv/publishers
 - avoid subfolders: keep any figures or other files as siblings of the .tex file
 - use `\enquote{}` for quote marks and `\textit{}` for italics; avoid boldface
 - use `\citet{}` and `\citep{}` for textual and parenthetical citations, respectively
 - use en dash (`--`) for ranges of values
 - use em dash (`---`) to offset adjunctive phrases stronger than those in parentheses
 - ensure table columns' values right-align on the decimal
 - avoid system fonts, instead use texlive-provided font packages
 - avoid importing other packages unless truly necessary (it rarely is)
 - compile often, check log for warnings/errors, and resolve them promptly
 - run the pre-commit hooks to lint via chktex, and resolve any warnings


## Paper Outline

The trick to an effective paper is a good structure.

Before you draft a paper, make sure you can articulate your interrelated research question, argument, and significance. The **question** is simply what your project sets out to answer. The **argument** is your paper's single "big idea" in 1-2 sentences, motivated by an existing knowledge gap, and around which you organize your paper and your evidence to persuade the reader. One paper, one idea. The **significance** is the "so what?" Why should we read your paper? What will we do differently in research or practice now that we've read it?

- **Introduction**: your audience doesn't care about your work and you have three paragraphs to change their mind
  - introduce your topic and its overall context and importance (persuade us to care)
  - introduce your research problem, question, and argument
  - summarize your methods, findings, and significance
- **Background**: build an argument to establish/justify your research problem, question, methods, and importance
  - explain the real-world context behind your study
  - review relevant previous work to establish what is currently known and the state-of-the-art
  - identify what important problem remains (gap in the literature or unmet need in practice)
- **Methods**: what did you do and how did you do it
  - state your research question and hypotheses
  - data subsection: describe your data collection, variables, and any relevant processing
  - analysis subsection: describe your analyses with enough detail that an expert could replicate them
- **Findings**: what did your analysis reveal
  - organize your results around your argument but present them objectively with limited interpretation
  - include supporting tables/figures
  - do not mix in any methods: all the "how-to" goes in the previous section
- **Discussion**: answer your question, advance your argument, and demonstrate significance
  - return to research problem/question and interpret (don't repeat) your findings as evidence for/against your hypothesis: tell a story to link your findings together to persuasively advance your argument
  - how do your results align with or contradict existing theory reviewed in the background section, and why?
  - significance: discuss specific implications for research and practice (the "so what"). If a practitioner read your paper, what would they do differently at work tomorrow in light of this new knowledge?
  - acknowledge study's limitations and alternative interpretations of your evidence: what opportunities are there for future research?
- **Conclusion**: succinctly wrap up
  - summarize your topic, question, and argument
  - summarize what you did, what you found, what it means, and why it matters


## Tips for using the outline

Sometimes the introduction and background are merged into a single section. Sometimes the discussion and conclusion are merged into a single section. But this is the basic structure of an effective paper, be it a technical report or a scholarly article.

The structure represents a loose symmetry. The introduction and conclusion roughly mirror each other by explaining the topic's importance, the research question, how you answered it and what you found, and its meaning/significance in the real world. The background and discussion roughly mirror each other by explaining what is known about the topic before (to motivate your specific study) and after your study (to advance our knowledge and impact the real world). The methods and findings sections roughly mirror each other by laying out what you did and then presenting what you found when you did so.

In general, people struggle most with writing an effective introduction and discussion. Perversely, these are also the most critical sections of your paper for persuading your readers (including peer reviewers). A strong **introduction** in four paragraphs:

1. Lay out the topic's context and background using anecdotes or facts to illustrate its importance. Show, don't tell. Orient the reader toward your paper's subject, motivate why this should interest us in the first place, and establish your perspective on approaching it.
2. What is the problem and its significance? What is the open research question that follows from it and what argument do you develop over the course of this paper? Why is it important from a real-world planning or policy perspective?
3. How did you answer your question and what did you find? Summarize your data and methods in 1-2 sentences. Then summarize your findings specifically and precisely in 1-2 sentences, citing specific takeaways like "a 1% increase in fuel prices decreases VMT by 0.2%". Conclude with 1 sentence on "who cares?" That is, how do these findings impact real-world policy? What should a practitioner do differently after reading this study? Why is the world better off for having discovered what you have discovered?
4. Optional roadmap: signpost the organization of the remaining sections so the reader knows what's coming and how you've laid things out.

An **abstract** (when required) is written last and summarizes everything into a succinct paragraph. Consider using a simple five-sentence structure:

1. what is the research context and problem
1. what is your research question
1. how did you answer that question
1. what did you find
1. significance: how are these findings important and useful


## Writing guidelines

Whether it's a professional report or a scholarly article, all strong technical writing shares common elements.

Don't overstate things: you'll lose your readers' trust. Present your results clearly and honestly and avoid over-interpreting them. There's rarely a clear answer and there's almost never a definitive answer. You've contributed some new evidence and marginal knowledge. Embrace that confidently.

Write like a lawyer, not like a detective. Don't list your results in the order that you discovered them. Instead, structure them strategically around your argument to persuade us of its validity.

Rewrite and revise heavily, over and over and over. Get feedback from peers.

F. Scott Fitzgerald said: "You don't write because you want to say something, you write because you have something to say." What is the point you are trying to make? What are you trying to say? Keep refining that central point in your mind until you are ready to write about it. Communicating the point is the goal of writing. As you write, ask yourself, for each sentence: how does it contribute to that goal? Get out of the student-homework mode of thinking that the more you say about something shows the more you know about it. Persuasively arguing a precise and concise point is the goal.

**We all hate reading scholarly papers for good reason**. They are over-written by academics who mistake obscure language for a signifier of intelligence. They overflow with weak verbs, passive voice, and long circuitous sentences. To communicate effectively with a broad audience, follow a few simple guidelines (adapted from Belcher) as you write, revise, and edit:

### Practice brevity

Write directly and succinctly. Don't use two words when one will do. Excise redundant information. Break up long winding sentences into short direct ones. Don't say "very." Avoid most adverbs ending in "-ly." Example: "avoid adverbs unless really necessary." Better: "avoid adverbs unless necessary."

### Show, don't tell

Be assertive and precise to make it clear what you mean. Prefer specific words to general ones. Prefer nouns to pronouns. Prefer verbs to nouns. Avoid nominalizations (verbs converted into nouns). Example: "a 1% increase in fuel prices caused a 0.2% _reduction_ in VMT." Better: "a 1% increase in fuel prices _reduced_ VMT by 0.2%." Write positively: avoid using "not" to obscure your meaning. That is, tell us what did happen rather than what didn't.

### Use active language

Write in the present tense and (plural first-person) active voice: tell us who is kicking whom. Avoid the passive voice unless the subject is truly unknown/unimportant. Example: "this pattern is illustrated by figure 2." Better: "figure 2 illustrates this pattern." Prefer strong verbs to weak ones. Limit your use of to be, to do, to have, to make, to provide, to get, to seem, etc.

### Use fewer prepositions

Too many prepositions signal a circuitous sentence and often indicate other issues listed above. Prefer simpler nouns/verbs to prepositions for more direct writing. Example "in the case of a number of 20th century cities, the extent of new freeways grew rapidly." Better: "Planners rapidly extended new freeways in many 20th century cities."
