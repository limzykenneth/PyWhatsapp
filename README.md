# PyWhatsapp
[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://github.com/shauryauppal/PyWhatsapp)  [![License](https://img.shields.io/github/license/shauryauppal/PyWhatsapp.svg)](https://github.com/shauryauppal/PyWhatsapp/blob/master/LICENSE) [![GitHub stars](https://img.shields.io/github/stars/shauryauppal/PyWhatsapp.svg)](https://github.com/shauryauppal/PyWhatsapp/stargazers)  [![HitCount](http://hits.dwyl.io/shauryauppal/PyWhatsapp.svg)](http://hits.dwyl.io/shauryauppal/PyWhatsapp)

## Python Automation using Selenium &amp; Scheduling of messages and media

## Objective:
Pywhatsapp is used to Automate Whatsapp through Whatsapp web. We can
add number of contacts whom we want to send messages or Media
attachments ( like Video or Images). Selenium, Autoit, AppleScript and Schedule is used for automation and scheduling messages.

---

## Use Case:
We can schedule Good Morning or Good night messages with a nice Picture
at a particular time to our loved ones. We can set reminders. Suppose at
12 o'clock you want to wish your friend happy birthday so schedule your
messages and sleep peacefully.

---

## Installation

Uncomment the relevant module in `requirements.txt` for your platform

>$ pip install -r requirements.txt

OR

>$ pip install selenium
>
>$ pip install schedule
>

For Windows:
>$ pip install PyAutoIt

For macOS:
>$ pip install applescript

---

### ChromeDriver
Download and install the latest version from [Download Link](http://chromedriver.chromium.org/downloads), make sure ChromeDriver is available in your PATH.

[Set ChromeDriver Path in MacOS](https://stackoverflow.com/a/44870398/6897603)

Or you can install with your OS's package manager.

---
### For Sending Attachments

#### For Windows
You need to Install AutoIt:

You may install from the links given below or Install from the folder
named "Install AutoIt for Sending Attachments" in the repository.

[Official Website Download Webpage](https://www.autoitscript.com/site/autoit/downloads/)

[Installation Link of AutoIt.exe](https://www.autoitscript.com/cgi-bin/getfile.pl?autoit3/autoit-v3-setup.exe)

[AutoitScript Editor (optional to install)](https://www.autoitscript.com/cgi-bin/getfile.pl?../autoit3/scite/download/SciTE4AutoIt3.exe)

Installation is pretty Simple no changes in setting are required keep
everything default. Few clicks on Next and you are done.

#### For macOS
Make sure you have installed the relevant module. No additional steps required.

---

## Feature Enhancement:
QR CODE Scanning: On receiving a lot of complaints about QR Code Scanning Issue again and again. I have added a Cookie system that will save your session so that whatsapp don't think you are login for first time. By Saving Session data you will have to scan QR Code to Login only once or till the time whatsapp doesnot log you out from whatsappweb.

NOTE: A folder User_Data will be created which has all your session information. Keep this Folder VERY SAFE.

## Code:
### input_contacts()

In this functions Contacts list can be hardcoded or you can give input
accordingly.(Make changes in Contact array according to you)


```
1.Enter Saved Contact number->
2.Enter Unsaved Contact number->
Enter your choice(1 or 2):->1
# For saved Contacts
Enter number of Contacts to add(count)->1
Enter contact name(text)->Shaurya
# For unsaved Contacts
Enter number of unsaved Contacts to add(count)->1
Enter unsaved contact number with country code(interger)->919899123456
```

### NOTE: For unsaved contacts:
Do enter your country code then contact number.
>Use: 919899123456
>
>Don't Use: +919899123456



### input_message()
In this function we take input of message to send to all the Contacts
list from user.

Example:
>Enter the msg to send-> Good morning

### Enter choice to schedule message or not.
>Do you want to schedule your Message(yes/no): yes
>
>input time in 24 hour (HH:MM) format - 10:10

NOTE: If testing program for the first time Scheduling should be `no`
inorder to check it is working perfectly.

### Enter choice whether to send attachments or not.
>Would you like to send attachment(yes/no): yes
>
>Answer the input with yes or no.

### send_attachments()
NOTE: Add Photos & Videos in the Media Folder.

image_path = os.getcwd() +"\\Media\\" + 'goodmorning.jpg'

Example path to send goodmorning image to your listed Contacts.

*   "hour" variable is used to check current Hour on the clock and
according image is sent to the Contact.
*   If time is after 5am and before 11am schedule goodmorning.jpg image.
*   If time is after 9pm schedule goodnight image.
*   If time is anyother send howareyou image.

You can set your own photos at a particular time feel free to do that.

### send_files()
NOTE: Add the document in the documents folder.
>Would you file to send a Document file(yes/no): yes
>
>Enter the Document file name you want to send: opportunity

*   If the document file names are same then write the document name
with extension like opportunity.pdf or opportunity.txt


### Schedule messages and Attachments
schedule.every().Monday.at("06:00").do(sender)

schedule.every().Tuesday.at("07:00").do(sender)

schedule.every().Friday.at("07:30").do(sender)

schedule.every().day.at("08:30").do(sender)

*   You make change these schedule days and time according to you.

---

### Input Screenshot:
<img
src="https://raw.githubusercontent.com/shauryauppal/PyWhatsapp/master/Input_Type.PNG" height=300/>

---

### Demo of Working (GIF)
<img
src="https://raw.githubusercontent.com/shauryauppal/PyWhatsapp/master/Media/Demo.gif" height=400 width=400/>

---

## Contributions
<a href="https://github.com/shauryauppal/PyWhatsapp/issues"> Issues </a>
and <a href ="https://github.com/shauryauppal/PyWhatsapp/pulls"> Pull
requests </a> are most welcome.

---
## License
License
Code and documentation are available according to the Apache License
(see <a
href="https://github.com/shauryauppal/PyWhatsapp/blob/master/LICENSE">LICENSE</a>).

---

## Author:
## <a href="https://www.linkedin.com/in/shaurya-uppal/">Shaurya Uppal</a>

shauryauppal00111@gmail.com

Feel free to mail me for any queries (After you have tried finding your
solution).

#### If this helped you in any way gift me a cup of coffee :coffee:
[![paypal](https://www.paypalobjects.com/en_US/i/btn/btn_donateCC_LG.gif)](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=UXSREFS2VFSWU)
