# wa-auto

Send automatic notification from R to your WhatsApp from Twilio API.

First, you need to sign up and create Twilio account. You will get ACCOUNT SID and AUTH TOKEN. You maybe need to copy and Save these auth to your local R project so R can send the notification.  

Then install the {twilio} package from R.

```
install.packages("twilio")
```

After install the package successfully, now you can activate the package.

```
library(twilio)
```

Before you send the messages, you need to specify the ACCOUNT SID and AUTH TOKEN first.

```
Sys.setenv(TWILIO_SID = "xxxx") # ACCOUNT SID
Sys.setenv(TWILIO_TOKEN = "xxxx") # AUTH TOKEN
```

Now, you can send messages to your registered WhatsApp number using this code.

```
message = tw_send_message( 
  from = 'whatsapp:+14155238886',  
  body = 'Your appointment is coming up on July 21 at 3PM',      
  to = 'whatsapp:+62857xxxxxxxx' 
) 
```
Check your WhatsApp chat! 
