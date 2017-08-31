# Polymer 2 components to work with Service Workers

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/morbidick/serviceworker-helpers)
[![Build Status](https://travis-ci.org/morbidick/serviceworker-helpers.svg?branch=master)](https://travis-ci.org/morbidick/serviceworker-helpers)

## HowTo

### Register service worker

Since its more or less a one-liner to register your service worker and included in most boilerplates there is no specific element.

```html
<script>
  if ('serviceWorker' in navigator) {
    window.addEventListener('load', function() {
      navigator.serviceWorker.register('/service-worker.js');
    });
  }
</script>
```

### \<sw-update-toast\>

Displays a toast requesting the user to reload the page when a source code update is available.

The update message can be overwriten by setting `message` (optional). The display time can be changed by setting `duration`, defaults to 0 / persistend.

```html
<link rel="import" href="serviceworker-helpers/sw-update-toast.html">

<sw-update-toast
  message="My message"
  duration="5"
></sw-update-toast>
```

Change the link color by setting the css var `--primary-color`.

## Development

```bash
# Get dependencies
$ npm install

# Demo site
$ npm start

# Run tests
$ npm test
```
