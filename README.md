# async-get-file : Download files with Promise (Node.js)

![CI](https://github.com/arghyadeep-k/async-get-file/workflows/CI/badge.svg?branch=master)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=arghyadeep-k_async-get-file&metric=alert_status)](https://sonarcloud.io/dashboard?id=arghyadeep-k_async-get-file)
![npm](https://img.shields.io/npm/v/async-get-file) 
![npm bundle size](https://img.shields.io/bundlephobia/min/async-get-file)
![Libraries.io SourceRank](https://img.shields.io/librariesio/sourcerank/npm/async-get-file)
![Depfu](https://img.shields.io/depfu/arghyadeep-k/async-get-file)
![Snyk Vulnerabilities for npm package](https://img.shields.io/snyk/vulnerabilities/npm/async-get-file)
![npm](https://img.shields.io/npm/dt/async-get-file) 
![NPM](https://img.shields.io/npm/l/async-get-file?color=blue)

This package is a wrapper around the [download-file](https://www.npmjs.com/package/download-file) package replacing callback functions with functions that return a Promise.

Basically it lets you write code like this
```javascript
await get(url,options);
console.log("Success");
```
instead of
```javascript
get(url, options, err => {
    if (err) throw err;
    console.log("Success");
}) 
```

## Installation

[![NPM](https://nodei.co/npm/async-get-file.png)](https://nodei.co/npm/async-get-file/)

**Install from command line:**

`npm install --save async-get-file`

Or

**Install via package.json:**

Add the following to your *package.json* file under dependencies

`"async-get-file": "1.0.2"`

## Basic Usage

```javascript
const async = require("async");
const get = require("async-get-file");

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

Or

```javascript
const Promise = require("promise");
const get = require("async-get-file");

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

<br>

## References
- <https://www.npmjs.com/package/download-file>
- <https://stackoverflow.com/a/38428075/9647762>

## License

async-get-file is published under the MIT license. For more information, see the accompanying LICENSE file.


<br>

---
<br>

### PS: 
If you find this package useful, please [star](https://github.com/arghyadeep-k/google-sheets-logger) the project on Github. 

And, if you are willing to [buy me a coffee](https://ko-fi.com/arghyadeep), that would be awesome. :)
