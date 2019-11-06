# okta as IDP

Follow the Step-by-Step Guide for Jenkins Single Sign On(SSO)using Okta as IdP


Step 1: Create a new Application
Log into Okta Admin Console.
Navigate to the Application and click on the Add Application
Click on the SAML 2.0.

Step 2: Setting  SP metadata
In General  Settings, enter App Name and click on Next.
In SAML Settings, enter the following:


 
Single Sign-On URL
Root_URL/securityRealm/moSamlAuth
Audience URI(SP Entity ID)
Root_URL/securityRealm/moSamlAuth
Name ID Format
username
Application Username
Okta Username
Recipient URL and Destination URL
Root_URL
 
Step3: Configuring Attributes
Configure Attribute Statement as follows:
Add the username and email as an attribute.


Save the app settings.

Step4: Assigning Groups and People
After creating and configuring the app go to the Assignment Tab in Okta.
Here we select the people and groups you want to give access to login through this app. Assign this to the people/group you would like to give access to.


After assigning the people/groups to your app go to Sign On tab.
Click on view setup instructions to get the SAML Login URL (Single Sign on URL), Single Logout URL, IDP Entity ID, and X.509 Certificate.


Copy the required SAML Login URL (Single Sign on URL), Single Logout URL, IDP Entity ID, and X.509 Certificate.

Paste the above URL and certificate in respective field area of Jenkins  Miniorange Saml Plugin.