# Coding workshop 1: toward sharing Python code

## about

This workshop aims to offer means to re-use Python code written by
colleagues and to prepare and share code with colleagues. The advocated
practices, also, help to make scientific results reproducible. The
workshop is contained in the files starting with a number and ending in
`.ipynb` (jupyter notebooks). The number is used to order the workshop
material. It is work-in-progress - please file issues or talk to your
colleagues if things should be changed or advanced.

## prerequisites

We use GitHub to share the code, because it is basically accessible
everywhere. Some of the Boku-Met repositories are not public. To access
those, you need to become a member of Boku-Met. Ask any of your
colleagues for an invitation. Further, you will need to get git to
authenticate at GitHub. There are many options available, see the [docs
on git's credential
helpers](https://git-scm.com/doc/credential-helpers). The simplest way
is using the GitHub command line tool [`gh`](https://cli.github.com/).
After installation, do `gh auth login` whenever you want to install some
repository with anything similar to `pip install
git+https://github.com/boku-met/...`. This will save an authentication
token into your local environment[^1]. You will be asked to provide this
token. It can be obtained in the "developer settings" of your GitHub
account. Please find detailed instructions online, for example, in the
[GitHub
docs](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens).
To verify that you are good to go, try running the below:

```shell
conda create -n tmp pip
pip install "git+https://github.com/boku-met/data-utils"
conda env remove -n tmp
```

Finally, prepare the means to view and execute Jupyter Notebooks. All
modern integrated development environments (IDEs) can do that. However,
you can also use a conda environment with Jupyter installed and a
browser. In that case, run `jupyter lab` or `jupyter notebook
<notebook>.ipynb` and follow the instructions to access it in your
browser.

[^1]: The token is saved as plain text. This is a security risk. That is
why it makes sense to limit its life time and restrict it to the
resource you need to have access to. You will be asked to make these
choices when creating it. However, try to balance the risk of someone
obtaining the token (and having access to our shared GitHub account) and
the hassle of overly tight restrictions.
