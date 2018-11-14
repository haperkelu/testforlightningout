# Inustructions

### 1) 
Create account list as per https://trailhead.salesforce.com/en/content/learn/projects/slds-lightning-components-workshop/slds-lc-4

Create below Lightning application in your Salesforce instance and name it as **LightningOutDemo**

`<aura:application access="Global" extends="ltng:outApp">`
`<c:AccountList />`
`</aura:application>`

### 2)
Create Connected App in your Salesforce instance with callback URL - `https://testforlightningout.herokuapp.com/oauthcallback.html`
Copy consumer key created in connected app and update clientId variable defined in [OAuth.js] file

Note: https://testforlightningout.herokuapp.com is my example and you'd need to use your own heroku Dyno

### 3)
Save `https://testforlightningout.herokuapp.com` in **CORS** setting of Salesforce.

### 4)
Deploy the code to heroku 

### 5)
Navigate to ttps://testforlightningout.herokuapp.com and you'd see Lightning Out!
