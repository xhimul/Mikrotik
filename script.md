- Simple Queue for L3 DC > `:for x from=2 to=200 do={/queue simple add name="User-$x" dst=0.0.0.0/0 max-limit=10M/10M target="172.16.17.$x"}`

- Simple Queue > `:for x from=31 to=200 do={/queue simple add name="User-$x" dst=0.0.0.0/0  max-limit=5M/5M target="192.168.1.$x"}`





- https://wiki.mikrotik.com/wiki/Manual:Scripting
- http://phallaccmt.blogspot.com/2016/02/mikrotik-schedulscript-check-wans-to.html
- http://85.254.195.66/manual/Basic/Scripting.html
