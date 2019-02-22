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

## vim --version

    VIM - Vi IMproved 8.1 (2018 May 18, compiled Feb 12 2019 09:48:12)
    Included patches: 1-897
    Compiled by makimat@makimat-dev
    Huge version with GTK2 GUI.  Features included (+) or not (-):
    +acl               +extra_search      +mouse_netterm     +tag_old_static
    +arabic            +farsi             +mouse_sgr         -tag_any_white
    +autocmd           +file_in_path      -mouse_sysmouse    -tcl
    +autochdir         +find_in_path      +mouse_urxvt       +termguicolors
    -autoservername    +float             +mouse_xterm       +terminal
    +balloon_eval      +folding           +multi_byte        +terminfo
    +balloon_eval_term -footer            +multi_lang        +termresponse
    +browse            +fork()            -mzscheme          +textobjects
    ++builtin_terms    +gettext           +netbeans_intg     +textprop
    +byte_offset       -hangul_input      +num64             +timers
    +channel           +iconv             +packages          +title
    +cindent           +insert_expand     +path_extra        +toolbar
    +clientserver      +job               +perl              +user_commands
    +clipboard         +jumplist          +persistent_undo   +vartabs
    +cmdline_compl     +keymap            +postscript        +vertsplit
    +cmdline_hist      +lambda            +printer           +virtualedit
    +cmdline_info      +langmap           +profile           +visual
    +comments          +libcall           +python/dyn        +visualextra
    +conceal           +linebreak         +python3/dyn       +viminfo
    +cryptv            +lispindent        +quickfix          +vreplace
    +cscope            +listcmds          +reltime           +wildignore
    +cursorbind        +localmap          +rightleft         +wildmenu
    +cursorshape       +lua               +ruby              +windows
    +dialog_con_gui    +menu              +scrollbind        +writebackup
    +diff              +mksession         +signs             +X11
    +digraphs          +modify_fname      +smartindent       -xfontset
    +dnd               +mouse             +startuptime       +xim
    -ebcdic            +mouseshape        +statusline        +xpm
    +emacs_tags        +mouse_dec         -sun_workshop      +xsmp_interact
    +eval              -mouse_gpm         +syntax            +xterm_clipboard
    +ex_extra          -mouse_jsbterm     +tag_binary        -xterm_save
       system vimrc file: "$VIM/vimrc"
         user vimrc file: "$HOME/.vimrc"
     2nd user vimrc file: "~/.vim/vimrc"
          user exrc file: "$HOME/.exrc"
      system gvimrc file: "$VIM/gvimrc"
        user gvimrc file: "$HOME/.gvimrc"
    2nd user gvimrc file: "~/.vim/gvimrc"
           defaults file: "$VIMRUNTIME/defaults.vim"
        system menu file: "$VIMRUNTIME/menu.vim"
      fall-back for $VIM: "/usr/local/share/vim"
    Compilation: gcc -c -I. -Iproto -DHAVE_CONFIG_H -DFEAT_GUI_GTK  -pthread -I/usr/include/gtk-2.0 -I/usr/lib/x86_64-linux-gnu/gtk-2.0/include -I/usr/include/gio-unix-2.0/ -I/usr/include/cairo -I/usr/include/pango-1.0 -I/usr/include/atk-1.0 -I/usr/include/cairo -I/usr/include/pixman-1 -I/usr/include/libpng12 -I/usr/include/gdk-pixbuf-2.0 -I/usr/include/libpng12 -I/usr/include/pango-1.0 -I/usr/include/harfbuzz -I/usr/include/pango-1.0 -I/usr/include/glib-2.0 -I/usr/lib/x86_64-linux-gnu/glib-2.0/include -I/usr/include/freetype2   -g -O2 -U_FORTIFY_SOURCE -D_FORTIFY_SOURCE=1       
    Linking: gcc   -L. -Wl,-Bsymbolic-functions -Wl,-z,relro -Wl,-z,now -fstack-protector -rdynamic -Wl,-export-dynamic -Wl,-E   -L/usr/local/lib -Wl,--as-needed -o vim   -lgtk-x11-2.0 -lgdk-x11-2.0 -lpangocairo-1.0 -latk-1.0 -lcairo -lgdk_pixbuf-2.0 -lgio-2.0 -lpangoft2-1.0 -lpango-1.0 -lgobject-2.0 -lglib-2.0 -lfontconfig -lfreetype -lSM -lICE -lXpm -lXt -lX11 -lXdmcp -lSM -lICE  -lm -ltinfo -lnsl  -lselinux   -ldl  -L/usr/lib -llua5.1 -Wl,-E  -fstack-protector-strong -L/usr/local/lib  -L/usr/lib/x86_64-linux-gnu/perl/5.22/CORE -lperl -ldl -lm -lpthread -lcrypt    -lruby-2.3 -lpthread -lgmp -ldl -lcrypt -lm     
