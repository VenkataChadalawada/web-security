# Iframe
- An iframe or an inline frame allows you to load content from another site inside your webpage
- Iframe have their own url which can point to any site on the inetrnet
`<iframe src="http://www.nytimes.com/" width="800" height="300"></iframe>`
Iframe allows:
- frame based layouts
- 3rd party content embedding
- content isolation

Issues of Iframe
- click jacking
- can display malicious content
- webpage redirection
- malware
- interference


### Sandboxing Iframes
- we need a way to allow iframe to do stuff without interfering with our website
- the principle of least privilege using the `sandbox` attribute
this allows you to specify what exactly your iframe can and cannot do.
- you have very granular control over the privileges of the iframe.
- eg
```
<iframe sandbox="">
</iframe>
```
- no js execution
- same origin
- no new windows or dialouges `window.open` `target="_blank"`
- no forms or plugins you cant submit
- no parent navigation
- no auto-triggered features 

you cant have all these restrictions 
```
<iframe sandbox="allow-same-origin allow-scripts allow-popups allow-forms"
src="https://twitter.com/123"
></iframe>

```
