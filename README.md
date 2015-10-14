# refresh-ios-profiles
Downloads and installs all iOS provisioning profiles from Apple Developer Portal. This is an utility script for CI environments for downloading and installing iOS provisioning profiles. At the core it is using the [sigh](https://github.com/KrauseFx/sigh) command.

# What it can do ?

* Download and install all profiles from Apple Developer Portal
* Download and install profiles from multiple teams from one call
* Install profiles located in ```~/Library/MobileDevice/Extra```

## How to install ?

```shell
sudo gem install sigh
brew tap xfreebird/utils
brew install refresh-ios-profiles
```

## Usage

```shell
export APPLE_USERNAME="myapple@gmail.com"
export APPLE_PASSWORD="supersecret"
refresh-ios-profiles "Team name1, Team name 2, Other team name"
```

If you want to install additional profiles that are not available from Apple Portal (you've been given only the certificate and the profile), then copy it(them) to ```~/Library/MobileDevice/Extra``` to make sure that each time the profiles are refreshed these ones are copied too.

