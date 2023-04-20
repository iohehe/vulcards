---
description: PUT method enabled
---

# PUT



The HTTP PUT method can be used to upload data that is saved on the server.

* We can use the OPTIONS method to list the HTTP methods&#x20;
* Allow lists the set of methods supported by a resources
* Access-Control-Allow-Methods indicates which HTTP methods are allowed on a particular endpoint for cross-origin requrests.
* Let's change the method from OPTIONS to PUT and check for the allowed methods.

![](<../.gitbook/assets/image (1) (3).png>)

If the PUT method appears to be present and enabled, we can even upload backdoor and application will respond with 201 created response as shown in the blow Exhibit:



![](<../.gitbook/assets/image (2) (2).png>)

![](<../.gitbook/assets/image (1) (2).png>)

* You may receive 405 status code if you attempt to use the PUT method where it is not supported.

> Note that the permissions are likely to be implemented per implemented per directory, so recursive checking is directories on the server for the PUT method.&#x20;

### ![](<../.gitbook/assets/image (7).png>)

### Demos:

{% embed url="https://hackerone.com/reports/545136" %}

### Articles:

{% embed url="https://portswigger.net/kb/issues/00100900_http-put-method-is-enabled" %}

{% embed url="https://www.arridae.com/blogs/HTTP-PUT-method.php" %}

{% embed url="https://www.hackingarticles.in/multiple-ways-to-exploiting-put-method/" %}

###

### Tools:

* davtest

{% embed url="https://github.com/cldrn/davtest" %}



* Cadaver

