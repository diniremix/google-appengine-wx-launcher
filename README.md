**This project is Automatically exported from code.google.com/p/google-appengine-wx-launcher**

# Google App Engine wxLauncher
http://code.google.com/p/google-appengine-wx-launcher
http://code.google.com/appengine

This project contains source code for the launcher, a wxWidgets based
developer tool for creating, running, and deploying Google App Engine
applications.  This launcher is included in the Windows installer for
the App Engine SDK starting with version 1.2.5.  This launcher also
works on Linux and Mac but is not distributed in the App Engine SDK
for those platforms.  The launcher delivered with the App Engine Mac
SDK, GoogleAppEngineLauncher.app, is also open source:
http://code.google.com/p/google-appengine-mac-launcher

See the [google-appengine-wx-launcher](http://code.google.com/p/google-appengine-wx-launcher) project site for details on
prerequisites for running the launcher on various platforms
(e.g. **wxPython**).

For development we use the script coverage.py to run unit tests.  (A
nicer test runner is currently out for review).  Until that lands you
may need to edit coverage.py to work in your environment.  This
coverage.py script uses PyMox and the excellent code coverage script
found here: http://code.google.com/p/pymox/
http://nedbatchelder.com/code/modules/coverage.html


### Requeriments (Gnu/Linux)
On Linux, you need most of the same things as windows (of course, you won't need pywin32). *sudo apt-get install python-wxversion python-wxglade* should be adequate to pull in the necessary moving pieces.


- [python](http://wxpython.org/download.php)  2.7.x
- [wxglade](http://wxpython.org/download.php) 2.8.x


## Instal Requeriments (Debian/Ubuntu based)
```bash
sudo apt-get install python-wxversion python-wxglade
```


## How to use
Clone this repo.

    git clone https://github.com/diniremix/google-appengine-wx-launcher.git


>Addtional we are used a [.desktop file](http://standards.freedesktop.org/desktop-entry-spec/latest) for launch the app, by defaul please App Engine Launcher are installed in **~/bin** folder, please edit if path are changed


## Changelog

- fixed for Google app engine **1.9.24**  see commit [4bb5599](https://github.com/diniremix/google-appengine-wx-launcher/commit/4bb5599) 


### Contact
[Diniremix](https://github.com/diniremix)

email: *diniremix [at] gmail [dot] com*
