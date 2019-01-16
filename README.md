## Restaurant Reviews Project

This project attempts at creating a UI for searching and reading reviews of restaurants filtered by neighborhoods and cuisines.

## Pre-requisites
1. Need to have python installed in the computer

## Instructions to run the project
1. Clone this repository into a folder say 'restrntRevs' and cd into that folder.
2. In this folder, start up a simple HTTP server to serve up the site files on your local computer.
(Below instruction has been borrowed from Udacity Instructor Notes)
   * In a terminal, check the version of Python you have: `python -V`. If you have Python 2.x, spin up the server with `python -m SimpleHTTPServer 8000` (or some other port, if port 8000 is already in use.) For Python 3.x, you can use `python3 -m http.server 8000`. If you don't have Python installed, navigate to Python's [website](https://www.python.org/) to download and install the software.
   * Note -  For Windows systems, Python 3.x is installed as `python` by default. To start a Python 3.x server, you can simply enter `python -m http.server 8000`.


## About the solution
1. My contribution in this project has mainly been with the css (for responsiveness and accessibility) and adding of the service worker to enable assets to be available offline.
2. The starter kit had much of the javascript ready to use taking care of event handling, data population for select drop-downs, results served from database requests. The only changes I made in javascript were to:-
   1. add aria attributes and roles to html elements for enhancing accessibility
   2. register the service worker on DOMContentLoaded event
3. Notes on changes to CSS/HTML:-
   1. Used flexbox to serve restaurant list on index.html for smaller viewports and css grid for larger
   vieports
   2. Used some google fonts to enhance design linked the appropriate css in the html page
   3. added styles for hover and focus for accessibility
   4. modified html to use semantic elements such as sections
4. Service worker
   (A lot of this code should be credited to Instructor lessons and Udacity and
    https://developers.google.com/web/fundamentals/primers/service-workers/)
   1. On DOMContentLoaded: Attempts to  register
   2. On self install: Attempts to cache all the assets of the website into a cache named
   'restrnt-assets-cache-v1'
   3. On self activation: Deletes the previous cache
   4. On Fetch: Attempts to serve assets from cache. On failure fetches assets from the network
