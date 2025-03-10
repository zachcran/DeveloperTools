Developing NWX with VSCode
==========================

Once you've got the build working you're ready to start developing. The
following subsections provide some basic advice on how to go about doing
common development tasks.

Version Control
---------------

It's strongly recommended that you do your development on a new branch and not
on "master" (the bottom toolbar should show your current branch next to the
version control icon, three circles in a V-like pattern). Clicking on the branch
name will bring up a menu where you can select "Create new branch" to create
your new branch (clicking "Create new branch" will lead to a new menu where you
name the branch).

More version control options are available in the left toolbar by clicking on
the version control symbol. Here you will see a list of uncommitted changes for
each repo in your workspace. You can click on a change to see the difference.
Next to the file you also will see buttons for opening the file, reverting the
file, and staging the file. Next to the branch name is a checkmark which can be
used to quickly stage and commit all changed files (you'll have to type a
commit message in the provided box). Finally For the ellipses (three dots) will
bring up a menu with common git commands like push and pull.

Debugging
---------

Debugging is one of the main reasons to use an IDE. To debug an executable,
click on the play-arrow with a bug on it in the left toolbar. If you have no
debug configurations set up yet there will be a big "Run and Debug" button
Click on it. This will bring up a menu asking you about the type of C++ debugger
you want to use. Pick the appropriate one (probably GDB/LLVM). Next, it'll ask
you which configuration you want to use. This will generate a JSON with your
debug configuration and open it in an editor. For most purposes the only thing
we need to change is the value associated with the "program" key; change this to
the path for the executable you want to debug (note you can use
``${workspaceFolder}`` to get an absolute path to the top-level directory of
your current folder).

Clicking the green play arrow in the top toolbar will start a debugging session
for the current selected configuration (use the drop down menu next to the
arrow to select the configuration). The run will automatically stop on any
signal (such as segfault). It also will automatically stop when it hits a
breakpoint (you can set a breakpoint by clicking to the left of the line number
you want to break on). When the program stops the debugging pane will show the
values of the current variables and the current stack. You can use the toolbar
at the top-center to respectively: resume/pause execution, go to the next line
in the current source file, enter the function on the current line, go up one
call in the stack, restart execution, or stop execution.

Profiling
---------

TODO: Write Me!!!!
