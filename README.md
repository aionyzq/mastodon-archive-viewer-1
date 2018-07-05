## How to install mastodon-archive-viewer

First you need an initialized OPAM installed
If you don't have it installed, it can be fetched from your system packages manager.
Then to initialize it, do `opam init -a`, then `eval $(opam config env)`

Now, to install mastodon-archive-viewer, do `opam pin add mav .`

## How to use mastodon-archive-viewer

Now that mastodon-archive-viewer is installed you just need to download the archive you want
to view, extract it in a new directory, then do:

```
$ cd <the archive directory>
$ mav outbox.json
```

## Troubleshootings

If the installation fails somewhere while building the dependencies, you might miss one of
these tools on your systems: make, gcc, m4, libc-dev.
This might happen on a newly installed Alpine Linux, for instance.

## TODO

* Detect toot privacy (which seems kind of hard)
* Detect gifs vs. videos
* Testing (I guess I missed some heuristics, help welcome!!)
* Documentation
* A better short name (I don't like "mav" and I'd like to find a better one)
* Clean code and better errors
