# Schissler Group article production workflow

The git repo serves as a starting point for every article writing project we that we undertake.

# Description of tools and software

## Git

- Remember to *ALWAYS PULL FIRST THEN TRY TO PUSH YOUR WORK*.
- 

## Reference management

- We'll use [Mendeley](https://www.mendeley.com) for reference management. 
- Each project will have an associated `Group` and the project leader (1st author usually) will create and invite members while giving owner rights to the PI.
- Mendeley can be configured to produce a `bib` file for each group. We'll have `bash` `knitr` code to sync the latest bib file in the user selects a default configuration (`~/bib/group_name.bib`).

## Bookdown

This template began with a minimal article template cloned directly from https://github.com/rstudio/bookdown-demo that uses on R Markdown and **bookdown** (https://github.com/rstudio/bookdown). Please see the page "[Get Started](https://bookdown.org/yihui/bookdown/get-started.html)" at https://bookdown.org/yihui/bookdown/ for how to compile this example into HTML. You may generate a copy of the book in `bookdown::pdf_book` format by calling `bookdown::render_book('index.Rmd', 'bookdown::pdf_book')`. More detailed instructions are available here https://bookdown.org/yihui/bookdown/build-the-book.html. You can find the preview of the default book template at https://bookdown.org/yihui/bookdown-demo/.

# File structure

## Notebooks

# Publishing process and project management through git

1. Do as much content creation and editing as possible in the base HTML `bookdown` article_template.
2. Create a new `git` branch to prepare an article for submission to a particular publisher.
3. Reformat using possibly [`rticles`](https://github.com/rstudio/rticles) or [`bookdownplus`](https://github.com/pzhaonet/bookdownplus) to meet the submission guidelines.
4. Submit the manuscript and wait.
5. Once the article recevies peer review, we'll branch again and create a revision `git` branch for that journal.
6. Cycle this way through `revX` until acceptance.
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
