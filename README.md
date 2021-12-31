# Alfred Workflow - Wifi Speedtest
Test the Upload/Download speed of the wifi you're currently on.

[![alfred-speedtest-results.png](./alfred-speedtest-results.png)](./alfred-speedtest-results.png)

## Installation

1. Install `speedtest-cli` on your system using homebrew: `brew install speedtest-cli`.
2. Download the [workflow](https://github.com/mmroczka/alfred-speedtest/blob/master/Speedtest.alfredworkflow).
3. Double click the downloaded workflow to install it in Alfred.

## Usage

Using the keyword `speedtest` in alfred, select the workflow then wait 30 seconds while the speedtest is running (a notification will appear letting you know it's started the test). After 30 seconds, view the notification that pops up with the results of the speedtest.


### Shortened version (cuts 30 seconds of waiting for speedtest to finish)
<img src="./alfred-speedtest-shortened.gif" alt="speedtest results short" width="800" height="400">


### Speedtest Results
[![alfred-speedtest-results.png](./alfred-speedtest-results.png)](./alfred-speedtest-results.png)


## What's inside?

One (long) line of code:

```bash
/usr/local/Cellar/speedtest-cli/$(ls /usr/local/Cellar/speedtest-cli | grep "." | sort -V -r | head -n 1)/bin/speedtest | grep "Download\|Upload"
|_____________________________|  |______________________________________________________________________|               |________________________|
            |                                                      |                                                                 |
    SPEEDTEST-CLI PATH           PARSE FOR THE LATEST VERSION OF SPEEDTEST IN HOMEBREW CELLAR AND RETURN IT          GRAB RESULTS OF THE UPLOAD/DOWNLOAD
    
```

## New bash command line for M1 Macs
please change the command line in Alfred to the following for M1 macs - "/opt/homebrew/Cellar/speedtest-cli/$(ls /opt/homebrew/Cellar/speedtest-cli | grep "." | sort -V -r | head -n 1)/bin/speedtest | grep "Download\|Upload"

## Discussion

On Alfred forum: https://www.alfredforum.com/topic/15046-alfred-wifi-speedtest/?tab=comments#comment-76923

## Known issues

Installing without homebrew will result in you needing to change the path name. Please change the path name in the bash script to wherever the `speedtest-cli` is installed on your system if you don't want to use Homebrew to install it.

