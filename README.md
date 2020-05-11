# Phone2PPT
Send pictures from the phone directly to a slide in PPT

Spent some of my free time in the weekend doing an addin for Powerpoint to transfer a photo from my phone to a powerpoint slide. Without copy and paste, onedrive, email, etc.

 

The story goes like this: 
- Using the addin the user adds a QRCode on powerpoint- Points at it with the phone. The phone recognizes the qrcode (it's pointing to a webpage)
- User Points at it with the phone. The phone recognizes the qrcode and User uploads the photo from the phone.
- The photo appears automagically in the powerpoint.

In an image:
![image](docs/all.png)

## Steps to run

Deploy website in Azure Storage:

- Create Azure Storage Account
- Create a SAS for the container
- on imageupload.html fill *accountName*, *sasString* and *containername*
- Copy the content of HTMLStorage to a public container

Change the addin

- Point the addin to the Azure Storage Website and upload container, line 1 of PhotoAdd/src/taskpane/taskpane.js. Change content of BACKENDURL and BACKENDFOLDER vars.

Run

In the addin folder start the addin by doing: npm start

Note: QRCode source dropped in for easiness 