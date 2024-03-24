# Google-Dorks
[![License](https://img.shields.io/badge/license-MIT-_red.svg)](https://opensource.org/licenses/MIT)

Google dorks, also known as Google hacking or Google dorking, refer to specialized search queries that use advanced operators to find specific information indexed by Google's search engine. These queries are typically crafted to uncover vulnerabilities, sensitive data, or information that is not readily accessible through conventional searches.

Google dorks are often utilized by security professionals, hackers, and researchers to identify potential security flaws, exposed data, or misconfigured systems on the internet. They can be used to find anything from exposed databases and login credentials to vulnerable websites and confidential documents.

While Google dorks can be powerful tools for legitimate purposes such as security testing and research, they can also be exploited for malicious activities if used unethically. Therefore, it's important for users to exercise caution and ensure that they comply with relevant laws and ethical guidelines when employing Google dorks.

![image](https://assets.securitytrails.com/cdn-cgi/image/width=800,quality=80,format=auto/blog/google-hacking-techniques/thumbs/4x3.jpg)

## Search filters

| Filter          | Description                                        | Example                              |
| :-------------- |:---------------------------------------------------| :------------------------------------|
| allintext      | Searches for occurrences of all specified keywords. | `allintext:"keyword"` |
| intext      | Searches for the occurrence of keywords at once or consecutively. | `intext:"keyword"` |
| intitle      | Searches for occurrences of keywords in the title all or one. | `intitle:"keyword"` |
| allintitle      | Searches for all occurrences of keywords at once. | `allintitle:"keyword"` |
| inurl      | Searches for a URL that matches one of the keywords. | `inurl:"keyword"` |
| allinurl      | Searches for a URL that matches all the keywords in the query. | `allinurl:"keyword"` |
| site      | Searches specifically for that particular website and lists all results for that website. | `site:"www.github.com"` |
| filetype      | Searches for a specific file type named in the query. | `filetype:"pdf"` |
| link      | Searches for external links to pages. | `link:"keyword"` |
| numrange      | Used to find specific numbers in your search. | `numrange:33-43` |
| before/after      | Used to search within a specified date range. | `filetype:pdf & (before:2021-01-01 after:2021-05-01)` |
| allinanchor (and also inanchor)      | This shows the websites that the keywords refer to in links, in order of most links. | `inanchor:rat` |
| allinpostauthor (and also inpostauthor)      | Exclusively for the blog search, blog posts written by specific people are picked out. | `allinpostauthor:"keyword"` |
| related      | List web pages that are "similar" to a given web page. | `related:www.github.com` |
| cache      | Displays the version of the web page that Google has in its cache. | `cache:www.github.com` |

## Examples

intext:"index of /"
Nina Simone intitle:”index.of” “parent directory” “size” “last modified” “description” I Put A Spell On You (mp4|mp3|avi|flac|aac|ape|ogg) -inurl:(jsp|php|html|aspx|htm|cf|shtml|lyrics-realm|mp3-collection) -site:.info
Bill Gates intitle:”index.of” “parent directory” “size” “last modified” “description” Microsoft (pdf|txt|epub|doc|docx) -inurl:(jsp|php|html|aspx|htm|cf|shtml|ebooks|ebook) -site:.info
parent directory DVDRip -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory MP3 -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
parent directory Name of Singer or album -xxx -html -htm -php -shtml -opendivx -md5 -md5sums
filetype:config inurl:web.config inurl:ftp
“Windows XP Professional” 94FBR
ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) (intext:confidential salary | intext:"budget approved") inurl:confidential
ext:(doc | pdf | xls | txt | ps | rtf | odt | sxw | psw | ppt | pps | xml) (intext:confidential salary | intext:”budget approved”) inurl:confidential
<br><br>

![image](https://user-images.githubusercontent.com/6010786/152770177-537fbfa2-235e-4951-a885-12c6a90c40a5.png)

## Operators
#### Search Term

This operator searches only for the exact term inside the quotation marks. You can use this for example if the term you are looking for is ambiguous and could easily be confused with something else, or if you don't get enough relevant results. 

Here is an example:

```
"Admin Loginpage"
```
#### OR
This operator searches for a specific search term OR another term.

```
site:instagram.com | site:github.com
```

#### AND
This operator searches for a specific search term and another term.

```
site:github.com & site:twitter.com
```

#### Operators combinaison
This operator combines search terms 
```
(site:instagram.com | site:twitter.com) (intext:"admin")
(site:instagram.com | site:twitter.com) & intext:"admin"
```

#### Include results

This will order results by the number of occurrence of the keyword.

```
site:twitter.com +site:twitter.*
```

#### Exclude results

```
site:twitter.* -site:twitter.com
```

### Better Results (Subdomains)
```
site:*.site.com

site:*.*.site.com

site:*.*.*.site.com
```
#### Synonyms

```
~set
```

#### Glob pattern (*)

```
site:*.com
```

# Ideas
- [x] Git google dorks
- [x] phpmyadmin google dorks
- [x] phpinfo google dorks
- [x] log file google dorks
- [x] google dorks for excel files
- [ ] Google Dorks for presentations 
- [ ] best google dorks reports 
- [x] finding aws secrets with google dorks
- [ ] js secrets with google dorks
- [ ] CMS google dorks
  - [x] Wordpress
  - [x] Typo3
  - [x] Magento
  - [x] Joomla
  - [ ] Drupal
  - [ ] Shopify
- [x] Admin google dorks
- [x] Monitoring pages - google dorks
- [ ] Google Dorks - Github page


# Links

- exploit-db.com
- nvd.nist.gov
- cxsecurity.com
- vulnerability-lab.com 

## Preventing Google Dorks

Encoding/encrypting sensitive data such as usernames, passwords and so forth.
Run inquiries against your own site to check whether you can locate any sensitive data. On the off chance that you discover sensitive information, you can remove it from search results by utilizing Google Search Console.
Protect sensitive content by utilizing a robots.txt document situated in your root-level site catalog. 
Utilizing robots.txt helps prevent Google from indexing our site, but it can also show an attacker where sensitive data might be located.
User-agent: * 
Disallow: / 

You can also block specific directories to be excepted from web crawling. 
If you have the /phpinfo site and you need to protect it, just place this code inside:

User-agent: *   
Disallow: /phpinfo/ 


Restrict access to specific files:

User-agent: *   
Disallow: /member/info.html 

Restrict access to dynamic URLs that contain ? symbol:

User-agent: *   
Disallow: /*?  

# My Love Google Dork 
```
allintext:password filetype:log

```
More about google dorks checkout this https://medium.com/@thek4rthi/unveiling-google-dorks-an-easy-guide-to-advanced-search-techniques-220e2ed67f7f

# Disclaimer: DONT BE A JERK!
Needless to mention, please use this tool very very carefully. The authors won't be responsible for any consequences.
