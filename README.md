Nagios Plugin: check_domain
============================

A Nagios plugin for checking a domain expiration date by registry name.  


> This plugin relies on [jwhois](https://github.com/jodrell/jwhois) to find the registration 
> dates so any TLD that is not supported by whois will not return correctly and will output
> something similar to the following:
> 
> 	Error running whois:
>
> Thanks to [glensc](https://github.com/glensc) for his work on [nagios-plugin-check_domain](https://github.com/glensc/nagios-plugin-check_domain) 
> which inspired this php version of his shell plugin.

Usage:

	$./check_domain.php -d nagios.org
	OK - Domain nagios.org will expire in 248 days (2015-10-04)

Full Usage:

	check_domain.php - v1.1.0
        Copyright (c) 2014 Luke Groschen, Nagios Enterprises <lgroschen@nagios.com>, 
                      2009-2014 Elan Ruusamäe <glen@pld-linux.org>
	Under GPL v2 License

	This plugin checks the expiration date of a domain name.

	Usage: check_domain.php -h | -d <domain> [-c <critical>] [-w <warning>] [-s <whoisServer>]
	NOTE: -d must be specified

	Options:
	-h
	     Print this help and usage message
	-d
	     Domain name to query against
	-w
	     Response time to result in warning status (days)
	-c
	     Response time to result in critical status (days)
	-s
		 Specify a whois server (whois.internic.net by default)

	This plugin will use the whois service to get the expiration date for the domain name.
	Example:
	     $./check_domain.php -d nagios.com -w 30 -c 10 \n\n"
