
<h1 align="center">shizzle 🔥</h1> 

<p align="center">
<a href="https://github.com/moolahdb"><img alt="author" src="https://img.shields.io/badge/author-moolah-yellow"/></a>
<a href="https://github.com/ellerbrock/open-source-badges/"><img alt="author" src="https://badgen.net/badge/Open%20Source%20%3F/Yes%21/blue?icon=github"/></a>
</p>

<hr>
<h3 align="center">
A Google Drive Index Running on Cloudflare Workers ❤️

Based on [panta js](https://github.com/Hidove/goindex) with magic change beautification.

App.js is based on [yanzai's js](https://github.com/yanzai/goindex) beautification, supports features such as multi-disk, search, pagination and call-to-external player, plus DPlayer playback.


### How to Use

 - Open [this](https://install.kenci.workers.dev/) website, verify and get the code.
 - Copy the obtained Client ID, Client Secret and refresh token into
   [index.js](https://github.com/sawankumar/GoIndex-Theme-Nexmoe/blob/master/index.js)
- Deploy index.js code to Cloudflare Workers


### Manual Method to generate Client ID, Client Secret and Refresh Token

* Open https://console.developers.google.com/apis/credentials
* After creating project or if you already have one.
* Click create credentials.
* Select OAuth client ID.
* Select Web application.
* Give it a name. (anything for your own reference)
* In Authorized JavaScript origins add https://developers.google.com
* In Authorized redirect URIs add https://developers.google.com/oauthplayground
* Save and note down your Client ID and Secret
* Open https://developers.google.com/oauthplayground
* On Right Top Side click on Setting Icon ![](https://developers.google.com/oauthplayground/assets/images/settings.png)
* Click on Use your own OAuth credentials.
* Enter OAuth Client ID: and OAuth Client secret:
* Now back to same page https://developers.google.com/oauthplayground left side Step 1 i.e. Select & authorize APIs
* Find Drive API v3
* Select First Option i.e. https://www.googleapis.com/auth/drive
* Click on Authorize API. and give permissions using your google account.
* It will turn to Step 2 Exchange authorization code for tokens at the end of authentication.
* Click on Exchange authorization code for tokens, if it goes to step 3, click on Step 2 yourself.
* Select the option Auto-refresh the token before it expires.
* Copy the refresh token and paste in Line 8 of https://github.com/kulokenci/goindex-drive/blob/master/worker.js along with your own Client ID and Secret at Line 6 and Line 7.
* Copy the Code and paste it into https://workers.cloudflare.com Site.


### Extra Options
``` js
const uiConfig = {
  .......
  "avatar": "",  // Changes the avatar image in the navbar
  "disable_navicon": true // Disables useless nav menu in navbar
  .......
};
```

##### *Thanks* :heart:   [5MayRain](https://github.com/5MayRain/goIndex-theme-nexmoe) 
