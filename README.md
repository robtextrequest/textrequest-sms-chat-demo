# Text Request SMS Chat Demo

Text Request's SMS Chat widget is an excellent way to generate inbound leads from your website. Engagement is substantially higher than email and contact forms. Information on the SMS Chat widget [can be found here](https://www.textrequest.com/queuniversity/sms-chat/). You can sign up for a Text Request account [here](https://www.textrequest.com). 

## Opening and Closing SMS Chat via JavaScript

If you prefer to toggle the SMS Chat open and closed using your own custom button, you can do that. The steps to do so are:

* Go to your SMS Chat settings within Text Request, and uncheck the boxes for "Show on Desktop" and "Show on Mobile". This will hide the SMS Chat button that floats in the lower right-hand corner. This step is optional. 

* You'll need to place the following JavaScript snippet anywhere between your <head></head> tags.
```
<script>
   var chatApi = {};
   openWindow = function () { chatApi.openChatWindow(); };
   closeWindow = function () { chatApi.closeChatWindow(); };
</script>
```

* Finally, add your Text Request SMS Chat JavaScript snippet just before the closing </body> tag. You can find this script on the SMS Chat settings page, located under the Integrations menu option in your Text Request account. 
```
<txr-sms-chat api="{chatApi}" accountid="Your Text Request account ID" chatid="Your Text Request chat ID"></txr-sms-chat>
<script type="text/javascript" src="https://fs.textrequest.com/sms-chat/main.bundle.js"></script>
```

Take a look at the openAndCloseChat.html demo page to see an example implementation. 
