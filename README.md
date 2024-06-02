# Dorks-for-BBH
Tips and tricks to find programms & Google Dorks
🚩 **“inurl:”Responsible disclosure” to print out all public programs for any company if they have !** 

- **site:*.domain.com ext:php** → This will search for PHP files on a domain. Useful for finding undisclosed phpinfo.php files or other sensitive scripts.
- **site:*.domain.com inurl:login | admin** - Find admin or login pages that may be vulnerable to brute force or default credentials.
- **site:*.domain.com intext:"sql syntax near" | intext:"syntax error has occurred" | intext:"mysql_fetch_array()"** - Find pages that reveal SQL errors and may indicate SQL injection flaws.
- **site:*.domain.com ext:log | ext:txt | ext:bak** - Find log, text or backup files that may contain sensitive info.
- **site:*.domain.com inurl:"pwd=" | inurl:"pass=" | inurl:"password="** - Find pages that may leak passwords or sensitive data in URLs.
- **site:*.domain.com intitle:"index of" | inurl:"rsync"** - Find directory listings that should be blocked.
- **site:*.domain.com inurl:"shell.php" | inurl:"backdoor.php" | inurl:"cmd.php"** - Locate common webshells and backdoors.
- **site:*.domain.com ext:git** - Find exposed .git folders that reveal source code.
- **site:*.domain.com inurl:/.svn/entries** - Locate exposed subversion metadata.
- **site:*.domain.com inurl:"/api/v1"** - Find API endpoints that may not be protected.

Here is a google dork to search for **backup** files and **admin panels/logins** on subdomains of a site:

> site:*.example.com ext:bak | ext:backup | ext:sql | ext:gz | ext:tar | ext:zip | inurl:/admin | inurl:/wp-login.php | intitle:"admin panel" | intitle:"admin login"
> 

**Breakdown**:

- site:*.example.com - Searches all subdomains of example.com
- ext:bak | ext:backup | ext:sql | ext:gz | ext:tar | ext:zip - Looks for various file extensions commonly used for backups
- inurl:/admin | inurl:/wp-login.php - Finds admin directories or WordPress admin login pages
- intitle:"admin panel" | intitle:"admin login" - Finds pages with "admin panel" or "admin login" in title

—

Google Dork - all the juicy extensions

site:"target[.]com" ext:log | ext:txt | ext:conf | ext:cnf | ext:ini | ext:env | ext:sh | ext:bak | ext:backup | ext:swp | ext:old | ext:~ | ext:git | ext:svn | ext:htpasswd | ext:htaccess

__

Google Dork - Open Redirect

inurl:url= | inurl:return= | inurl:next= | inurl:redirect= | inurl:redir= | inurl:ret= | inurl:r2= | inurl:page= inurl:& inurl:http site:target[.]com

__

> This Google dork is searching for sensitive information disclosure vulnerabilities on a site. Let's break it down:
> 

inurl:email= | inurl:phone= | inurl:password= | inurl:secret= inurl:& site:target[.]com

⇒ Google Dork - High % inurl keywords

inurl:config | inurl:env | inurl:setting | inurl:backup | inurl:admin | inurl:php site:example[.]com

---
https://my.tomorrowland.com/forgotpassword/confirm?code=290336&email=mal_00%2Buser2%40intigriti.me
