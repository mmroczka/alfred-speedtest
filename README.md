# Alfred Workflow - Wifi Speedtest
Test the Upload/Download speed of the wifi you're currently on

[![alfred-speedtest.png](./alfred-speedtest.png)](./alfred-speedtest.png)

## Installation

1. Install `speedtest-cli` on your system using homebrew: `brew install speedtest-cli`.
2. Download the [workflow](https://github.com/mmroczka/alfred-speedtest/blob/master/Speedtest.alfredworkflow)
3. Double click to install it in Alfred

## Usage

Use the keyword `speedtest`, wait 30 seconds while the speedtest is running, view the notification that pops up.

## What's inside?

One line of code:

```bash
/usr/local/Cellar/speedtest-cli/$(ls /usr/local/Cellar/speedtest-cli | grep "." | sort -V -r | head -n 1)/bin/speedtest | grep "Download\|Upload"
|___ speedtest cli path ___|     |__ parse for the latest version of speedtest cli in homebrew Cellar and return it ___|  |___ get just the results of the upload/download__|
```

## Discussion

On Alfred forum:

## Known issues

Installing without homebrew will result in you needing to change the path name.

