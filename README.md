# Smart Wait Example Project
Welcome to the Smart Wait Example Project repository!<br>
A smart waiting function is introduced in Katalon Studio version 7. The Smart Wait will tell the WebDriver to wait for the web page to become static before any operations perform.<br>
You can read the document and see more details [here](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html).

## Discussion/Support
Join the Katalon Comunity if there are things you want to discuss https://forum.katalon.com/

## Apply Smart Wait to all elements in a project
To enable the Smart Wait function for the whole project in Katalon Studio, navigate to ***Project > Settings > Execution > Select Enable in Default Smart Wait.***

## Apply Smart Wait to specific elements in a script
If you want to use Smart Wait function for certain test elements only, it's important that you ***disable*** Default Smart Wait in Project Settings. Navigate to ***Project > Settings > Execution> Select Disable in Default Smart Wait***.
Then use "enableSmartWait" and "disableSmartWait" keywords to enable and disable this function respectively.

### enableSmartWait
```
Keyword name: enableSmartWait
Description: Enable the Smart Wait function when it's disabled by default in project settings
```

### disableSmartWait
```
Keyword name: disableSmartWait
Description: Disable the Smart Wait function when it's enabled by using the above keyword
```

> Note: The Smart Wait function is only available in Chrome and Firefox.
