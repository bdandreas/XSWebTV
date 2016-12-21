This version has been introduced at [date needed].
Improvements over the previous version:
* Support additional channels from supscription packages
* Has been documented: https://webtv-api.xs4all.nl/2/doc
* ...

The base URL of this version is https://webtv-api.xs4all.nl/2/

# Functions
(Needs more documentation)
## Metadata functions
* authenticate    
URL: https://webtv-api.xs4all.nl/2/authenticate
* listpackages   
URL: https://webtv-api.xs4all.nl/2/listpackages
* listallchannels   
URL: https://webtv-api.xs4all.nl/2/listallchannels

## Stream functions
### low
Supplies the url for the low quality stream of the given channel:    
https://webtv-api.xs4all.nl/2/channel/[channel]/[format]/low
### medium

Supplies the url for the medium quality stream of the given channel:    
https://webtv-api.xs4all.nl/2/channel/[channel]/[format]/medium
### high

Supplies the url for the high quality stream of the given channel:    
https://webtv-api.xs4all.nl/2/channel/[channel]/[format]/high   
[channel] is derived from output of listallchannels, e.g. 'ned1'
[format] can be either 'apple' or 'silverlight-drm'


# Response types

## Default

The default response type is a key/value pairs, separated by newlines:

```javascript
name : Basispakket
description : WebTV content voor TV Basispakket
```
Example url: https://webtv-api.xs4all.nl/2/listpackages

## JSON

```
[{"name":"Basispakket","description":"WebTV content voor TV Basispakket"}]
```

keyword: json   
Example url: https://webtv-api.xs4all.nl/2/listpackages.json

## JSONP

```
callbackfunction([{"name":"Basispakket","description":"WebTV content voor TV Basispakket"}])
```

Keyword: jsonp   
Extra querystring parameter needed: callback=[desired javascript function]   
Example url: https://webtv-api.xs4all.nl/2/listpackages.jsonp?callback=mycallbackfunction

# To do:
* What is the purpose of the underscore querystring parameter which is being used by the webtv app?
