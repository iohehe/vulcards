# vuls

* [727330-header-modification-results-in-disclosure-of-slack-infra-metadata-to-unauthorized-parties](https://app.gitbook.com/@iohehe/s/vulcards/~/drafts/-MbkyiHGsd0pQ-L6TGtB/vuls/2021/6/09): using \`X-Forwarded-Host\` header test a SSRF, and use @ symbol bypass. e.g. X-Forwarded-Host: a.com@vul.com



## 

* [**GitLab**](https://hackerone.com/gitlab) disclosed a bug submitted by [**ajxchapman**](https://hackerone.com/ajxchapman)  [FogBugz import attachment full SSRF requiring vulnerability in \*.fogbugz.com](https://hackerone.com/reports/1092230)13 Jul 2021 

as the code in app/services/projects/download\_service.rb\#

```ruby
WHITELIST = [ /^.freeze
...
def valid_url?(url) url && http?(url) && valid_domain?(url) end
def http?(url) url =~ /\A#{URI::DEFAULT_PARSER.make_regexp(%w(http https))}\z/ end
def valid_domain?(url) host = URI.parse(url).host WHITELIST.any? { |entry| entry === host } end
```

  
If a vulnerability be identified in a fogbugz.com subdomain, can results a crafted API response including an arbitrary attachment URL, a full read GET based SSRF would be exploitable on \`gitlab.com\`.

* [**GitLab**](https://hackerone.com/gitlab) disclosed a bug submitted by [**ajxchapman**](https://hackerone.com/ajxchapman)  [FogBugz import attachment full SSRF requiring vulnerability in \*.fogbugz.com](https://hackerone.com/reports/1092230)13 Jul 2021 

as the code in app/services/projects/download\_service.rb\#

```ruby
WHITELIST = [ /^.freeze
...
def valid_url?(url) url && http?(url) && valid_domain?(url) end
def http?(url) url =~ /\A#{URI::DEFAULT_PARSER.make_regexp(%w(http https))}\z/ end
def valid_domain?(url) host = URI.parse(url).host WHITELIST.any? { |entry| entry === host } end
```

  
If a vulnerability be identified in a fogbugz.com subdomain, can results a crafted API response including an arbitrary attachment URL, a full read GET based SSRF would be exploitable on \`gitlab.com\`.

