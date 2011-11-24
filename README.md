NWTestFlightUploader
=============

Script to prepare and upload your builds directly from Xcode4 to TestFlight, at the end of a scheme like Archive.
It provides a sequence of AppleScript dialogs to let you fill in the details of your build, like:

* Signing identity & provisioning profile
* Release notes
* Selection of distribution list(s)

How-to
-------

* Edit the Scheme of your product in Xcode4
* Expand the "Archive" scheme
* Click "Post-actions"
* Add a "New Run Script Action"
* Select the target that corresponds to the Scheme in the "Provide build settings from..." dropdown
* Copy & paste the contents of `NWTestFlightUploader.sh` into the text field
* At minimum, supply `API_TOKEN` and `TEAM_TOKEN` (use the URLs to look them up in your TestFlight dashboard)
* Done! To try it out, build the Archive scheme. At the end of the process the TestFlight upload 'wizard' will start.

![Xcode4 Scheme Editor - Adding TestFlight integration script](https://github.com/noodlewerk/NWTestFlightUploader/blob/master/how-to-screenshot.png "Xcode4 TestFlight Integration Script")