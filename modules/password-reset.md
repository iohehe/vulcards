---
description: https://anugrahsr.github.io/posts/10-Password-reset-flaws/
---

# Password reset



#### Exploitation <a href="#exploitation" id="exploitation"></a>

* Request password reset to your email address
* Click on the password reset link
* Dont change password
* Click any 3rd party websites(eg: Facebook, twitter)
* Intercept the request in burpsuite proxy
* Check if the referer header is leaking password reset token.

\