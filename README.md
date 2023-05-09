# Client router doesn't strip trailing slashes before redirecting

When navigating via link to a route that redirects, the client router doesn't
strip the trailing slash, causing the relative redirect to be based in the wrong
directory and the path to be `foo/foo/bar` instead of `foo/bar`.

If the link is opened in a new tab instead, everything works as expected.
