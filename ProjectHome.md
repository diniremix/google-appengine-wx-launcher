![http://www.google.com/accounts/ah/appengine.jpg](http://www.google.com/accounts/ah/appengine.jpg)

# Windows Launcher for Google App Engine #

This project contains the source code for the GUI Launcher, first included with the Google App Engine SDK 1.2.5 for Python on Windows.  The Launcher is an application for creating, running, uploading, and otherwise managing Google App Engine applications.

The Launcher itself is written in Python and uses the wxWidgets toolkit.  You can run the Launcher on Linux and Mac OS X as well.  Mac developers already have a native Launcher included with its SDK.  You can find the Mac Launcher source code over at the [Mac Launcher for Google App Engine](http://code.google.com/p/google-appengine-mac-launcher) page.

## The Launcher ##

![http://google-appengine-wx-launcher.googlecode.com/svn/site/images/launcher-screen.png](http://google-appengine-wx-launcher.googlecode.com/svn/site/images/launcher-screen.png)

Here you can see the Launcher window with four projects.  The first project is currently running locally on port 8080.  The second project, not running, is currently selected.  You can run it, see the logs, edit the project's YAML configuration, deploy it to appspot.com, and see the project dashboard.  The last project, displayed in red, has had its local files removed.  Removing a project from the Launcher does not affect the files on disk, and removing the files on disk won't remove the project from the Launcher.

## Development ##

### Prerequisites ###

You may need a  few other packages to run the Launcher from out of the source tree:

On **Windows**, you will need
  * Python 2.5 or later (NOT cygwin's python!).  You can download this from http://www.python.org/download/
    * For example, to get Python 2.5.2, download http://www.python.org/ftp/python/2.5.2/python-2.5.2.msi
  * The wxPython toolkit: http://wxpython.org/download.php
    * For example, http://downloads.sourceforge.net/wxpython/wxPython2.8-win64-unicode-2.8.9.1-py25.exe
  * If you plan on editing the UI, you'll need to get wxGlade: http://sourceforge.net/projects/wxglade
  * The Launcher uses some Windows extensions, so you need the pywin32 package: http://sourceforge.net/projects/pywin32/
  * Finally, if you wish to create a stand-alone `exe` on Windows, you'll need py2exe: http://sourceforge.net/project/showfiles.php?group_id=15583

Several of the above pieces (e.g. Python and pywin32) need to be matched.  Be sure to read the various product's release notes for compatibility issues.


On **Linux**, you need most of the same things as windows (of course, you won't need pywin32).  `sudo apt-get install python-wxversion python-wxglade` should be adequate to pull in the necessary moving pieces.

On **Mac**, virtually all needed packages come pre-installed with the OS.  The exception is wxGlade which can be found at http://sourceforge.net/projects/wxglade.    You only need wxGlade if you plan on editing the UI components.

### Running ###

Run the Launcher like any other python program.  E.g. `C:\Python25\python.exe GoogleAppEngineLauncher.py`, or `./GoogleAppEngineLauncher.py`, depending on your platform.

On MacOS 10.6, the pre-installed wxWidgets are 32-bit only, so python must be run in 32-bit mode: `VERSIONER_PYTHON_PREFER_32_BIT=yes ./GoogleAppEngineLauncher.py`.

### Unit Tests and Code Coverage ###

The Launcher team believes in the value of unit tests.  To run the tests, you will need two additional libraries:
  * PyMox, a mock object framework for Python, found at http://code.google.com/p/pymox/.
  * Ned Batchelder's Python coverage tool, found at http://nedbatchelder.com/code/modules/coverage.html.

We're working on a new unit test runner, but for now, the command `coverage.py` found at the top level of the source tree will run all unit tests and generate code coverage numbers. You will need to adapt this script to your environment by changing the `COVSCRIPT` variable to point to your coverage tool.  `coverage.py` command runs on all 3 platforms and does not require a cygwin installation on Windows. To run unit tests for just one file, use the syntax `./coverage.py launcher/blah_unittest.py`.

At this time, code coverage from the unit tests is 84%.

## Deployment ##

For Windows, the Launcher is converted to an executable with the command `python setup.py py2exe`.


