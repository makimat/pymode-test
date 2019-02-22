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
