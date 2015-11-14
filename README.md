# KeePass web app (unofficial)

This webapp can read KeePass databases. It doesn't require any server or additional resources.
It can be run either in browser, or as a desktop app. 

![screenshot](https://habrastorage.org/files/bfb/51e/d8d/bfb51ed8d19847d8afb827c4fbff7dd5.png)

# Quick Links

Web: [Web App](https://antelle.github.io/keeweb/)  
Desktop: [Windows](https://github.com/antelle/keeweb/releases/download/v0.3.0/KeeWeb.win32.exe)
[Mac OSX](https://github.com/antelle/keeweb/releases/download/v0.3.0/KeeWeb.mac.dmg)
[Linux](https://github.com/antelle/keeweb/releases/download/v0.3.0/KeeWeb.linux.x64.zip)  
Timeline: [Release Notes](release-notes.md)
[TODO](TODO.md)  
On one page: [Features](features.md)  
Twitter: [kee_web](https://twitter.com/kee_web)  

# Status

Reading and display is mostly complete; modification and sync is under construction, please see [TODO](TODO.md) for more details.

# Known Issues

These major issues are in progress, or will be fixed in next releases, before v1.0:

- dropbox sync is one-way: changes are not loaded from dropbox, only saved

# Self-hosting

Everything you need to host this app on your server is any static file server. The app is a single HTML file + cache manifest (optionally; for offline access).
You can download the latest distribution files from [gh-pages](https://github.com/antelle/keeweb/tree/gh-pages) branch.

# Building

The app can be built with grunt: `grunt` (html file will be in `dist/`).    
Desktop apps are built with `grunt desktop`. This works only in mac osx as it builds dmg; requires wine.  
To run Electron app without building, install electron package (`npm install electron-prebuilt -g`) and start in this way:
```bash
$ cd electron
$ electron . --htmlpath=../tmp
```

For debug build:

1. run `grunt`
2. run `grunt watch`
3. open `tmp/index.html`


# Contributing

Plugins are not supported for now. If you want to add a feature, please contact the author first. Pull requests, patches and issues are very welcome.  
If you have found an bug, please [open an issue](https://github.com/antelle/keeweb/issues/new) and fill in the app version and your user-agent 
(you can find these details in Settings/Help section).

# License

[MIT](https://github.com/antelle/keeweb/blob/master/MIT-LICENSE.txt)