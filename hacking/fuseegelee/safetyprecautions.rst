.. Homebrew Guide documentation master file, created by
   sphinx-quickstart on Sun Jan 13 23:22:33 2019.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Safety Precautions (fusee-gelee)
================================

You are now able to run Hekate on your Nintendo Switch to launch the Atmosphere custom firmware. These next steps will make sure you're being as careful as possible in regards to keeping your Switch from bricking and getting banned. These steps are optional but highly recommended.

.. note:: 
   If something goes wrong or you need help, check `troubleshooting </troubleshooting.html>`_.
   
........
   
Step 1: Backing up your NAND and BIS keys
-----------------------------------------

By backing up your NAND (the Switch's internal memory), you will later be able to restore it in the event that anything goes wrong, essentially rewinding it back to a previous state. BIS keys are also good to backup so you can reinstall any firmware version manually should your NAND backup become corrupted or lost.

1. Enter RCM and send the Hekate payload provided in the SDSetup download to your Switch (refer to `Section 1: Accessing RCM </gettingstarted/checkingrcm.html#step-1-accessing-rcm>`_ for instructions about sending the Hekate payload)
2. In Hekate, select **'Tools > Backup eMMC > eMMC BOOT0 & BOOT1'**
3. When finished, remove your SD card (you don't need to shutdown Hekate), insert it into your PC, and copy the 'backup' folder to a safe location on your PC. Afterwards, delete the 'backup' folder on your SD card.
4. Insert your SD card back into your Switch
5. In Hekate, select **'Tools > Backup eMMC > eMMC RAW GPP'**

    * If your SD card has less than ~32GB free space, Hekate will provide additional instructions every few minutes about pulling files off of your SD card so it can continue.

6. If you weren't required to copy files during the backup process, once again copy the 'backup' folder off of your SD card and put it in a safe location on your PC. Delete the 'backup' folder on your SD card.
7. Close the Backup menu, go back to the Home tab and tap **'Reboot > RCM'**
8. Send the **"Lockpick_RCM.bin"** payload provided in the SDSetup download to your Switch (if you do not have this payload, you can obtain it `from GitHub <https://github.com/Decscots/Lockpick_RCM/releases>`_).
9. Select `Dump from SysNAND` and press Power to confirm; press again Power when finished to go back to the Lockpick menu
10. Select poweroff from the menu once finished.
11. Insert your SD card into your PC.
12. Copy the **/switch/prod.keys** file to a safe location.

.. warning::
    It is highly recommended that you store these backups and keys in multiple locations (ex. cloud storage, external harddrive, etc) as they may be critical to restoring your Switch if anything goes wrong in the future.

........

Step 2: (EU Only) Enabling GDPR Protections
--------------------------------------------

Users with EU Nintendo Network accounts have the option of enabling GDPR protections in their account settings. Doing so has been confirmed to disable lots of telemetry that can get you banned. This setting will not appear if your account is not from the EU.

1. Go to https://accounts.nintendo.com/setting
2. Login with your NNID
3. Under **'Other settings'**, Edit **'Usage information'** and set it to **'Don't share'**
4. Save your changes

........


.. raw:: html

	<div class="admonition warning">
		<p class="last">Continue to <a href="/hacking/fuseegelee/aftersetup">After Setup (fusee-gelee)</a></p>
	</div>

.. toctree::
   :maxdepth: 2
   :caption: Contents:
