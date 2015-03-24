CouchIDE
========
Version `0.6 Alpha`

Install
-------
*this is still blue skies and as there is nothing there yet is for now just a dream, or a lie*

1. Go to [couchide.easier.io/install-on-my-own-server](http://couchide.easier.io/install-on-my-own-server)

2. Enter the server where you want to install CouchIDE

3. Authenticate with your username and password and press install

4. Go to the URL of the database you installed

5. Enter the editor by going to `*/_ide/` and set up the URL to visit your site on.

You can always return to CouchIDE to edit your files.

Build from source
-----------------
*nothing here*

Features
--------
*none*

Backlog
-------
The Backlog and Roadmap for CouchIDE can be found at [The issue tracker or the HuBoard](https://huboard.com/EasierIO/CouchIDE/#/)

Router
------
| From | Where
|-|
| `/` | Opens up the `index.html` file (or the home file you specify in the editor)
| `/_files/*filename*` | Opens up a file by it's name you can specify in the editor.
| `/_ide` | Open up the editor.
| `/_session` | The session endpoint.
| `/_api` | The endpoint for the API
| `/_lib/*packagename*/*versionname*/*` | Packages installed and managed
| `/_db` | The endpoint for the database
