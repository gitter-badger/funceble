_A script to check domains or IP accessibilities._

The main idea was to create a script that can **check if domain** or a **list of domains** are/is **ACTIVE** or **INACTIVE**. And, in between, **create a hosts file** based on the results.

# Issues

For all issues/bugs and others, please report [here](https://github.com/funilrys/funceble/issues/new).

# Version

Current Version: **1.2.2**

# Usage

## funceble

```sh
Usage: ./funceble [ -a ] [ -ex ] [ --help ] [ -h ] [ -ip ] [ -q ] [ -n ] [ -p ] [ --split ]

       {[ -d domain-name.me ]} || {[ -f listOfDomainInAFile ]}

  --all                      -a              Output all information on screen (Must be before -d or -f)
  --domain                   -d              Domain to analyze
  --file                     -f              File with a list of domains
  --execution                -ex             Show the execution time (Must be before -d or -f)
  --help                                     Print this screen
                             -ip             Change the ip to print in host file (Must be before -d or -f)
  --host                     -h              Activate the generation of host (Must be before -d or -f)
  --quiet                    -q              Activate quiet mode (Must be before -d or -f)
  --percentage               -p              Show the percentage of the results (Must be before -d or -f)
  --noFiles                  -n              Deactivate the production of output files (Must be before -d or -f)
  --split                                    Split output files (Must be before -d or -f)
```

## tool

```sh
Usage: ./tool [ -d ] [ -h ]

       {[ -i ]} || {[ -p ]} || {[ -u ]}

  --debug                    -d              Activate the debug mode with the installation (Must be before -u or -i)
  --help                                     Print this screen
  --installation             -i              Execute the installation script
  --production               -p              Prepare the repository for production
  --update                   -u              Update the script
```

# Status

* **ACTIVE**
    * `whois` return the date of expiration
    * `nslookup` don't return "**server can't find domain-name.me: NXDOMAIN**"
* **INACTIVE**
    * `whois` don't return anything
    * `nslookup` return "**server can't find domain-name.me: NXDOMAIN**"
* **INVALID**
    * Domain extension has an invalid format or is unregistered in **[IANA](https://www.iana.org/domains/root/db) Root Zone Database**.

# How to contribute?

To contribute, you have to send a new [Pull Request](https://github.com/funilrys/funceble/compare) after you [forked](https://github.com/funilrys/funceble/pulls#fork-destination-box) and edited the script(s).

## DO NOT FORGET

* To sign your commit(s) with **'Signed-off by: FirstName LastName <e at mail dot com>'** AND/OR simply sign your commit(s) with **PGP**. **Please read more [here](https://github.com/blog/2144-gpg-signature-verification)**.
* All contributions/modifications must be done under **the `dev` branch**.

____
# Special Thanks
Thank you guys for your awesome lists which helped _(and still help)_ me build this script. :smile: :+1:

* [@mitchellkrogza](https://github.com/mitchellkrogza)
* [@PromoFaux](https://github.com/PromoFaux) with [Pi-Hole](https://github.com/pi-hole/pi-hole) hosts file.

# Contributors

* [@WaLLy3K](https://github.com/WaLLy3K)

____
# `Hosts` files

## What is a hosts file?

A hosts file, named `hosts` (with no file extension), is a plain-text file
used by all operating systems to map hostnames to IP addresses.

In most operating systems, the `hosts` file is preferential to `DNS`.
Therefore if a domain name is resolved by the `hosts` file, the request never
leaves your computer.

Having a smart `hosts` file goes a long way towards blocking malware, adware, ransomware, porn and other nuisance websites.

A hosts file like this causes any lookups to any of the listed domains to resolve back to your localhost so it prevents any outgoing connections to the listed domains.

## Recommendations

I'd personally recommend using [Steven's hosts](https://github.com/StevenBlack/hosts) or [Pi-Hole](https://github.com/pi-hole/pi-hole) which are in my opinion the best out there.
