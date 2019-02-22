# pymode-test
Test pymode with small sample project

## Steps to reproduce https://github.com/python-mode/python-mode/issues/973

In this repository, execute:

    vim -u .vimrc test.py
    :PymodeLint

or

    vim -i NONE -u ~/.vim/bundle/python-mode/debugvimrc.vim test.py
    :PymodeLint

It will result in the same tracebacks and linting fails.

## python-mode git repository status in Vundle

    $ git status
    On branch develop
    Your branch is up-to-date with 'origin/develop'.
    nothing to commit, working directory clean

    $ git show -1
    commit 166268a4882cd35b3d61ce9f926845d92a53ee06 (HEAD -> develop, origin/develop, origin/HEAD)
    Merge: 81a4f6e dff0075
    Author: Diego Rabatone Oliveira <diraol@diraol.eng.br>
    Date:   Thu Feb 21 10:01:43 2019 -0300

        Merge pull request #993 from diraol/fix_pkg_resources

        Get the package loader instead of its spec.

    $ git submodule status
    5b5cd7acbecaa9b587b07de27a3334a2ec4f2a79 submodules/astroid (astroid-2.0.4)
    159bb88843e298534e46914da242e680a1c8c47d submodules/autopep8 (v1.3.2-90-g159bb88)
    c2f5b386458cfda0aa4239f4d11b4e5e75027bda submodules/mccabe (0.6.1-19-gc2f5b38)
    566cdc0cb22e5530902e456d0b315403ebab980c submodules/pycodestyle (2.4.0-19-g566cdc0)
    eea4ca179553189a7b8a62d6085f15b50bb98e35 submodules/pydocstyle (0.4.1-431-geea4ca1)
    45fc732466056fe35c85936ff25491df7905c597 submodules/pyflakes (2.0.0-10-g45fc732)
    837ecd3d7a8597ab5f28bc83072de68e16470f1e submodules/pylama (0.1.0-552-g837ecd3)
    66cb32187c040f82dd067bc0d226b2f105bf6c38 submodules/pylint (pylint-2.1.0-59-g66cb321)
    95aa2749f978d579fda03478dece4d611c2323f9 submodules/rope (0.11.0-2-g95aa274)
    84d07dd19523a3a41385f23a744a126d00a72c79 submodules/six (1.11.0-14-g84d07dd)
    404cab3e069cd5c2c891c19404fbd85bd285c021 submodules/snowball_py (remotes/origin/HEAD)
