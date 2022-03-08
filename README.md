# requested-domains
DNS enumeration of domains seen on IT Army of Ukraine telegram channel.

### The following items are contained in the tarball 1__all_domains.tar.gz:

Data was gathered only using Subfinder and DNSENUM with a custom dictionary of just over 101,000 subdomains.  See dict.txt 


### Project URLs:
https://github.com/projectdiscovery/subfinder && https://github.com/fwaeytens/dnsenum


### Files in the root:

__1__all_domains.tar.gz__ is all the domains enumerated to date.  As of now, gov.ru is still undergoing enumeration.  gov.ru has a LOT of subdomains, and some have a wildcard DNS entry.

dict.txt is the dictionary used for DNSENUM.

domains.txt is the list of domains enumerated.

### ENUMERATED_DOMAINS folder:

Files ending in __.dns__ contain discovered subdomains that resolve (from sublister) + subdomains bruteforced with DNSENUM.  I have not looked for DNSENUM results that have a wildcard DNS entry, but it will make it unusually large, and therefore affect the .dns file for the same domain.  I'll work on that. 

Files ending in __.subdomain_ips__ have subdomains that can be resolved with public DNS, discovered by running Sublister.  The 1st field in these files are used for part of the files with the .dns extension (mentioned above).

Files ending in __.subdomain_all__ have all Subfinder found subdomains.  Subdomains that do not resolve could either, 1. no longer exist, or 2. could be private hostnames that only resolve with internal DNS, but for which a certificate had been requested ... could be interesting.

Files ending in __.dnsenum__ contain the full output of DNSENUM.  I will work on cleaning up any domains with a wildcard DNS.  An example of that is rs.gov.ru, which if a hostname is queried that doesn't exist, it will return __89.208.226.52__.


### File Types:

All files in the tarball are text only.  There is no code of any kind in these files.
