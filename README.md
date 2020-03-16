# Headless Scraper
This is an implementation of a headless scraper based on puppeteer

## Install
```
$ npm install
# or
$ yarn install
```

## Preparing configuration

create your own config file

`./config`
```js
const {scrollDown} = require('./lib/browserHelper')

module.exports = {
  name: `<yoururl>-${new Date().getTime()}`,
  url: 'https://<your-url>.com/',
  isDownloadResource: true,
  }
}

```


## Generate Report
```
$ node script/generateReport.js --meta='./1552988325707-temp/meta.json' --output='./1552988325707-temp/report.json'
```

## Getting cookies

```
const cookies = await page._client.send('Network.getAllCookies');
```
