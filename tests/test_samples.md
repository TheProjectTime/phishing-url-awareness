# Test Results

Python version used: Python 3.13.7 | Operating system: Windows 11 | Date: 29-10-2026

| #   | Input                                   | Expected result         | Actual result                                                                                 | Pass/Fail |
| --- | --------------------------------------- | ----------------------- | --------------------------------------------------------------------------------------------- | --------- |
| 1   | https://www.example.com/login           | No listed warning signs | No listed warning signs found. This does NOT prove safety.                                    | PASS      |
| 2   | http://192.0.2.10/account               | IP address + HTTP       | Uses an IP address instead of a familiar domain. Uses HTTP. HTTPS alone does not prove trust. | PASS      |
| 3   | http://example.com@sample.invalid/login | @ symbol + HTTP         | Contains an @ symbol; inspect carefully. Uses HTTP. HTTPS alone does not prove trust.         | PASS      |
| 4   | https://a.b.c.d.e.example.invalid/path  | Many hostname segments  | Contains many hostname segments/subdomains.                                                   | PASS      |
| 5   | https://xn--example.invalid/            | Punycode-style hostname | Contains a punycode-style hostname.                                                           | PASS      |

## Notes

I learned how to identify suspicious URL patterns, including
the @ symbol, IP addresses, HTTP connections, and unusual
hostname structures.

I also learned that a URL without these warning signs is
not necessarily safe. The program only checks selected patterns.

I was surprised that a URL can look legitimate but contain
a hostname or symbol that deserves closer inspection.
