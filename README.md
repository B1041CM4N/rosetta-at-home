# Rosetta@home - help in the fight against COVID-19

With the recent COVID-19 outbreak, R@h has been used to predict the structure of proteins important to the disease as well as to produce new, stable mini-proteins to be used as potential therapeutics and diagnostics, like the one displayed above which is bound to part of the COVID-19 spike protein. [Read more](http://boinc.bakerlab.org/rosetta/)

This project has been built to get you up and running with as many devices as possible for the least effort.

## Hardware compatibility
This project should run on all 64-bit OS devices with 2 or more GB of RAM, but we've tested on the below:
* Raspberry Pi 4 (2GB RAM) **Note:** GPU memory allocation must be set to 16MB within device configuration
* Raspberry Pi 4 (4GB RAM)
* NVIDIA Jetson Nano
* Intel NUC (and other generic x86_64 devices)

## Getting started

This is a containerized application intended to run on [balenaCloud](https://www.balena.io/cloud/), which allows you to deploy it to an entire fleet of devices with a single command. BalenaCloud covers 10 devices for free, but if you want to run this application on a larger fleet please [get in touch](mailto:hello@balena.io).

### Setup the device(s)

* Sign up for or login to the [balenaCloud dashboard](https://dashboard.balena-cloud.com)
* Create an application, selecting the correct device type
* Add a device to the application, enabling you to download the OS
* Flash the downloaded OS to your SD card with [balenaEtcher](https://balena.io/etcher)
* Power up the Pi and check it's online in the dashboard

### Deploy this application

* Install the [balena CLI tools](https://github.com/balena-io/balena-cli/blob/master/INSTALL.md)
* Login with `balena login`
* Download this project and from the project directory run `balena push <appName>` where `<appName>` is the name you gave your balenaCloud application in the first step.
* The application will then be downloaded and started by each device in your fleet.

For further information, see the [balenaCloud documentation](https://www.balena.io/docs/learn/getting-started/jetson-nano/nodejs/).

## Customization

By default, your device will contribute work units to the [balena team](https://boinc.bakerlab.org/rosetta/team_display.php?teamid=18832). To override this and contribue to a team of your choosing, you can set your account authentication key by using the [environment variable](https://www.balena.io/docs/learn/manage/serv-vars/) `ACCOUNT_KEY`, set from the balenaCloud dashboard. This will automatically update the XML configuration file with your key and ensure you're credited for completed work units.

## FAQ

* You can start the cli-based UI by running `boinctui` within a terminal to the `main` container.

* If you are not receiving work units, in `boinctui` try pressing F9 -> rosetta -> update.

## Contributing

We encourage you to submit bug reports, feature requests and PRs, compatibility updates, everything! Let's get this running on as many devices as we can.

## Support

If you have issues deploying or running this project please start a thread in the [balena forums](https://forums.balena.io) and we'll be happy to help.