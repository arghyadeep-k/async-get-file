# Download files with Promise (node.js)

[![npm version](https://badge.fury.io/js/async-get-file.svg)](https://badge.fury.io/js/async-get-file)

A wrapper around download-file package to make it return a promise.

## Installation

[![NPM](https://nodei.co/npm/async-get-file.png)](https://nodei.co/npm/async-get-file/)

## Basic Usage

```javascript
const async = require("async");
const get = require("async-get-file);

async function main(){
  var url = "http://i.imgur.com/G9bDaPH.jpg";
  var options = {
    directory: "./images/cats/",
    filename: "cat.gif"
  }
  await get(url,options);
}

main();
```

OR

```javascript
const Promise = require("promise");
const get = require("async-get-file);

var url = "http://i.imgur.com/G9bDaPH.jpg";
var options = {
  directory: "./images/cats/",
  filename: "cat.gif"
  }

get(url,options)
.catch(err => {
      console.log(err);
      });
```

## API

get(url, [options])

- url string of the file URL to download

- options object with options

  - directory string with path to directory where to save files (default: current working directory)
  - filename string for the name of the file to be saved as (default: filename in the url)
  - timeout integer of how long in ms to wait while downloading (default: 20000)

---

## References

- <https://stackoverflow.com/a/38428075/9647762>

## License

async-get-file is published under the MIT license. For more information, see the accompanying LICENSE file.
