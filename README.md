# Router Tetris

When I was writing some scripts for my asus routers, I suddenly wanted to try if I could play games on the router, so I tried to find some games written in shell scripts, at first I wanted to try The Game of Life, But the CPUs usage is always 100% due to many calculations, I ended up going with Tetris, after trying a few I decided to fork [@ContentsViewer](https://github.com/ContentsViewer)'s [shtris](https://github.com/ContentsViewer/shtris) and make compatibility improvements.


## The main changes I made are:

Because the `sleep` provided by busybox does not support floating point numbers, use `usleep` instead.

Changed thespecial character for `GHOST_CELL` to ensure better compatibility.


## Usage

```sh
# go to the temporary directory (this game will be deleted after restarting the router)
cd /tmp

# download
wget https://raw.githubusercontent.com/l11/router-tetris/main/shtris -O ./shtris

# add permissions
chmod +x ./shtris

# run it
sh ./shtris
```

<details>
<summary>Show Help</summary>

```shellsession

$ ./shtris -h
Usage: shtris [options]

Options:
 -d, --debug          debug mode
 -l, --level <LEVEL>  game level (default=1). range from 1 to 15
 --rotation <MODE>    use 'Super' or 'Classic' rotation system
                      MODE can be 'super'(default) or 'classic'
 --lockdown <RULE>    Three rulesets —Infinite Placement, Extended, and Classic—
                      dictate the conditions for Lock Down.
                      RULE can be 'extended'(default), 'infinite', 'classic'
 --seed <SEED>        random seed to determine the order of Tetriminos.
                      range from 1 to 4294967295.
 --no-color           don't display colors
 --no-beep            disable beep
 --hide-help          don't show help on start
 -h, --help     display this help and exit
 -V, --version  output version infromation and exit
 
Version:
 3.0.0
```

</details>


## Supported Environments

| Environment                                       | Support              |
| :-----------------------------------------------: | :------------------: |
| Asuswrt 386.x and higher  (sh by busybox)         | o                    |
| Asuswrt-Merlin 386.x and higher  (sh by busybox)  | o                    |
| Fresh Tomato 2022 (sh by busybox)                 | o (Not fully tested) |


 ## Notice
 
I did testing on an RT-AC86U running 386.5_2 (this is a cortex-a53 router with dual core 1.8GHz) but the CPUs usage is still over 80% in play and stutters as the difficulty level of the game increases will be more serious.

So, this is just a test of whether the router CPUs can handle a simple game, enjoy it or not.

This fork is designed to be compatible with specific platforms, and as a proof of concept for running games on routers, it may not be actively maintained in the future, any issues in [the original code](https://github.com/ContentsViewer/shtris) should be submitted directly to [the original project](https://github.com/ContentsViewer/shtris/issues), and any comments about this project should be in [the discussion](https://github.com/l11/router-tetris/discussions).

## Screenshot from original project
![shtris](https://contentsviewer.work/Master/ShellScript/Apps/Tetris/Images/shtris.jpg)

 
## Credit

**Original Author:**
 
IOE <Github: [@ContentsViewer](https://github.com/ContentsViewer)>
 
**Compatibility Modifier:**
 
OOOD <Github: [@oood](https://github.com/oood)>
 

## License

(MIT License)[https://github.com/l11/router-tetris/blob/main/LICENSE]
 
