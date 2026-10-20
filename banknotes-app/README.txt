AUSTRALIAN BANKNOTES APP (Year 2)
An offline explore tool for the Next Generation Australian banknotes.

WHAT'S IN THIS FOLDER
  index.html              The whole app, with all banknote images built in
  sw.js                   Saves the app on the iPad so it works with no internet
  manifest.webmanifest    App name and icon details
  icon-180.png, icon-512.png   Home screen icons

SETTING IT UP IN JAMF SCHOOL (for IT)
1. Upload the whole folder, as is, to any HTTPS web server (for example the
   school intranet). All files must sit together in the same folder.
   Example address: https://intranet.iswa.wa.edu.au/apps/banknotes/index.html

2. In Jamf School, go to Profiles and click + Create Profile.
   Choose iOS, then Device Enrollment, and give the profile a name.
   Open the Web Clips payload and fill in:
   - Label: Banknotes
   - URL: the full address of index.html
   - Icon: icon-180.png (an icon is required for iPad web clips)
   - Tick "Full Screen" so it opens as its own app, with no Safari address
     bar, search bar or tabs. (The app already includes the code iPadOS
     needs for this.)
   - If a "Removable" option is shown, untick it so students can't delete it.
   Use the Scope section to add the Year 2 iPad device group, then save.

3. Open the Web Clip once on each iPad while connected to Wi-Fi. This saves
   the app to the iPad. After that it works with Wi-Fi turned off.

4. To stop students leaving the app, a teacher can use Guided Access
   (Settings > Accessibility > Guided Access, then triple-click the top or
   home button while the app is open). Jamf School's Single App Mode locks
   to an app, and its help article doesn't mention web clips, so test before
   relying on it.

THE APP
- Contains no links to the internet and loads nothing from outside.
- "Read to me" uses the iPad's built-in voice (Australian English where
  available), so it works offline.
- Pinch zoom, text selection and long-press menus are turned off.

UPDATING
If the app is changed later, change CACHE = 'banknotes-v1' in sw.js to
'banknotes-v2' (and so on) before uploading, so the iPads pick up the new
version next time they open it online.

Images: specimen banknote images from the Reserve Bank of Australia.
Content adapted from banknotes.rba.gov.au.
