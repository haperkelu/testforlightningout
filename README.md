# Inustructions

### 1) Build Lightning Component in Salesforce
Create account list as per https://trailhead.salesforce.com/en/content/learn/projects/slds-lightning-components-workshop/slds-lc-4

Create below Lightning application in your Salesforce instance and name it as **LightningOutDemo**

`<aura:application access="Global" extends="ltng:outApp">`
`<c:AccountList />`
`</aura:application>`

### 2) Create connected app in Salesforce
Create Connected App in your Salesforce instance with callback URL - `https://testforlightningout.herokuapp.com/oauthcallback.html`

Copy consumer key created in connected app and update clientId variable defined in [/client/js/OAuth.js] file

Note: https://testforlightningout.herokuapp.com is my example and you'd need to use your own heroku Dyno

### 3) White list remote web container(external application) in Salesforce
Save `https://testforlightningout.herokuapp.com` in **CORS** setting of Salesforce.

### 4) Add lightning component to remote web container with a couple of lines of code 
Check out this repository and the code is in [/views/Main.html]

`<script src="https://testforlightningout-dev-ed.lightning.force.com/lightning/lightning.out.js"></script>`

`$Lightning.use(appName, function() {}, url, $.cookie("SFAccessToken"));`

`$Lightning.createComponent("c:AccountList", {type: type}, "placeholder"); `

### 5) Deploy
Navigate to ttps://testforlightningout.herokuapp.com and you'd see Lightning Out!
