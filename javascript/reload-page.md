# Reload a Page

Use the history go() method.

```html
<form>
  <input type="button" onClick="history.go(0)" value="Refresh" />
</form>
```

Alternatively, you can use cache control.

```
Cache-Control: no-cache, no-store, must-revalidate
Pragma: no-cache
Expires: 0
```

Set using Java or Node.js:

```java
response.setHeader("Cache-Control", "no-cache, no-store, must-revalidate"); // HTTP 1.1.
response.setHeader("Pragma", "no-cache"); // HTTP 1.0.
response.setHeader("Expires", "0"); // Proxies.
```

## References

1. [Reload From A User’s Click](https://www.htmlgoodies.com/getting-started/reloading-the-page/)
1. [History go() Method](https://www.w3schools.com/jsref/met_his_go.asp)
1. [History.go()](https://developer.mozilla.org/en-US/docs/Web/API/History/go) (MDN Web Docs)
1. [Reload a Page](https://jsfiddle.net/gkhays/zt20u7h4/5/) (JSFiddle)
1. [How do we control web page caching, across all browsers?](https://stackoverflow.com/a/2068407/6146580)
1. [Force browser to reload index.htm](https://stackoverflow.com/a/26818602/6146580)
