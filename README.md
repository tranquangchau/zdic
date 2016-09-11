# zdic
汉典谷歌浏览器插件




Of me.
basis
https://developer.chrome.com/extensions/getstarted

update file popup.js
to
```
chrome.tabs.executeScript( {
  code: "window.getSelection().toString();"
}, function(selection) {
	//alert(selection);
  var query = encodeURIComponent(selection[0] || '汉典')
  document.querySelector('iframe').src = 
    'https://vdict.com/' + query+',1,0,0.html'
    //'https://www.google.com.vn/search?q=' + query
    //'https://vi.m.wikipedia.org/wiki/' + query
});
```
