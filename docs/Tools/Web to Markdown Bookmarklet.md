Dumping the current page to markdown could be pretty useful, couldn't it? 

Here's a magic [[bookmarklet]] for your bookmarks bar: 

```
javascript:(function(){  var currentURL = window.location.href;  var newURL = "https://r.jina.ai/" + currentURL;  window.location.href = newURL;})();
```

Drag the link below to your bookmarks bar:
[Jina-Chop](javascript:(function(){  var currentURL = window.location.href;  var newURL = "https://r.jina.ai/" + currentURL;  window.location.href = newURL;})();)