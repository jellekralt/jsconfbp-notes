# Offensive and Defensive Strategies for Client-Side JavaScript Security
*Anand Vemuri* [@brownhat57]()

---

* relotnek/medcellar
* Burp suite (proxy)
* BeEF (Browser exploitation framework project)
* Kali Linux

## Fixing CSRF
* CSRF token
* Origin header (Quick Band Aid)
* CSP header (Another secondary measure)

## 3 important points
* Random !== Cryptographically Secure
* Implementation is Tough
  * Method interchange
  * Beware of CSRF token replay
  * Token must be tied to the users session on the server-side
  * CSRF Token exposed as GET param
* CORS
  * &ast; is bad
