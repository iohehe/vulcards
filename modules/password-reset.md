---
description: https://anugrahsr.github.io/posts/10-Password-reset-flaws/
---

# Password reset

## Test the password reset token leakage.  <a href="#exploitation" id="exploitation"></a>

#### Exploitation <a href="#exploitation" id="exploitation"></a>

* Request password reset to your email address
* Click on the password reset link
* Dont change password
* Click any 3rd party websites(eg: Facebook, twitter)
* Intercept the request in burpsuite proxy
* Check if the referer header is leaking password reset token.

## Test the password reset link reuse.



#### Exploitation <a href="#exploitation" id="exploitation"></a>

* Request password reset  to your email address
* Use it
* Use it again...





## Passby the validation to ATO



[https://0xmahmoudjo0.medium.com/admin-account-takeover-via-weird-password-reset-functionality-166ce90b1e58](https://0xmahmoudjo0.medium.com/admin-account-takeover-via-weird-password-reset-functionality-166ce90b1e58)&#x20;



\
