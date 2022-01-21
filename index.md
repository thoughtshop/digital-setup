# Digital interactive Installations

Last Updated: 27 July 2021

---

## Prerequisites
- OSX 10.12 Sierra ([check LogMeIn requirements here](https://documentation.logmein.com/webhelp/EN/LogMeInGetStart/LogMeIn/c_lmi_systemrequirements_host.html) )

## Installation Checklist

### A - User Setup
1. Create a new user. Username and password is generally the client name for each. I.e. if the client is Polygon, username/password is polygon/polygon. **User must be an administrator.**
2. If there are other users, delete them.

### B - Configure System Preferences
1. `Login Options > Automatic login`, set user to automatically login
2. `Desktop & Screen Saver > Screen Saver`, turn off screensaver. For Mac, set **Start after** to “never”.
3. `Security & Privacy > General`, turn off **Require password...after screen saver begins**
4. `Notifications > Do not Disturb`. Set do not disturb to turn on between 7am and 10pm
5. `Notifications` Set all notifications to none and turn off sounds and banners. 
6. `Software Update`, turn off  **Automatically keep my Mac up to date**.
7. `Bluetooth > Advanced`, turn off **Open Bluetooth Setup Assistant at startup** for both keyboard and mouse/trackpad.
8. `Sharing`, turn on Screen Sharing. I use this as a backup in case one computer (in a multiple computer setup) is on LogMeIn, but another is not. 
9. `Sharing` Update computer name:
>  Our standard naming protocol is "[Development Name] Digital [Device Number]" so for the first computer for Richmond Centre you'd get: "Richmond Centre Digital 1"
10. `Energy Saver` (or `Battery > Power Adapter` as of macOS11)
  10.1. Set **Turn display off after** to Never
  10.2. Disable **Put hard disks to sleep when possible**
  10.3. Enable **Start up automatically after a power failure**

### C- LogMeIn Setup
1. Install LogMeIn. Go to [LogMeIn.com](https://logmein.com) using our account (in LastPass). Follow all the prompts and grant all permissions to install
2. `LogMeIn Control Panel > Options > Preferences and Security`
  2.1 Disable **Lock when connection has been lost** 
  2.2 Disable **Lock when connection has been timed out**	

### D - Add Startup Apple  Script
1. Install [Google Chrome](https://www.google.com/intl/en_ca/chrome/)
2. Open Script Editor and paste and edit one of these scripts (Chrome preferred, safari should only be used as a fallback):
	2.1 For Chrome: https://gist.github.com/coreylowe/ea179e0b98180243ccfbecbea3bf809c
	2.2 For Safari: https://gist.github.com/coreylowe/8aa26c45d8692310808e5c14a8aa0d62
3. Update the `[url]` placeholder in the script
4. If using Chrome, under `View`, disable the **Always show toolbar in fullscreen** option
5. Export as an Application, to the `~/Documents` folder.
6. Open the Application you just created 
7. Add the new application to the Dock
8. Add the new application to `System Preferences > Users & Groups`, under the current user’s Login Items. Alternatively, right click the application on the dock and select **Open at Login**

---
## Tests
- Turn off the wifi (in devtools or manually) and hit refresh to make sure the web app still functions properly offline.
- Soft Restart the computer to make sure the web app starts automatically.
- On another computer, check that the LogMeIn connection is initialized post restart
- Pull the plug (literally) and plug in back in to verify that everything is operational in the case of a power failure.


## Deployment
- Label the computer with masking tape or a sticky note
- Include the computer name, username and password
- In the case of multiple computers, make sure you add a count somewhere (i.e. 1 of 2) 
- Ensure a working power cable is included

---

## Troubleshooting and Tips
- If you don't have the password for the account on the computer, boot into recovery mode (`CMD + R`), open the terminal `Utilities > Terminal` and use the `resetpassword` command. 
- If LogMeIn isn't initializing properly after restarts, first check that it's listed as a login item and next check if it's been granted all the necessary permissions. If all else fails, reinstall. 
- If the computers are from Pure Image, their default password is `PureImage1`
- Updating the OS can take a couple of hours depending on the condition of the computer. Make sure you do this before anything else.
- Touchscreens usually require both a display cable and a usb connected. If you're not seeing any feedback at all, you've probably forgotten to plug in the usb.
- You may need to install [Touch Base](https://www.touch-base.com/) if the touchscreens aren't working as expected (eg. you press on the top left corner and the feedback is seen on the bottom left ).
