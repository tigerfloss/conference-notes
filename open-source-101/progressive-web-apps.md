# Progressive Web Apps - What, Why, & How
Speaker: Jennifer Bland

## Requirements
### 1. HTTPS
### 2. Web App Manifest
```html
<link rel="Manifest" href="manifest.json">
```
#### Manifest.json
* `short_name` - name displayed on shortcut
* `display` - dfine the developer's preferred display mode for the web application (standalone|fullscreen)
* `backgground_color` - expected background color for the web application
* `theme_color` - default theme color for an application
* `icons` - an arrage of image objects that can serve as app icon sin various contexts
* `orientation` - can enforce a specific orientation
### 3. Service Worker
* Background script to serve network or cached content
* what distingueshes a PWA to HTML
#### Registration
```c++
if ('serviceworker' is navigator){
 window.addEventListener('load', function(){
  navigator.serviceWorker
...
```
#### Installation
#### Activation
#### Fetch

### 4. Responsive Design
* Can be installed on any device

#### [PWA Checklist][https://developers.google.com/web/progressive-web-apps/https://developers.google.com/web/progressive-web-apps/checklist]

#### PWA Performance
* Lighthouse


