# Quick Start

## Download
Follow
[this GitHub repository link](https://github.com/chhh/IMTBX/releases/latest)
to get the latest available pre-built binaries.  

!!! note "Note"
    64-bit Windows only. NET 4.5.2 required, It won't work under Mono.


## Typical usage

1. Show available commands:  
    `IMTBX.exe help`  
* Show documentation for the `peaks` command that extracts single features from
raw data:
    `IMTBX.exe help peaks`  
* Detect peaks in Top-Down mode (the most basic version):  
    `IMTBX.exe peaks --mode Sum -wvl -o "+Results" -i
    "path/to/input.RAW"`  
    * The `+` sign in `-o` argument tells the program that the output path is
      relative to the input path. You could also use `+../Results-2017` to place
      the results into a new subfolder `Results-2017` on level higher that the
      input file, or just use an absolute path.
* Detect peaks (specifying filter size and shape):  
    `IMTBX.exe peaks --mode Sum -wvl -f 2 2 1 1 2 2 --hyper 0.2 0.5 0.3
    --orig -o "+Results" -i "path/to/input.RAW"`
        * `--filter` specifies the filter size in points.
        * `--hyper` specifies how quickly the filter falls off.
        * `--orig` flag makes it put all the results in yet another subfolder
        inside the one specified as `-o`. This is useful if you use an absolute
        path for `-o`, e.g. `c:\results`, and want to put the peaks files for
        each input file to a separate subfolder with the same name as the
        original RAW.
