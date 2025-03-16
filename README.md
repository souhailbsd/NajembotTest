## Integrating Twilio with rasa
* Enable Whatsapp sandbox under Programmable SMS.[Here](https://www.twilio.com/console/sms/whatsapp/sandbox).
* Add Twilio channel to your RASA ```credentials.yml```.More info [here](https://rasa.com/docs/rasa/user-guide/connectors/twilio/).
* ```twilio:```
  ```account_sid: "<account_sid>"```
  ```auth_token: "<auth_token>"```
  ```twilio_number: "whatsapp:<TWILIO NUMBER>"```.
*  Launch your rasa instance.  use ngrok to get a public https URL for your bot instance. More info [Here](https://rasa.com/docs/rasa/user-guide/messaging-and-voice-channels/#testing-channels-on-your-local-machine-with-ngrok).
*  ```./ngrok http 5005;,rasa train, rasa run actions ,rasa run```.
* ```https://<your id>.ngrok.io/webhooks/facebook/webhook```
* Add your Rasa Twilio Webhook to [Sandbox configuration](https://www.twilio.com/console/sms/whatsapp/sandbox) put it on the POST and save.
* And also add webhook in the message callback [Here](https://www.twilio.com/console/phone-numbers/PNfab2e6125f58410c3e9ea6e4915f2c75)
* Finally follow the instruction to join the WhatsApp sandbox from your mobile number [Here](https://www.twilio.com/console/sms/whatsapp/learn).
* Now you have your RASA bot integrated with Whatsapp.