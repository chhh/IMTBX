# Download IMTBX+Grppr
Precompiled binaries for *Win-x64* are available in the
[Releases](https://github.com/chhh/IMTBX/releases/latest) section of the
GitHub repository.

## What's in the distribution

* `WatersIMSPeakDetector.exe` - The peak detection program for Waters .RAW
files.
* `WatersDataPlotter.exe` - Data viewer for both regular MS and IM-MS data from
Waters' instruments.
* `grppr-0.3.6.jar` - Isotopic clustering program.


## Requirements

* `WatersIMSPeakDetector.exe` and `WatersDataPlotter.exe`
  * Require *.NET 4.5.1* installed. If you're on Windows 10, you already have
  it. Most likely you have it on older systems as well, but if the program
  doesn't run, you can get it
  [here](https://www.microsoft.com/en-us/download/details.aspx?id=40773).
* `grppr-0.3.6.jar`
  * Requires *Java 1.8* installed. If you don't want to install the standard
  one from Oracle, you can get an alternative OpenJDK pre-built distribution
  for Win/Linux/Max [here](https://www.azul.com/downloads/zulu/).



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
