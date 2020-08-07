# driverConfig
Running Selenium with certain browser settings.

This project is about runnung Selenium with browser settings. 

Firstly, let's create firefox profile (close current if open).
For that: go to terminal and write firefox -P

Then create new profile and make some settings. For example i did some installations of addons like adblock. whatever.

Then go to your firefox directory and find your profile, then copy it to ur project directory and delete cash name at the beginning. 

Then in ur project folder open terminal and create package.json by writing:
```
npm init
```

Then write code . in terminal and create index.js file.
Create new terminal and install selenium by typing:

```
npm install selenium-webdriver
```

Put in the following script (it should work):
(at the like options.setProfile("./") write the name of your firefox profile name, mine is SeleniumTutorial)

```
const { Builder } = require("selenium-webdriver");
const firefox = require("selenium-webdriver/firefox");
const options = new firefox.Options();

options.setProfile("./SeleniumTutorial");

const driver = new Builder().forBrowser("firefox").setFirefoxOptions(options).build();

driver.get("http://google.com");
```

Then run the script by writing 
```
node index
```


