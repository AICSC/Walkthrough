# Installing MinGW on Windows

<img src="../images/mingw-website.png" alt="MinGW website" width="640" height="324" />

Go to [MinGW.org](http://mingw.org/) and click the "**Download Installer**"
button in the top right corner.

![Download Installer button](../images/mingw-download-installer.png)

You will be redirected to **SourceForge.net**, where the download will begin
automatically after a few seconds.

![MinGW in Chrome's downloads toolbar](../images/mingw-download-toolbar.png)

When the download completes, run the installer by either clicking the button in
your browser's downloads toolbar, or navigating to your downloads folder and
double-clicking the installer. The downloaded executable should be named
`mingw-get-setup.exe`


![MinGW Installer's welcome screen](../images/mingw-installer-welcome.png)

The installer will present you with a welcome screen. Click the **Install**
button at the bottom of this window.

![MinGW Installer options](../images/mingw-download-options.png)

The installer will present you with some options; the defaults are acceptable.
Click **Continue** to begin installation.

![MinGW Installer finished downloading](../images/mingw-installer-finished.png)

After the installer has finished downloading and installing the required
components, click **Continue** to start the **MinGW Installation Manager**

Now that we have **MinGW** installed, we must actually install the packages that
we wish to use with **MinGW**

![Mark for Installation](../images/mingw-manager-mark.png)

To tell **MinGW** that we want a particular package installed, we click on the
corresponding checkbox and select **Mark for Installation**

![MinGW is ready to install the selected packages](../images/mingw-manager-ready-to-install.png)

We will install:
 * `mingw32-base`
 * `mingw32-gcc-g++`
 * `msys-base`

![Apply Changes](../images/mingw-manager-apply-changes.png)

After all required packages have been marked for installation, from the **Installation** dropdown menu, select **Apply Changes**

![Pending Changes](../images/mingw-manager-pending.png)

This will bring up a window listing all pending changes. Click the **Apply**
button to begin downloading and installing the selected packages.

![MinGW Installation Manager finished(finally)](../images/mingw-manager-finished.png)

Once the Installation Manager has finished installing the selected packages,
click the **Close** button.

The packages have now been installed but, before they can be used, the system's
`PATH` needs to be set to point to **MinGW**

# Setting the System's `PATH`

![System button in Windows 8.1 Control Panel](../images/win8-control-panel-system.png)

Open the Control Panel and click the **System** button

![System panel in Windows 8.1 Control Panel](../images/win8-control-panel-system-panel.png)

Click the **Advanced system settings** link in the left sidebar

![Advanced System Properties in Windows 8.1](../images/win8-system-properties-advanced.png)

Click the **Environment Variables** button at the bottom of the window

![Environment Variables in Windows 8.1](../images/win8-env-vars.png)

The the **System variables** pane in the bottom of the window, scroll to the
**`Path`** variable. Select it, and click the **Edit&hellip;** button

![Editing a system variable in Windows 8.1](../images/win8-edit-system-variable.png)

Position your cursor at the very end of the **Variable value** text field, and
type `;C:\MinGW\bin\;C:\MinGW\msys\1.0\bin\`

Click **Ok**

![GCC has been installed successfully](../images/win8-cmd-gcc-version.png)

To verify that **MinGW** has been installed and the **`Path`** has been set
correctly, open **`Cmd`** and enter `gcc -v`

You should see **GCC** print some diagnostic information.
