Steps to create apk application from PWA application.

1. You must be familiar with the fundamentals of HTML, CSS, and JavaScript to use PWA.
2. Make a standard website that is responsive to mobile screens.
3. Keep images, css and javascript in separate folder and html file in root directory.
4. Create a number of icons in the following resolutions under the images folder. These symbols of various sizes are used to show
symbol on several gadgets.
	- 128x128
	- 144x144
	- 152x152
	- 192x192
	- 384x384
	- 512x512
	- 72x72
	- 96x96
5. In the root directory, create a file named "manifest.json" that provides details about our application.
You can use my file with few changes like name, color, and icons file names.
6. Now make a new file called "sw.js," a service worker that enables quick loading (regardless of the network),
Push alerts, offline accessibility, and more features. You must set that up in a registry in order for it to function.
Include a separate javascript file in our index.html file. I did it in the "app.js" file located in the "js" folder.
7. Therefore, when you launch the programme for the first time, it registers the service worker, install it, and then activates it.
it. However, if you run the programme again, the service worker will already be installed and won't need to be activated.
However, it will be reinstalled if you make any modifications to the service worker. however, maintains it in the waiting state. i.e.
not turning it on. To activate the service worker, first unregister it under the "application" tab in developer mode.
8. Using the fetch event in our service worker, we can utilise our application to operate offline.
send our own cached answer after retrieving the server's request from the client.
9. At the service worker's install event, you may add cache files, and at the fetch event, you can look for those assets.
if they are located in caches, return them. However, if you alter such cache files, it will get the previous versions of those items from
cache. To prevent this, we produce many iterations of those files so that they load fresh copies throughout the installation event of
service worker, and erasing previous caches while the service worker is active.
10. Now will upload it to firebase. I have hosted this application on https://wissen-technology-pwa.web.app/
11. Go to "pwabuilder.com" and paste the url to generate the apk file. I have loaded the apk file into this file directory.