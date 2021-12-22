iosetopts
=====

Library to use `io:setopts/1` on startup of application. Useful for application that are starting with -noshell in production, but need encoding set to unicode.

Config
------

What you pass into opts will be used during app start.

```erlang
[
    {iosetopts,
        [{opts, %% see https://www.erlang.org/doc/man/io.html#type-setopt
            [{encoding, unicode}]
        }]
    }
].
```

Build
-----

    $ rebar3 compile
