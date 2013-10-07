CouchIDE
========

Drop this design doc into your database, instant webserver.

*Current state*

Nothing uploaded to github yet, sorry

Features
- HTML/JS/CSS code highlighting and advanced editor. Supports multiple cursors.
- New file, save and delete
- Open files from the sidebar
- Remembers the line number on save making editing easier
- Tells you when your file was last saved
- Somewhat displays on mobile
- Keybindings for the Ace editor are at 
  https://github.com/ajaxorg/ace/wiki/Default-Keyboard-Shortcuts

Feature requests
- Change file name
- Package in 1 design doc with router and editor for easy dropping
- Authorisation
- VHosts installation
- Folder structure?
- Works on mobile
- Loads file from url

Future Router
/           =>    /index.html
/x          =>    /x
/couchide   =>    CouchIDE editor
/couchide/* =>    Open file in CouchIDE editor
/_ session  =>    ../../../_session
