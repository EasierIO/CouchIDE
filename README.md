CouchIDE
========
Version `0.5`

1. Copy the design file `_design/couchide` to any CouchDB database and *BOOM*, instant webserver!

2. Well, it needs a bit of setup first, but hopefully this gets eliminated in the future.

3. Go to `http://YOURSI.TE/DATABASENAME/_design/couchide/_rewrite/couchide/`

4. Make a file called `index.html`

5. Go to `http://YOURSI.TE/DATABASENAME/_design/couchide/_rewrite/` and view the site.

You can always return to CouchIDE to edit your files.

Features:
-------------
- One design doc you drop into your database
- HTML/JS/CSS code highlighting and advanced editor. Supports multiple cursors.
- New file, save and delete
- Open files from the sidebar
- Remembers the line number on save making editing easier
- Tells you when your file was last saved
- Keybindings for the Ace editor are at 
  https://github.com/ajaxorg/ace/wiki/Default-Keyboard-Shortcuts
- Loads file in address bar plus rewrites URL for bookmarks and navigation
- Has new file snippets for fast development (html and json)
- Save with Command-S (mac) or Ctrl-S (windows)

Where is the source WTF?
-------------
The file `editor.html` is actually a large part of the source, it has the editor
(plus it loads some content from cdn) to edit your files. To upload this into a 
design document it is BASE64 encoded as an attachment in the 
`_design/couchide.json` file. So if you want to change the editor, edit 
`editor.html`, encode it into BASE64 and stick it where the BASE64 string is now
in the design document.

How do I set up CouchIDE for Offline editing
-------------
Create a database named 'libraries' and put attach the nessecary scripts to
documents there, for naming check the source. In the future I plan to offer a
libraries database for replication but I have not had the time yet.

I see 404's loading the scripts, yet the editor loads fine...
-------------
CouchIDE first looks for the javascript dependencies in the database `libraries`
and tries to load the scripts from there, if impossible because there is no 
libraries database it says 'screw it' and loads versions of an CDN.

Feature requests:
-------------
- Change file name
- Authorisation
- VHosts installation
- Folder structure?
- Works on mobile

Router
-------------
`/           =>    /index.html`

`/*          =>    /*`

`/couchide   =>    CouchIDE editor`

`/couchide/* =>    Open file in CouchIDE editor`

`/ _session   =>    ../../../ _session`

`/api/*      =>    ../../../*`

`/lib/*      =>    ../../../libraries/*`

`/db/*       =>    ../../*`
