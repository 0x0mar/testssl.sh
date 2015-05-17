
## Intro

[![Gitter](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/drwetter/testssl.sh?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

`testssl.sh` is a free command line tool which checks a server's service on any port for the support of TLS/SSL ciphers, protocols as well as some cryptographic flaws. It's designed to provide clear output for your "is this good or bad" decision.

It is working on every Linux distribution out of the box with some limitations of disabled features from the openssl client -- some workarounds are done with bash-socket-based checks. It also works on BSD and other Unices out of the box, supposed they have `/bin/bash` and standard tools like sed and awk installed. MacOS X and Windows (using MSYS2) work too. OpenSSL version >= 1 is highly recommended.

On github you will find in the master branch the development version of the software -- with new features and maybe some bugs. For the stable version and a more thorough description of the software please see [testssl.sh](https://testssl.sh/ "Go to the site with the stable version and more documentation"). 

New features in this stable release 2.4 are: 

* "only one cmd line option at a time"
* several tuning parameters on the cmd line (only available through environment variables b4): --assuming-http, --ssl-native, --sneaky, --warnings, --color, -- debug, --long
* certificate information
* more HTTP header infos (cookies+security headers)
* protocol check via bash sockets for SSLv2+v3
* debug handling significantly improved (verbosity/each function leaves files in $TEMPDIR) 
* BEAST check
* FREAK check
* Secure Client-Initiated Renegotiation check
* lots of cosmetic and maintainability code cleanups
* bugfixing

Contributions, feedback, also bug reports are welcome. For contributions please note: One patch per feature -- bug fix/improvement. Please file bug reports @ https://github.com/drwetter/testssl.sh/issues .

Update notification here or @ [twitter](https://twitter.com/drwetter). 


