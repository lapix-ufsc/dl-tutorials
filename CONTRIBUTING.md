# How to contribute to dl-tutorials?

First, thanks a lot for wanting to help! Everyone is welcome to
contribute. Answering questions, helping others, improving the
already existing tutorials (or creating new ones) are some of the ways
to contribute.

## How to get started (Pull requests)

Before writing code, search through the existing PRs or issues to ensure 
that nobody is already working on the same thing.

1.  Fork the [repository](https://github.com/lapix-ufsc/dl-tutorials)
    by clicking on the 'Fork' button on the repository's page.

2.  Clone your fork to your local disk, and add the base repository as
    a remote:

    ```bash
    $ git clone git@github.com:<your Github user>/dl-tutorials.git
    $ cd dl-tutorials
    $ git remote add upstream https://github.com/lapix-ufsc/dl-tutorials.git
    ```

3.  Sync your fork with the original repository.

    ```bash
    $ git fetch upstream
    $ git rebase upstream/main
    ```    

4.  Create a new branch for your changes:
    ```bash
    $ git checkout -b descriptive-of-my-changes
    ```

    **Do not** work on the `main` branch.

5.  Write the changes on your branch.

    As you work on improving or writing new tutorials, you should
    make sure that the notebook follow PEP8.
    
    Keeps in mind, that the pages are build directly from the jupyter
    notebooks. This is done with the help of [nbdev](https://github.com/fastai/nbdev/).
    So, you can try and test the build locally, where you first will
    need to install it:

    ```bash
    $ pip install -r requeriments-dev.txt
    $ pip install nbdev
    ```

    To preview the pages, run:

    ```bash
    $ nbdev_preview
    ```
    
    Note: you can use some `magic flag` from nbdev to improve the
    pages. By example use at some cell `%nbdev_collapse_output` to
    hidden the output at the page.

    To help on follow PEP8 and also on formatting the notebooks with
    `black` and `isort`, you can use [pre-commit](https://github.com/pre-commit/pre-commit).
    You can check all hooks we use at [.pre-commit-config.yaml](/.pre-commit-config.yaml),
    or just let the pre-commit do its magic by installing with:
    
    ```bash
    $ pip install pre-commit
    ```

    The pre-commit hooks will automatically run when you try create a
    commit. Also, can be run manually with:

    ```bash
    $ pre-commit run
    ```

    If you work at [index](./tutorials/index.ipynb) file, please
    also auto generate the readme file with the command:

    ```bash
    $ nbdev_readme
    ```

    Please write [good commit messages](https://chris.beams.io/posts/git-commit/).

    Push the changes to your account using:

    ```bash
    $ git push -u origin descriptive-of-my-changes
    ```

6.  When you finish your changes, go to the webpage of your fork on
    GitHub (`github.com/<your Github user>/dl-tutorials`).
    Click on 'Pull Request' to send your changes for review.



### Checklist

1.  The title of your pull request should be a summary of your
    contribution;

2.  If your pull request addresses a issue, please mention the issue
    in the description of the pull request to make sure that they are
    linked;

3.  To indicate a work in progress, please prefix the title with `[WIP]`.
    You can also create the PR as a draft.