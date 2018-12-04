## Built a Chrome Extension using Javascript

Storage mechanism in chrome:

- chrome.storage.local  - uses localstorage
- chrome.storage.sync  - uses localstorage as well as sync data in other chrome browser. 


Create png images with below dimentions : 

- 19 X 19
- 128 X 128
- 150 X 150

Create a manifest.json file

```json
{
    "manifest_version": 2,
    "name": "Techie Tab",
    "description": "Dashboard tab for Techies",
    "version": "1.0.0",
    "icons": {
        "128": "icon_128.png"
    },
    "browser_action": {
        "default_icon": "icon.png",
        "default_popup": "popup.html"
    },
    "permissions": [
        "activeTab",
        "storage"
    ],
    "incognito": "split",
    "chrome_url_overrides": {
        "newtab": "index.html"
    }
}
```

### RSS Feed Reader

Below jquery plugin is used for rss feed reader.. <br/> 
https://github.com/sdepold/jquery-rss

jQuery-rss uses https://feedrapp.info/ to read feeds. This is an alternative to google feed api. 


---

### Notes:

Chrome Storage: 
https://developer.chrome.com/extensions/storage

