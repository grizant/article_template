# Schissler Group article production workflow

The git repo serves as a starting point for every article writing project we that we undertake.

# Description of tools and software

## Bookdown

This template began with a minimal article template cloned directly from https://github.com/rstudio/bookdown-demo that uses on R Markdown and **bookdown** (https://github.com/rstudio/bookdown). Please see the page "[Get Started](https://bookdown.org/yihui/bookdown/get-started.html)" at https://bookdown.org/yihui/bookdown/ for how to compile this example into HTML. You may generate a copy of the book in `bookdown::pdf_book` format by calling `bookdown::render_book('index.Rmd', 'bookdown::pdf_book')`. More detailed instructions are available here https://bookdown.org/yihui/bookdown/build-the-book.html. You can find the preview of the default book template at https://bookdown.org/yihui/bookdown-demo/.

I've modified the minimal demo to fit our style and taylor towards statistical work.

## Git/github

- You need to get familiar with `git`. Try the resources here: (https://try.github.io/).
- Remember to *ALWAYS PULL FIRST THEN TRY TO PUSH YOUR WORK*.
- Try to avoid conflicts by coordinating with your team members. Don't work on the same things at the same time.

## Menedely: reference management

- We'll use [Mendeley](https://www.mendeley.com) for reference management. 
- Each project will have an associated `Group` and the project leader (1st author usually) will create and invite members while giving owner rights to the PI.
- Mendeley can be configured to produce a `bib` file for each group. We'll have `bash` `knitr` code to sync the latest bib file in the user selects a default configuration (`~/bib/group_name.bib`).

## Conda

- We use [`conda`](https://conda.io/projects/conda/en/latest/user-guide/index.html) to manage virtual environments to have reproducible results.
- Ideally, we have a dedicated `conda` env for each article.
- But if the project uses fairly standard tools (non-*Big Data* projects) then we can avoid this sometimes cumbersome step.

# Files and directory structure

Again, we begin with a minimal yet nicely formatted `bookdown` article template. I then tweak this settings slightly and include some extra directories and files.

## Files

I slightly modify the section labels to meet our template analysis and allow for easier subsection extensions. For example I changed `02-literature.Rmd` to `020-background.Rmd`.

I also modified the `index.Rmd` and `.yml` files to tailor our template.

## notebooks directory

The `./notebooks/` directory contains `.Rmd` files for content that is not directly included in the chapters. Some examples:

- Notebooks that describe experiments that may have not made it to the main document yet.
- Notebooks that generate data that is used in the main chapter (e.g., `rslurm4myData.Rmd` from calculations on the server).
- Notebooks that generate presentations such as `ioslides` for talks.
- Notebooks that generate scientific posters.
- Notebooks with tutorials and workflows.

Basically any related work that may have utility later or supports the article generation.

## data/ directory

The `./data/` directory contains data in the case that the data used is very large or time-consuming to compute. Usually we summarize and compress large datasets as `.rds` files for reference in the article sections. 

Please *be frugal with this as to not bloat* the repo.

# Publishing process and project management through git

1. Do as much content creation and editing as possible in the base HTML `bookdown` article_template.
2. Create a new `git` branch to prepare an article for submission to a particular publisher.
3. Reformat using possibly [`rticles`](https://github.com/rstudio/rticles) or [`bookdownplus`](https://github.com/pzhaonet/bookdownplus) to meet the submission guidelines.
4. Submit the manuscript and wait.
5. Once the article recevies peer review (or rejection), we'll branch again and create a revision `git` branch for that journal.
6. Cycle this way through `revX` until acceptance, or rejection. If reject, start again at the `master` branch.
7. Once accepted, prepare a single-page `pdf` article suitable for (https://arxiv.org/archive/stat) to archive and release our work from the `master` branch. Then create a new `git` branch `prePeerReview`. 
8. Then merge the `revX` branch into `master` and wait for proofs.
9. Handle proofs in the `master` branch.
10. Update your CVs!

# Writing tips

1. Draft quickly, edit slowly.
2. Always consider your audience when deciding on selection of details, depth, scope, language choice, etc.
3. Set and meet daily writing goals.
4. Read while you write --- don't wait to create.
5. Get feedback on your writing and revise eagerly.
