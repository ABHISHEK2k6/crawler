# Overview
This script is a simple CSRF vulnerability scanner that checks if a webpage forms include a csrf_token field. The presence of a csrf_token is a common measure to prevent Cross-Site Request Forgery (CSRF) attacks.

## How It Works
Fetch the Webpage:
The script uses the requests library to fetch the HTML content of the target URL.

## Parse the HTML:
The BeautifulSoup library is used to parse the HTML and extract all <form> elements.

## Check for CSRF Tokens:
Each form is checked for an <input> element with the name attribute set to csrf_token.

If a form does not contain a csrf_token, the script flags it as potentially vulnerable.
### Output Results:
For each form missing the csrf_token, a message is printed indicating a potential CSRF vulnerability.

Example Usage
python
```bash
url = 'https://example.com'
csrf_scanner(url)
```
Dependencies
requests: For making HTTP requests to fetch webpage content.
beautifulsoup4: For parsing and analyzing HTML.
Installation
Install the required libraries using pip:

```bash
pip install requests beautifulsoup4
```
Notes
This scanner only checks for a basic csrf_token implementation. Websites may use other CSRF prevention methods, such as cookies or JavaScript-based tokens, which this script will not detect.
Always ensure you have permission to scan a website for vulnerabilities. Unauthorized scanning can be illegal.
