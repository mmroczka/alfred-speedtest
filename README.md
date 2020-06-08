# Alfred Workflow - Wifi Speedtest
Test the Upload/Download speed of the wifi you're currently on

[![alfred-speedtest-results.png](./alfred-speedtest-results.png)](./alfred-speedtest-results.png)

## Installation

1. Install `speedtest-cli` on your system using homebrew: `brew install speedtest-cli`.
2. Download the [workflow](https://github.com/mmroczka/alfred-speedtest/blob/master/Speedtest.alfredworkflow).
3. Double click to install it in Alfred.

## Usage

Use the keyword `speedtest`, wait 30 seconds while the speedtest is running, view the notification that pops up.


### Shortened version (cuts 30 seconds of waiting for speedtest to finish)
<img src="./alfred-speedtest-results-shortened.gif" alt="speedtest results short" width="800" height="400">

### Full length version
<img src="./alfred-speedtest-results-true-length.gif" alt="speedtest results true length" width="800" height="400">

## What's inside?

One (long) line of code:

```bash
/usr/local/Cellar/speedtest-cli/$(ls /usr/local/Cellar/speedtest-cli | grep "." | sort -V -r | head -n 1)/bin/speedtest | grep "Download\|Upload"
|_____________________________|  |______________________________________________________________________|               |________________________|
            |                                                      |                                                                 |
    SPEEDTEST-CLI PATH           PARSE FOR THE LATEST VERSION OF SPEEDTEST IN HOMEBREW CELLAR AND RETURN IT          GRAB RESULTS OF THE UPLOAD/DOWNLOAD
```

## Discussion

On Alfred forum:

## Known issues

Installing without homebrew will result in you needing to change the path name.

