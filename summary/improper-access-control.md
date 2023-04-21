# 🛸 Improper access control

## vuls

### 0x01 Privilege Escalation

> [https://hackerone.com/reports/1114617](https://hackerone.com/reports/1114617)

### 0x02 Validate Session

> [https://hackerone.com/reports/1295187](https://hackerone.com/reports/1295187)
>
> [https://hackerone.com/reports/1166076](https://hackerone.com/reports/1166076)

#### How-to

1. login the same account at two browser
2. change the password in one.
3. check the session whether validation in another one

### 0x03 X-Forwarded-For

> [https://hackerone.com/reports/382678](https://hackerone.com/reports/382678)



### 0x04 Password Reset Link

> [https://hackerone.com/reports/1288898](https://hackerone.com/reports/1288898)



* How-to:
* send the reset link
* change password by active session(user after login).
* whether the reset link is expiring

> [https://hackerone.com/reports/1177287](https://hackerone.com/reports/1177287)

How-to:

* &#x20;Request a password reset link for a valid account&#x20;
* Click on the reset link&#x20;
* Before resetting the password click on webiste&#x20;
* You will notice the following request in burpsuite

### &#x20;<a href="#undefined" id="undefined"></a>

### ​ <a href="#undefined" id="undefined"></a>

### 0x05 Account

> [https://hackerone.com/reports/1202590](https://hackerone.com/reports/1202590)



### 0x06 Publicly Accessible

> [https://hackerone.com/reports/1004964](https://hackerone.com/reports/1004964)



### 0x07 403 Bypass

> [https://hackerone.com/reports/1219681](https://hackerone.com/reports/1219681)



#### How-to:

Try 127.0.0.1

#### reference:

> [https://vulners.com/hackerone/H1:991717](https://vulners.com/hackerone/H1:991717)



> [https://hackerone.com/reports/991717](https://hackerone.com/reports/991717)

#### How-to:

curl -H "Content-Length:0" -X POST [U](https://www.xn--4zhaaaaaaa.mil/%E2%96%88%E2%96%88%E2%96%88)RL



### 0x08 Token Leak

> [https://hackerone.com/reports/1210043](https://hackerone.com/reports/1210043)



### 0x09 No Rate Limitation(Email Flooding/Email bombing)

> No Rate Limit On Forgot Password Page:
>
> [https://hackerone.com/reports/1245529](https://hackerone.com/reports/1245529)

> No Rate Limit (Leads to huge email flooding/email bombing):
>
> [https://hackerone.com/reports/272596](https://hackerone.com/reports/272596)
>
> [https://hackerone.com/reports/1337425](https://hackerone.com/reports/1337425)



### Others

> [https://hackerone.com/reports/1234746](https://hackerone.com/reports/1234746)

##

## articles
