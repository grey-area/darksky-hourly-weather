# Dark Sky Hourly Weather

A simple Python script intended for getting an hourly weather forecast using the Dark Sky API.

## Requirements & Setup

You'll need termcolor, which can be installed via pip.

You'll need to replace the dummy key in the config.json file
with a key obtained from [Dark Sky](https://darksky.net/dev).

This script is currently set up for only two locations: HOME and WORK. You'll want to replace
the (decimal) latitudes and longitudes of these in the config.json file.

## Use

Just run

```console
./weather [--no-request --compact --location <HOME/WORK>]
```

to get hourly weather information for your location. The returned columns are time, temperature,
precipitation intensity (mm), precipitation probability, and weather summary.

Any row for which the precipitation probability is greater than 20% or 40% will be displayed in gellow or red.

The --no-request flag causes the script to display the weather information
that was last retrieved, without making a new request to Darksky.

The --compact flag will display the weather in a more compact form, displaying only the time,
temperature, and precipitation probability columns.

Use the --location argument to set the location of the forecasts, using the options from
the config.json file.

## Example Output

Thursday 3 January 2019, requested at 14:45
=============================================
02 PM	3°C	0.0mm, 0%	Overcast
03 PM	3°C	0.0mm, 0%	Mostly Cloudy
04 PM	2°C	0.0mm, 0%	Partly Cloudy
05 PM	0°C	0.0mm, 0%	Clear
06 PM	-1°C	0.0mm, 0%	Clear
07 PM	-1°C	0.0mm, 0%	Clear
08 PM	-2°C	0.0mm, 0%	Clear
09 PM	-2°C	0.0mm, 0%	Clear
10 PM	-2°C	0.0mm, 0%	Clear
11 PM	-2°C	0.0mm, 0%	Clear
