# mkpasswd for Debian system
This tiny script to create password candidates is for Debian System that doesn't have mkpasswd command natively.
Perhaps using this script can be used more easily than building mkpasswd command from source codes.

#### Usage

`mkpasswd [-s|--simbol] [length] [number of password candidates]`

  - When using option `-s` or `--simbol`, password candidates includes some simbole characters. If you wish to edit excluding simboles, set environment variable `MKPWD_EXCHR`. `MKPWD_EXCHR` default value is `!&*()[]{}<>?|/\;`

  - When not giving `number of password candidates`, default is `1`.
  - When not giving `length`, default is `42`.
  - I recomend you to install `pwgen` package using `sudo apt-get install pwgen`. It presents better passwords.
  - When not installed `pwgen`, `mkpasswd` uses `/dev/uramdom` instead and prints an alert message, `Please insall "pwgen" to make it more convenient.`

#### Example
1. `$ mkpasswd`
   `ofiecooCh7reikofaixiK9xaej9cogai9ahchiepha`
   `$`

1. `$ mkpasswd 24`
   `UochohriPohzie4yoh9Ep3wa`
   `$`


1. `$ mkpasswd 24 4`
   `jaiXiy7hiuHoh4uqui9yie7g`
   `Evij3iesh9ahnah9zooHai9e`
   `aihoVaepieniting7eoboe9r`
   `Aixo7roh7ANahz7okeaphire`
   `$`

1. `$ mkpasswd 24 -s`, `mkpasswd -s 24`, `mkpasswd --simbol 23` or `mkpasswd 24 --simbol`
   `I^:aBtUnyh=g,^#IWtCz7va,`
   `$`


#### License
MIT License.
