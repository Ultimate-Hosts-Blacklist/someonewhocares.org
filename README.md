# About someonewhocares.org

[![Build Status](https://travis-ci.org/Ultimate-Hosts-Blacklist/someonewhocares.org.svg?branch=master)](https://travis-ci.org/Ultimate-Hosts-Blacklist/someonewhocares.org)

```
# This hosts file is brought to you by Dan Pollock and can be found at
# https://someonewhocares.org/hosts/zero/
# You are free to copy and distribute this file for non-commercial uses,
# as long the original URL and attribution is included.
#
# See below for acknowledgements.

# Please forward any additions, corrections or comments by email to
# hosts@someonewhocares.org

# Last updated: Mon, 12 Mar 2018 at 01:12:14 GMT

# Use this file to prevent your computer from connecting to selected
# internet hosts. This is an easy and effective way to protect you from
# many types of spyware, reduces bandwidth use, blocks certain pop-up
# traps, prevents user tracking by way of "web bugs" embedded in spam,
# provides partial protection to IE from certain web-based exploits and
# blocks most advertising you would otherwise be subjected to on the
# internet.

# There is a version of this file that uses 127.0.0.1 instead of 0.0.0.0
# available at https://someonewhocares.org/hosts/.
# On some machines this may run minutely faster, however the zero version
# may not be compatible with all systems.

# This file must be saved as a text file with no extension. (This means
# that the file name should be exactly as below, without a ".txt" appended.)

# Let me repeat, the file should be named "hosts" NOT "hosts.txt".

# For Windows 9x and ME place this file at "C:\Windows\hosts"
# For NT, Win2K and XP use "C:\windows\system32\drivers\etc\hosts"
#                       or "C:\winnt\system32\drivers\etc\hosts"
# For Windows 7 and Vista use "C:\windows\system32\drivers\etc\hosts"
#			or "%systemroot%\system32\drivers\etc\hosts"
# For Windows 8 and Windows 10 use "C:\Windows\System32\drivers\etc\hosts"
# 		You may need to tell Windows Defender to ignore this path
# 		see: http://support.microsoft.com/kb/2764944
# You may have to use Notepad and "Run as Administrator"
#
# For Linux, Unix, or OS X place this file at "/etc/hosts" or on some
#    systems at "/private/etc/hosts". You will require root access to do
#    this. Saving this file to "~/hosts" will allow you to run something
#    like "sudo cp ~/hosts /etc/hosts".
# For OS/2 copy the file to "%ETC%\HOSTS" and in the CONFIG.SYS file,
#    ensure that the line "SET USE_HOSTS_FIRST=1" is included.
# For BeOS place it at "/boot/beos/etc/hosts"
# On a Netware system, the location is System\etc\hosts"
# For Macintosh (pre OS X) place it in the Mac System Folder or Preferences
#    folder and reboot. (something like HD:System Folder:Preferences:Hosts)
#    Alternatively you can save it elsewhere on your machine, then go to the
#    TCP/IP control panel and click on "Select hosts file" to read it in.
#    ------------------
#    | As well, note that the format is different on old macs, so
#    | please visit https://someonewhocares.org/hosts/zero/mac/ for mac format
# For Android place the file at "/system/etc/hosts". You will need root
#   access on your device to do this.
#    ------------------
# To convert the hosts file to a set of Cisco IOS commands for Cisco routers
#   use this script by Jesse Baird:
#   http://jebaird.com/blog/hosts-ip-host-generating-blocked-hosts-host-file-cisco-router

# If there is a domain name you would rather never see, simply add a line
# that reads "0.0.0.0 machine.domain.tld". This will have the effect of
# redirecting any requests to that host to your own computer. For example
# this will prevent your browser from downloading banner ads, or sending
# your information back to a company.
```

--------------------------------------------------------------------------------

# About Ultimate-Hosts-Blacklist

[Ultimate-Hosts-Blacklist](https://github.com/Ultimate-Hosts-Blacklist) serve a place to test and keep a track on each input sources that are present into [Ultimate Hosts Blacklist](https://github.com/mitchellkrogza/Ultimate.Hosts.Blacklist).

As [Ultimate Hosts Blacklist](https://github.com/mitchellkrogza/Ultimate.Hosts.Blacklist) grew up it became impossible to test the whole repository, as it takes weeks to finish. That's why we use the GitHub organization system in order to create different repository for each list that are present into [Ultimate Hosts Blacklist](https://github.com/mitchellkrogza/Ultimate.Hosts.Blacklist).

--------------------------------------------------------------------------------

# About PyFunceble

PyFunceble like [Funceble](https://github.com/funilrys/funceble) is A tool to check domains or IP availability by returning 3 possible [status](https://github.com/funilrys/PyFunceble/wiki/Columns#status): ACTIVE, INACTIVE or INVALID.

It also has been described by one of its most active user as:

> [An] excellent script for checking ACTIVE, INACTIVE and EXPIRED domain names.

If you need further informations about PyFunceble or Funceble please report to our [Wiki page](https://github.com/funilrys/PyFunceble/wiki) and/or if you don't find any answer feel free to create an issue into one of the [Dead Hosts](https://github.com/search?q=user%3Adead-hosts&type=Repositories&utf8=%E2%9C%93)'s or [Py-Funceble](https://github.com/search?utf8=%E2%9C%93&q=funceble+user%3Afunilrys&type=)'s repositories.

## About the status returned by PyFunceble

For an up to date version of this part please report to the [Status](https://github.com/funilrys/PyFunceble/wiki/Columns#status) section of our Wiki.

### ACTIVE

This status is returned when **one of the following cases** is met:

- We can extract the expiration date from `Lookup().whois()`.

  - _Please note that we don't check if the date is in the past._

- `Lookup().nslookup()` don't return `server can't find domain-name.me: NXDOMAIN`.

- `HTTOCode().get()` return one the following code `[100, 101, 200, 201, 202, 203, 204, 205, 206]`.

### INACTIVE

This status is returned when **all the following cases** are met:

- We can't extract the expiration date from `Lookup().whois()`.
- `Lookup().nslookup()` return `server can't find domain-name.me: NXDOMAIN`.

### INVALID

This status is returned when **the following case** is met:

- Domain extension has an invalid format or is unregistered in **[IANA](https://www.iana.org/domains/root/db) Root Zone Database**.

  - Understand by this that the extension **is not present into the `iana-domains-db.json` file**.
