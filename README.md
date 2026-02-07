# mkpasswd for Debian system
This tiny script to create password candidates is for `Debian` System that doesn't have `mkpasswd` command natively.
Perhaps using this script can be used more easily than building mkpasswd command from source codes.

#### Usage

`mkpasswd [-s|--simbol] [length] [number of password candidates]`

  - When using option `-s` or `--simbol`, password candidates includes some simbol characters. If you wish to edit excluding simbols, set environment variable `MKPWD_EXCHR`. `MKPWD_EXCHR` default value is `!&*()[]{}<>?|/\;`

  - When not giving `number of password candidates`, default is `1`.
  - When not giving `length`, default is `42`.
  - I recomend you to install `pwgen` package using `sudo apt-get install pwgen`. It presents better passwords.
  - When not installed `pwgen`, `mkpasswd` uses `/dev/uramdom` instead and prints an alert message, `Please install "pwgen" to make it more convenient.`

#### Example
1. `$ mkpasswd`<br />
   `ofiecooCh7reikofaixiK9xaej9cogai9ahchiepha`<br />

1. `$ mkpasswd 24`<br />
   `UochohriPohzie4yoh9Ep3wa`<br />


1. `$ mkpasswd 24 4`<br />
   `jaiXiy7hiuHoh4uqui9yie7g`<br />
   `Evij3iesh9ahnah9zooHai9e`<br />
   `aihoVaepieniting7eoboe9r`<br />
   `Aixo7roh7ANahz7okeaphire`<br />

1. `$ mkpasswd 24 -s`,<br />`$ mkpasswd -s 24`,<br />`$ mkpasswd --simbol 24` or<br />`$ mkpasswd 24 --simbol`<br />
   `I^:aBtUnyh=g,^#IWtCz7va,`<br />


#### License
MIT License.
