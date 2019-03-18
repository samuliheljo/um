% Curl(shell) Um Pages | Um Pages
%
% October 15, 2018
# NAME
curl --

# EXAMPLES

## Curl for some address and display time (Accept gzip)

```
URL="http://samuliheljo.com";
COOKIE="";
for X in `seq 60`; do
  curl -k \
    -w "HTTPCODE=%{http_code} time_appconnect=%{time_appconnect} time_connect=%{time_connect} time_starttransfer=%{time_starttransfer} time_total=%{time_total}\n" \
    -H "cookie: $COOKIE" \
    -H "Accept-Encoding: gzip" \
    $URL -so /dev/null;
done
```

where

http_code           The  numerical  response  code that was found
                    in the last retrieved HTTP(S) or FTP(s) transfer.

time_appconnect     The time, in seconds, it took from the start until
                    the SSL/SSH/etc connect/handshake to the remote host
                    was completed.

time_connect        The time, in seconds, it took from the start until
                    the TCP connect to the remote host (or proxy) was
                    completed.

time_namelookup     The time, in seconds, it took from the start until the name
                    resolving was completed.

time_pretransfer    The time, in seconds, it took from the start until the
                    file transfer was just about to begin.

time_starttransfer  The time, in seconds, it took from the start until the first
                    byte was just about to be transferred.

time_total          The total time, in seconds, that the full operation lasted.


see: https://ops.tips/gists/measuring-http-response-times-curl/

