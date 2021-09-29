.. lued documentation master file, created by
   sphinx-quickstart on Tue Sep 28 18:29:33 2021.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

################################
Welcome to lued's documentation!
################################


*************
What is it?
*************

**Lued** is a *Lua* based *Editor* that runs in the console like 
`emacs <https://www.gnu.org/software/emacs/>`_ or `vim <https://www.vim.org/>`_. 

Lued's goal is to be comfortable for Windows users. Common Windows keystrokes
are supported. For example, ``Ctrl+C``, ``Ctrl+X``, ``Ctrl+V`` do copy, cut and
paste, respectively. ``Ctrl+Z`` and ``Ctrl+Y`` undo and redo. Ctrl+S, Ctrl+Q
save and quit. You move arrow using the arrow keys. ``PgUp``, ``PgDn``,
``Home`` and ``End`` work as expected. For more advanced commands, Lued attempts
to be similar to `Sublime <https://www.sublimetext.com/>`_ or 
`VScode <https://code.visualstudio.com/>`_. You can use the mouse to copy and
paste and the scroll wheel lets you easily navigate up and down the document.

Lued is compatible with most xterms such as
`Konsole <https://konsole.kde.org/>`_ and 
`Gnome Terminal <https://wiki.gnome.org/Apps/Terminal>`_. It also works well
with `PuTTy <https://www.chiark.greenend.org.uk/~sgtatham/putty/>`_ and
`tmux <https://github.com/tmux/tmux/wiki>`_.


*************
Get it
*************

Lued source code is available under the
`MIT License <https://opensource.org/licenses/MIT>`_ at
`github.com/jwrr/lued <https://github.com/jwrr/lued>`. You can download a zip
file or clone the repo.

:download:`Download Lued Zip File <https://github.com/jwrr/lued/archive/master.zip>`

.. code-block:: bash

  git clone https://github.com/jwrr/lued


*************
Build it
*************

To build Lued just run the ``COMPILE`` script. The script handles downloading
Lua 5.2, applying a few minor patches to the Lua release, running cmake and
compiling lued.

.. code-block:: bash

  cd lued
  COMPILE


You will need `cmake <https://cmake.org/>`. On Ubuntu you can install with apt-get.

.. code-block:: bash

  sudo apt-get -y install cmake


**************
Try it
**************

.. code-block:: bash

  ./lued filename.txt
  

**************
Use it
**************

You've gotten this far and you haven't turned away. You want to know more.
Lued offers many ways to move, select, find and delete. I recommend you
first take a quick look at the key bindings. And then dive into the User
Guide.


**************
Tweak it
**************

You can easily change the key bindings. The key bindings are defined in file 
``lua_src/bindings/lued_bindings.lua``. The bindings have the format ``alt_xxx``
and ``ctrl_yyy`` (these are actually lua function calls but don't worry about
that). To change a binding, just find it and replace it with what you want. For
example, say you want to change the delete to end-of-line command from ``alt+xe``
to ``ctrl+K``, as it is in Emacs. You would open the lued_bindings.lua file
(using lued or your editor of choice), find ``alt_xe`` using  ``ctrl+F`` and then
change it to ``ctrl_K``. Now restart lued and you're good to go. BTW, ``Ctrl+K``
is not currently used, and is waiting for you to make this change.


**************
Extend it
**************

All commands are implemented in Lua (there’s some C under the hood but you'll
never see it… unless you want to). Lua is an easy to learn scripting language
that is powerful and blazingly fast. You can modify the Lua code directly or
you can develop a plugin (also written in Lua). The plugins support 
`emmet <https://docs.emmet.io/>`_ snippets where you type a user-defined tag
followed by Tab and a pre-defined template is printed out.


**************
Fix it
**************

Submit your pull requests. Thanks



.. toctree::
   :maxdepth: 2
   :caption: Contents:



Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
