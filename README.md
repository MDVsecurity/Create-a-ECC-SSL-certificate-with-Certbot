## <font color="#512DA8"> **Part.2 Coming soon...**</font>

# How to Generate a ECC - SSL Certificate with Certbot.

### Note this is only for ACME-Challenge
\
The first thing that we have to do is install certbot.

	 pip install certbot

Once you install the library, let's start...

--- 

### **Here is the Complete Code ** ✅

	sudo certbot certonly --manual -d example.com -d www.example.com --agree-tos --manual-public-ip-logging-ok --preferred-challenges http-01 --server https://acme-v02.api.letsencrypt.org/directory --register-unsafely-without-email --key-type ecdsa

---


### *Explanition of the code:* 📖

\
<tab>
1. The `certbot` initialize the command 

\
<tab>

2. The `certonly` subcommand tells Certbot to obtain a certificate but not to install it.

\
<tab>

3.  The `-d` flag specifies one or more domain names for which you want to obtain a certificate. In this case, you are requesting a certificate for `example.com` and `www.example.com`.

\
<tab>
<font color="#E91E63"> **Beware Here**</font>

if you add `--manual-public-ip-logging-ok` to your code possible you `can't` create more SSL certificates
\
<tab>

4. The `--agree-tos` flag indicates that you agree to the terms of service for Let's Encrypt. The `--manual-public-ip-logging-ok` flag allows Let's Encrypt to log your public IP address for the purposes of detecting abuse.

\
<tab>

5. The `--preferred-challenges` flag specifies the challenge type that you prefer to use for domain validation. In this case, you are using the HTTP challenge, which requires you to create a specific file on your web server in order to prove that you control the domain.

\
<tab>

6. The `--server` flag specifies the ACME server to use for the certificate request. ACME (Automated Certificate Management Environment) is a protocol for automating the process of issuing and renewing SSL/TLS certificates.

\
<tab>

7. The `--register-unsafely-without-email` flag tells Certbot to register an account with Let's Encrypt without providing an email address. This is not recommended, as it may make it more difficult to recover your account in the event of a problem.

\
<tab>

8. The `--key-type` flag specifies the type of private key to use for the certificate. In this case, you are using an elliptic curve digital signature algorithm (ECDSA) key.

\
<tab>
---

*The easiest way to me is do it with acme-challenge.*

## And That's all! for now! 👌
Made with <font color="#EB144C"> **❤️**</font> to Everyone.
