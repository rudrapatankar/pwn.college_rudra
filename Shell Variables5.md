# Shell Variables

## Printing exported variables


### Solve
FLAG=pwn.college{wnzr69D4Inil-NEK1x-KIKRU5KT.QX4UTN0wiNxIzNzEzW}

env prints all the exported variables	in the shell

```bash
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=d5bd3050beacc62ffa4d635e7fb60eafc4ee6d9b86f488101c1f2a95f32d83d5
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{wnzr69D4Inil-NEK1x-KIKRU5KT.QX4UTN0wiNxIzNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive

FLAG=pwn.college{wnzr69D4Inil-NEK1x-KIKRU5KT.QX4UTN0wiNxIzNzEzW}

```

### New Learnings
env prints all the exported variables	in the shell

### References 
N.A.
