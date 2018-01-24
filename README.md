# ssl-date-checker-plus v1.0.4

Nodejs Library to check and report on the issues on and expiration date of a given SSL certificate for a given domain. Also reports issuer info and covered domains (only for JSON currently).  

Usage:

$ ssl-date-checker-plus host [-f text|json] [-p port]

Example results:

$ ssl-date-checker-plus npm.org

Certification for npm.org
Issue On: Dec 13 00:51:56 2014 GMT
Expires On: Jan 13 11:24:29 2017 GMT
Expires in 536 days

$ ssl-date-checker-plus npm.org -f json

Example results:

{
    "valid_from": "Oct 31 00:00:00 2016 GMT",
    "valid_to": "Oct 31 23:59:59 2018 GMT",
    "issuer_cn": "Symantec Class 3 EV SSL CA - G3",
    "valid_hosts": "DNS:www.apple.com, DNS:images.apple.com, DNS:trailers.apple.com, DNS:ssl.apple.com, DNS:apple.com, DNS:rebate.apple.com, DNS:helposx.apple.com, DNS:help.apple.com, DNS:helpqt.apple.com, DNS:documentation.apple.com",
    "expires": 280,
    "expired": false,
    "host": "apple.com"
}

## Installing

npm install ssl-date-checker-plus

## License

MIT
