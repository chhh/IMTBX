# Quick Start

## Download
Follow
[this GitHub repository link](https://github.com/chhh/IMTBX/releases/latest)
to get the latest available pre-built binaries.  

!!! note "Note"
    64-bit Windows only. NET 4.5.1 required, It won't work under Mono.

## Typical usage

1. Show available commands:  
    `WatersIMSPeakDetector.exe help`  
* Show documentation for the `peaks` command that extracts single features from
raw data:
    `WatersIMSPeakDetector.exe help peaks`  
* Detect peaks (the most basic):  
    `WatersIMSPeakDetector.exe peaks --orig -o "+Results" -i
    "path/to/input.RAW"`  
    * The `+` sign in `-o` argument tells the program that the output path is
      relative to the input path. You could also use `+../Results-2017` to place
      the results into a new subfolder `Results-2017` on level higher that the
      input file.
* Detect peaks (specifying filter size and shape):  
    `WatersIMSPeakDetector.exe peaks -f 2 2 1 1 2 2 --hyper 0.2 0.5 0.3
    --orig -o "+Results" -i "path/to/input.RAW"`
        * `--filter` specifies the filter size in points.
        * `--hyper` specifies how quickly the filter falls off.
