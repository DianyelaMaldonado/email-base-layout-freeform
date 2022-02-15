# Email Base Layout [Free Form] ✨
[![N|Solid](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/assets/BM-logo.png?raw=true)](https://heyblackmagic.com/)

Re-usable email template fully tested in:

- Apple Mail (Light/Dark)
- Outlook Office 365 (Light/Dark)
- Outlook 2016
- Outlook 2019
- Gmail App Android (Light/Dark)
- Gmail App iOs (Light/Dark)
- iPad (Retina)
- iPhone 11/12/12 mini/SE
- AOL Mail (Edge)
- Gmail (Chrome)
- Outlook (Chrome) (Light/Dark)
- Yahoo! Mail (Firefox)

## How to use in your awesome Craft CMS project:
### Templates:

You will find the email layout and the example FreeForm template within `templates` directory.

- Place the `email-templates` directory inside your templates directory.
- Place the `_email-layout.html` file inside your templates directory (`email-templates` directory and `_email-layout.html` file must be at the same level).
- Go to `/admin/freeform/settings/email-templates` to set up the templates path.
- Type `email-templates` as the template directory path.
- Click `Save`.
- The example **Contact Us** template will be shown below.

![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/template-directory-path.png?raw=true)

- Go to your Express form in `/admin/freeform/forms` to configure your form notification template.
- Click on your form name.
- At the top/right corner, click in the **Admin Notification** (![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/envelop-icon.png?raw=true) icon) and select the example **Contact Us** template.

![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/admin-notification-select.png?raw=true)

Don't forget to set up the admin recipients email addresses in the textarea below. It is recommended to use internal testing email addresses for testing purposes, your personal/blackmagic emails would be fine. NOTE: ON PROCUCTION ENVIRONMENT THESE EMAIL ADDRESSES WILL BE REPLACED WITH THE ONES OF THE CLIENT:

![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/testing-emails.png?raw=true)

### Template customization:

The email layout is ready to be customized through the CMS, **THIS IS NOT MANDATORY** but it would be more magical if you use it like this 🦯🎩✨

#### Fields
The template can have these custom elements:
- Logo
- Header background
- Body background
- Footer background

So we will need to create a field for each of them. So, go to `/admin/settings/fields` and create a new group of fields, I recommend to name it "Email layout" but you can use the name you prefer. Inside that group we will create these fields:

| Field Name | Handle | Type |
| ------ | ------ | ------ |
| Logo | logo | asset |
| Header Background Color | headerBgColor | color |
| Body Background Color | bodyBgColor | color |
| Footer Background Color | footerBgColor | color |

NOTE: In the Logo field description be sure to request an image in PNG/JPG format.

![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/fields.png?raw=true)

#### Globals

- Go to `/admin/settings/globals`, click on `New global set` and create a global called **Email Layout**, be sure the handle is `emailLayout`.
- Drag and drop all the fields you created previously to the global.
- Click `Save`.

![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/global.png?raw=true)

- Go to `/admin/globals/default/emailLayout` to customize your email basic elements.

![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/global-2.png?raw=true)

### Form submission
Whenever your FreeForm is submitted, the customized template will be sent:
![alt text](https://github.com/DianyelaMaldonado/email-base-layout-freeform/blob/development/src/screenshots/example-email.png?raw=true)

NOTE: If you test your form in your local environment, you will see a broken logo. Don´t worry, it will work fine when you deploy to a higher environment 🚀

-----
MAKING THE INTERNET A HAPPIER PLACE 💫
