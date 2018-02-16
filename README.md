Simple no-auth pull data from a Public Google Spreadsheet.
````
try {
  var gsheet = require('.');
} catch(e) {
  var gsheet = require('gsheet-web');
}

gsheet('1LEKra-mjOrJq7tG2JKU1pYclpDWKxTMnbgCpGZHBemY', (data)=>{
  console.log('Try callback ', data.length);  // array of objects
});

gsheet('1LEKra-mjOrJq7tG2JKU1pYclpDWKxTMnbgCpGZHBemY').then((data)=>{
  console.log('Try promise ', data.length);
});
````
Browser
````
<script src=https://rawgit.com/digplan/gsheet-web/master/gsheet-web-browser.js ></script>
<script>
  (async ()=>{
    var array = await gsheet('sheetid')
  })()
</script>
````
