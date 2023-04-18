# 🧶 SSRF

##

## Vuls:

### 0x01&#x20;

{% embed url="https://hackerone.com/reports/727330" %}

> How-to:

using \`X-Forwarded-Host\` header test a SSRF, and use @ symbol bypass. e.g. X-Forwarded-Host: a.com@vul.com



### 0x02

{% embed url="https://hackerone.com/reports/1092230" %}

> How-to:

as the code in app/services/projects/download\_service.rb#

```ruby
WHITELIST = [ /^.freeze
...
def valid_url?(url) url && http?(url) && valid_domain?(url) end
def http?(url) url =~ /\A#{URI::DEFAULT_PARSER.make_regexp(%w(http https))}\z/ end
def valid_domain?(url) host = URI.parse(url).host WHITELIST.any? { |entry| entry === host } end
```

\
If a vulnerability be identified in a fogbugz.com subdomain, can results a crafted API response including an arbitrary attachment URL, a full read GET based SSRF would be exploitable on \`gitlab.com\`.

* [**GitLab**](https://hackerone.com/gitlab) disclosed a bug submitted by [**ajxchapman**](https://hackerone.com/ajxchapman) \
  [FogBugz import attachment full SSRF requiring vulnerability in \*.fogbugz.com](https://hackerone.com/reports/1092230)13 Jul 2021&#x20;

as the code in app/services/projects/download\_service.rb#

```ruby
WHITELIST = [ /^.freeze
...
def valid_url?(url) url && http?(url) && valid_domain?(url) end
def http?(url) url =~ /\A#{URI::DEFAULT_PARSER.make_regexp(%w(http https))}\z/ end
def valid_domain?(url) host = URI.parse(url).host WHITELIST.any? { |entry| entry === host } end
```

\
If a vulnerability be identified in a fogbugz.com subdomain, can results a crafted API response including an arbitrary attachment URL, a full read GET based SSRF would be exploitable on \`gitlab.com\`.



### 0x03

{% embed url="https://hackerone.com/reports/978823" %}

### 0x04 cve-2021-22958

{% embed url="https://hackerone.com/reports/863221" %}

### 0x05 cve-2019-8451

{% embed url="https://hackerone.com/reports/713900" %}

> HOW-TO:

Test the path: /plugins/servlet/gadgets/makeRequest

![SSRF](<../.gitbook/assets/image (9) (3).png>)

> reference:

{% embed url="https://jira.atlassian.com/browse/JRASERVER-69793" %}

##

## Articles:

{% embed url="https://www.hackerone.com/application-security/how-server-side-request-forgery-ssrf" %}
