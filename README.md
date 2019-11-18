# Smart Wait Example Project
A smart waiting function has introduced in Katalon Studio version 7. The Smart Wait will tell the WebDriver to wait for the web page to become static before any operations perform.<br>
You can read the document and see more details [here](https://docs.katalon.com/katalon-studio/docs/webui-smartwait.html).

## Discussion/Support
Join the Katalon Community / Forum if there are things you want to discuss https://forum.katalon.com/

## Apply Smart Wait to all elements in a project
To enable the Smart Wait function for the whole project in Katalon Studio, navigate to Project > Settings > Execution > Select ***Enable*** in Default Smart Wait.

## Apply Smart Wait to specific elements in a script
If you want to use Smart Wait function for certain test elements only, it's important that you ***disable*** Default Smart Wait in Project Settings. Navigate to Project > Settings > Execution> Select ***Disable*** in Default Smart Wait.
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

### Example:
```java
WebUI.openBrowser('')

WebUI.navigateToUrl('https://demo.tutorialzine.com/2009/09/simple-ajax-website-jquery/demo.html')

'Enable the Smart Wait function when it\'s disabled by default in project settings.'
WebUI.enableSmartWait()

WebUI.click(findTestObject('Page_AjaxDemo/a_Page 1'))

WebUI.verifyTextPresent('Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam feugiat neque vel metus sodales auctor sed et arcu. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Phasellus cursus tellus ac urna sollicitudin viverra.', 
    false)

'Disable the Smart Wait function when it\'s enabled by using the above keyword.'
WebUI.disableSmartWait()

WebUI.closeBrowser()
```

> Note: The Smart Wait function is only available in Chrome and Firefox.
