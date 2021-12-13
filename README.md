# sh-tetris

Tetris game written in pure sh.

This script is based on [dkorolev/bash-tetris](https://github.com/dkorolev/bash-tetris)
Thank you!

## Feature

The implementation follows [Tetris Guideline. Tetris Wiki. accessed at 2020-05-23](https://tetris.fandom.com/wiki/Tetris_Guideline).

* [x] Hold Queue
* [x] Next Queue
* [x] Random Generation with Bag System
* [x] Score System
* [x] Variable Goal System
* [x] T-Spin / Mini T-Spin
* [x] Back-to-Back Bonus
* [x] Extended Placement / Infinite Placement / Classic Lock Down
* [x] Super / Classic Rotation System
* [x] Changing the Starting Level
* [ ] Ghost Piece

## Usage

```sh
# Download (v2.1.0)
wget https://raw.githubusercontent.com/ContentsViewer/sh-tetris/v2.1.0/tetris
chmod +x tetris

# Local
./tetris

# Global
sudo install tetris /usr/local/bin
tetris
```

<details>
<summary>Show Help</summary>

```shellsession
$ ./tetris -h

Usage: tetris [options]

Options:
 -d, --debug          debug mode
 -l, --level <LEVEL>  game level (default=1). range from 1 to 15
 --rotation <MODE>    use 'Super' or 'Classic' rotation system
                      MODE can be 'super'(default) or 'classic'
 --lockdown <RULE>    Three rulesets —Infinite Placement, Extended, and Classic—
                      dictate the conditions for Lock Down.
                      RULE can be 'extended'(default), 'infinite', 'classic'
 --no-color           don't display colors
 --no-beep            disable beep
 --hide-help          don't show help on start

 -h, --help     display this help and exit
 -V, --version  output version infromation and exit

Version:
 2.1.0
```

</details>

![Tetris](https://contentsviewer.work/Master/ShellScript/Apps/Tetris/Images/tetris.jpg)

Enjoy :-)

## Supported Environments

| Environment | Support? |
| :---------: | :------: |
| Linux   sh  | o        |
| FreeBSD sh  | o        |
| BusyBox sh  | o        |
| Solaris sh  | x        |

## Author

IOE <Github: [@ContentsViewer](https://github.com/ContentsViewer)>
