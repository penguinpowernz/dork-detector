dork-detector
=============

A Debian package to use the Linux/Cdorked.A detector from ESET to monitor a system for the malware using cron.


## What is this

This is a tool that can check your system for the Linux/Cdorked.A malware simple by running `dork-detector check`.  However so you don't have to do this all the time a cron entry is also installed to scan for the malware every hour automatically.

It uses the [tool from ESET for detecting and dumping Linux/Cdorked.A memory if it is found on the system](http://www.welivesecurity.com/wp-content/uploads/2013/04/dump_cdorked_config.c).

## How to install

You will need to have gcc installed so the tool can be built for you system.  This is specified as a requirement in the DEBIAN control file so that it can be automatically installed by apt-get.

```sh
sudo dpkg -i dork-detector.deb
apt-get -f install
```

## Todo

* alert the admin when the malware is found
* allow sending of the dump to ESET lab
* check web server binaries for known malware hashes

## More information

For more information about this malware see the [ESET blog entry on Linux/Cdorked.A](http://www.welivesecurity.com/2013/05/07/linuxcdorked-malware-lighttpd-and-nginx-web-servers-also-affected/).
