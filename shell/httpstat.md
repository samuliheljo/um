% httpstat(shell) Um Pages | Um Pages
%
% October 15, 2018
# NAME
httpstat --

# EXAMPLES

## httpstat for some address and display time (Accept gzip)

```
URL="http://samuliheljo.com/";
COOKIE="";
httpstat $URL -k -H "cookie: $COOKIE" -H "Accept-Encoding: gzip"
```

## Links

https://github.com/reorx/httpstat