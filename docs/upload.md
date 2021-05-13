# Uploading data to server
This section details how to to push any changes to the live version of the web portal.

## Remote login
Before accessing the site, users must either be at a UD IP address or remote login. To enable remote login follow the steps found here

<http://web.facilities.udel.edu/docs/technology/VPN.pdf>

Once these steps have been followed, open the Cisco AnyConnect Secure Mobility Client and log in using the user's UD credentials.
The user will need an authenticator passcode. You can download an authenticator from the app store on your phone

<https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2&hl=en_US&gl=US>

##WinSCP
The user will need to remote login to the portal. For windows, this can be done through WinSCP. Instructions on how to download WinSCP can be found here

<https://winscp.net/eng/index.php>

Once installed, open the WinSCP program. Fill out the forms in the following format:

**Host name**: webdav.www.udel.edu

**User name**: your UDel username, i.e. "marrs".

**Password**: your UDel password.

This should fill out the other forms, but if not put in:

**File Protocol**: WebDAV

**Encryption**: TLS/SSL Implicit encryption

**Port number**: 443

This will login to the folder housing all the web portal's files. All the HTML files displayed on the site are stored in the main directory.
To change a file, copy over the version on the local computer to the remote page. There is no need to navigate into any sub folders for changing the
transition rate, matrix element, other data, or index pages.

It is good practice before pushing large changes to save the old file before it is changed. There is an "archive" folder in the web portal directory that
can store these HTML pages.
