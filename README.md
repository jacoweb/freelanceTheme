freelanceTheme
==============

Freelance Theme by startbootstrap.com modified for OctoberCMS by jacoweb

Contact email
---
While the basic scaffolding required for emailing has been built in, 
there are some backend settings that need to be made to get it working:

1. Make sure you have your mail driver setup correctly in your config file (https://octobercms.com/docs/services/mail)
2. Under "Backend"->"settings"->"Mail Configuration", set your server settings. For ex. if you are using Mailgun API

```
SenderName: My OctoberCMS Contact
SenderEmail: my_actual_email_address@domain.com
MailMethod:Mailgun
Mailgun domain: provider.mailgun.com
Mailgun Secret: key-yourrealmailgunsecretkey
```

3 . Under "Backend"->"settings"->"Mail Templates", click on create a "New Template"

```
Layout:System
Code: freelance::mail.contact
Subject: New Contact Message From Blog
Description: New Contact Message From Blog
html:
Greetings! <br/> 
You have a new contact from your OctoberCMS site. 
Here are the details: <br/><br/>
    
Name: {{name}} <br/>
Email: {{email}}<br/>
Phone: {{phone}}<br/>
Message: {{msg}}<br/>

<br/><br/>
Thanks!
```
Enjoy!
