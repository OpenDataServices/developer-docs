# Working Off-line

## Grab GitHub issues to work offline e.g.

```
wget -m --no-parent  -e robots=off "https://github.com/OpenDataServices/developer-docs/issues/"
```

The best way to view these is probably with a local instance of apache, e.g.:
```
cd github.com
docker run -d -v "$PWD":/usr/local/apache2/htdocs/ -p 127.0.0.1:8005:80 httpd:2.4
```

## Google Drive

With a chrome browser and the appropriate apps/settings it is possible 
to work off-line with documents, spreadsheets, etc

## Developing Off-line

GitHub issues can be grabbed (see above).

Git generally works well for offline usage. Remember that if you've done a git fetch (or git pull) before going offline, then you can interact with remote branches at origin/branch_name.

We use Content Delivery Networks quite often for style and layout (e.g.
Bootstrap), sometimes these can be a pain off-line. These are often heavily cached, so it can be better to be completely offline where the cached copy will be used immediately, rather than online on a flakey connection where the browser may hang checking for new versions of these files. Similarly doing a soft reload with Ctrl+L and then enter may keep the cache, whereas Ctrl+R will try to bust it.

Some of our applications rely on data fetched remotely - we should try to avoid this wherever possible, and describe workarounds in the applications README (e.g. faking with /etc/hosts) where this issue remains.
