# Cross Platform Visual Novel Setup 

This page will go over how to set up visual novels on all platforms.  

## Getting Visual Novels

Check out the [Resources](/resources/#the-following-may-be-nsfw) page to find where to get Visual novels.

Visual novels for Microsoft Windows are distributed commonly in disc image files. Usually in .ISO and sometimes .MDF/.MDS files, or, these files but contained in a .rar/.zip/.7z file.

!!! question "Glossary: disc image file"
	A disc image file does not refer to a picture of a disc, rather it is a file (usually `.iso`) that contains an exact copy of what was on a disc. Remember: Japanese visual novels are sold on optical discs, and then people make an exact copy of what is on the disc onto an `.iso` or `.mdf/.mds` file.

## Microsoft Windows

Visual novels are always Microsoft Windows applications. If you have a Windows PC, you will always be able to run visual novels as long as your visual novel supports the Windows version you are running. For most VNs out there, Windows 7 is a minimum, older titles will also work on XP. Newer titles released after 2019 will require Windows 8.1 as a minimum.  

### Step 1. Japanese Locale

Japanese visual novels will not run without Japanese locale. Some may run, but have limited functionality, audio, visuals and saving may not work. Japanese locale is the minimum requirement for running Japanese games on your Windows PC. You may use a locale emulator, though it is less of a hassle to just change system-wide locale in my opinion.  

**Follow the steps below to set Japanese locale on your Windows system.**  

!!! abstract "Setting Japanese locale"
	1. Open the Run dialog box using ++windows+r++
	2. Type `intl.cpl` and hit ++enter++
	3. Click on the *Administrative* tab, go to *Change System Locale* and select **Japanese (Japan)** and click OK.	
	4. Reboot your PC to apply the changes.

!!! question "FAQ: What about "Use Unicode UTF-8 for worldwide language support"?"
	Keep it disabled. This is a recent feature of Windows 10. We do not need it for VNs, it is unrelated, and may cause problems.   
	If you're curious: It sets CHCP 65001 in the registry.

??? tip "Advanced Users: Powershell"
	Japanese locale can also be enabled using **Windows Powershell (Administrator)**:
	```powershell
	Set-WinSystemLocale -SystemLocale ja-JP; Restart-Computer
	```  
	This will restart your PC.

### Step 2. Extracting archives and mounting images

Requirements:  
[Get 7-Zip](https://www.7-zip.org/)  
[Get WinCDEmu](https://wincdemu.sysprogs.org/download/)  

We will be using 2 pieces of software today, *7-Zip* which is a tool for making and extracting archives such as `.zip` , `.tar` and `.7z` files, and *WinCDEmu* which allows us to mount image files such as `.mds/.mdf`, `.iso`.  
	
If you have downloaded a visual novel, and it came in a .rar/.zip/.7z archive, you must extract it before you can mount the installation files. You can use 7-Zip for this. 

> Right click the archive > 7-Zip > Extract to %folder%

![Image](img/vnwin1.jpg)

Above is an example of extracting the archive using 7-Zip.  

After the archive has been extracted, we will now use WinCDEmu to mount the image that has been extracted from it.  

> Right click the image > Select drive letter & mount > OK

![Image](img/vnwin2.jpg)  

After that,

![Image](img/vnwin3.jpg)  

The disc image is now mounted. You should see a new volume appear on your Explorer sidebar.

![Image](img/vnwin4.jpg)  

!!! info ".MDS/.MDF files"
	It is a little different if you have .MDS/.MDF files, see below.  

![Image](img/vnwin5.jpg)

### Step 3. Installing the VN and applying patch

Click on the new volume that appeared on your sidebar and run the installer. See below for details.  

![Image](img/vnwin6.jpg)  

Proceed with the installation, you may want to take note of where you installed the game. I installed Angel Beats! into `D:\Games\KEY\AngelBeats!`

If your visual novel came with a crack, you will need to apply this crack before you are able to launch the game. Cracks often come in the form of a .exe/.dll file found in folders/archives called "AlphaROM" or  "NoDVD" or simply just "Patch" or "Crack", whatever it may be, copy these files into the installation directory of the game.  

You can find an example below. Sorry for the "awkward" cursor placement, it happens in the recording for some reason.  

![Image](img/vnwin7.gif)  

After that, you should just be able to launch the game! 

Now go back to [Visual Novel Guide](https://learnjapanese.moe/vn/#looking-up-words-in-vns-using-yomichan-and-textractor) to learn how to use Textractor with Yomichan.

### Steam Games

If you obtained your visual novel from Steam, first check if "Japanese" is listed as a supported Interface and Subtitles language on the store page first. You can then set Japanese language within the Steam client itself.  

1. Open your Steam Library.
2. From a game's library page, select Manage > Properties.
3. Go to the Language tab.
3. Select Japanese from the drop-down menu.

In other cases, the game language can be set within the game itself.  

If you did not purchase the **Steam game** from Steam (i.e. a cracked game) you can edit the `steam_api.ini` file within the game's installation directory.  
```txt
language=japanese
```

### Windows: Troubleshooting

!!! info "Please insert original disc オリジナルディスクを入れてください"
	Make sure you have applied the crack/patch. Some VNs require the original disc inserted at least once before it will launch. In that case, use WinCDEmu to mount the .ISO or .MDS as a DVD drive. If the problem persists, try restarting your PC.
!!! tip "No Crack?"
	If there is no crack available for your VN, and your VN does not launch, use [AlphaROMdiE](https://cdn.discordapp.com/attachments/813105334763126814/813105570567159898/AlphaROMdiE-Build20140214.zip). See pictures within .zip file for instructions.
!!! info "Direct3D, Visual C++ Related Issues" 
	This can be easily fixed by installing DirectX [here](https://www.microsoft.com/en-us/Download/confirmation.aspx?id=35) and all the Visual C++ Redistributable Runtimes [here](https://www.techpowerup.com/download/visual-c-redistributable-runtime-package-all-in-one/).  
!!! info "Garbled Text (文字化け)"  
	Solution 1: Check [Japanese locale](#step-1-setting-japanese-locale) and restart your PC.  
	Solution 2: Install Japanese fonts. Download [this .zip file](https://drive.google.com/file/d/1OiBgAmt3vPRu08gPpxFfzrtDgarBGszK/view?usp=drivesdk). Extract, ++ctrl+a++(select all), Right click, Install, check "Do this for all current items", then Yes.  
!!! info "Japan Time Zone Required"
	Check Japanese locale and make sure all patch(es)/crack(s) are applied. If the problem persists, do the following: ++windows+i++ > Time & Language > "Set time zone automatically" OFF > Time zone: (UTC+9:00 Osaka, Sapporo, Tokyo)
!!! info "This Game is Japan Only!"
	Check Japanese locale and ensure a crack/patch is applied, if there is no crack available try using [AlphaROMdiE](https://cdn.discordapp.com/attachments/813105334763126814/813105570567159898/AlphaROMdiE-Build20140214.zip). Or even, the Rewrite Gaijin Check Patcher, you can get that [here](https://cdn.discordapp.com/attachments/813105334763126814/825474730797563914/Rewrite_Oka-ken_Gaijin-check_Patcher.exe). It's made for KEY's Rewrite but I've had success with it on other VNs too.
!!! info "Cutscenes and video not working"
	First, check if you are not using an N or KN edition of Windows. You can do that buy doing ++windows+r++ and typing `winver` and hit ++enter++. There you will see your Windows version and edition. If you *are* using an N edition, then you need to get the Media feature pack from Microsoft [here](https://www.microsoft.com/en-gb/download/details.aspx?id=48231).   
	If you are not using a N or KN edition of Windows, then make sure the game files are installed correctly, try reinstalling the game. If the problem persists, maybe try installing [ffdshow](https://sourceforge.net/projects/ffdshow-tryout/files/SVN%20builds%20by%20clsid/generic%20builds/ffdshow_rev4532_20140717_clsid.exe/download) and [LAVFilters](https://github.com/Nevcairiel/LAVFilters/releases/download/0.74.1/LAVFilters-0.74.1-Installer.exe)  
!!! info "Legacy Visual Novels"
	If your visual novel is particularly old and does not work with recent versions of Windows, you can try using a [Windows XP Virtual Machine](#windows-xp-virtual-machine)  
!!! bug "Rare error: Boot failure 0xc000000f"  
	This is an issue that happens after locale settings are changed on a system that is missing NLS (National Language Support) files. If this happens to you, then it is likely you were using a **unofficial modified copy of Windows**. See [this article](https://support.microsoft.com/en-us/windows/about-genuine-windows-0b88ba3d-f799-7c15-9f36-2be445a56493) to check. You can restore NLS files on your Windows system with the archive I made [here](https://drive.google.com/file/d/1qk6T7pzwn-Nl9JaEJD8G3Amuxl8oG1vS/view?usp=sharing).  
	However I recommend checking the [Microsoft Software Download Center](https://www.microsoft.com/en-us/software-download/) for getting clean disc images for Windows. If you need to restore your system, insert a Windows recovery media and restore from a restore point.  

## macOS

Visual novels are only Microsoft Windows applications, therefore if you want to run a visual novel on your Mac you must either virtualize/dual boot Windows or use *Wine*.

### Virtual Machines (10.11 - 11.x)

It is usually best to use a Virtual Machine of Microsoft Windows 7, as it works on newer Macs and does not have a hacky setup like Wine. Why not Windows 10? Simply because 10 is not necessary for Visual Novels and is also bloated.  

Search on Google for how to run a Windows virtual machine on your Mac using Parallels (paid) or VirtualBox (free). I do not own an actual Mac, so I can't provide instructions on how to do this. Fortunately this isn't VN specific, and you can just find instructions everywhere on Google.    
Contact me on Discord if you need help with getting either a Windows XP, 7 or 10 ISO.  

### Boot Camp Assistant (Intel® based Macs)

You can check if your Mac is an Intel® based Mac by doing the following command in Terminal:
```bash
sysctl -n machdep.cpu.brand_string 
```

All Intel® based Macs are able to run Microsoft Windows, with the exception of Macs that predate 2007.   
If your Mac supports it, I recommend you run Windows 7 instead of Windows 10.  

**Macs that support Windows 7:**  

Any Intel® based Mac that predates 2014. (With the exception of 2013 Mac Pro)

**Macs that support Windows 10:**

Intel® based MacBook introduced in 2015 or later   
Intel® based MacBook Air introduced in 2012 or later  
Intel® based MacBook Pro introduced in 2012 or later   
Intel® based Mac mini introduced in 2012 or later   
Intel® based iMac introduced in 2012 or later  
Intel® based iMac Pro (all models)    
Intel® based Mac Pro introduced in 2013 or later     

Search on Google for how to use Boot Camp on your Mac. I do not own an actual Mac, so I can't provide instructions on how to do this. Fortunately this isn't VN specific, and you can just find instructions everywhere on Google.
Contact me on Discord if you need help with getting either a Windows 7 or 10 ISO.  

### PlayOnMac (10.5-11.x)

PlayOnMac uses the Wine compatibility layer which allows you to run Windows applications directly on your Mac without any virtualization or dual booting.  

#### Step 1. Installing Japanese fonts on your Mac.  

1. Download the font pack [here](https://drive.google.com/file/d/1gOv5Y4eDMtZTFJIXFWY62nFqkmeeBMkD/view?usp=sharing)
2. Double click the .zip file to extract it in Finder. This may happen automatically.  
3. Open Spotlight Search (++cmd+space++) and search for *Font Book* and open it.  
4. Click the + button and choose the extracted folder (macOS Japanese fonts [learnjapanese.moe])
5. Click *Open* to install. 

#### Step 2. Installing the Wine compatibility layer.  

Now we need to install Wine, which will let us run PlayOnMac.
You need to install *Homebrew* first, so we can install Wine properly from the Terminal.  

First we need to set Gatekeeper to allow us to install non App Store verified apps. Type the following command below and hit ++return++ 

```bash
sudo spctl --master-disable
```

Authenticate with the your password. You can now go in **System Preferences** > **Security & Privacy** > click the Lock at the bottom left > choose **Anywhere**.

!!! note "Re-enabling Gatekeeper"  
	You can revert this change using `sudo spctl --master-enable`

Now back in the Terminal, we will now install *Homebrew*, copy and paste the command below and hit ++return++  
!!! warning "macOS High Sierra and older"  
	macOS High Sierra and older versions is not officially supported by Homebrew anymore. This can successfully install on High Sierra but may fail entirely on anything older.  
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

It will ask for your password because it is an administrative action. Hit ++return++ when asked, and install Command Line Utilities when prompted.
When the Command Line Utilities installation is complete, press any key. Now we will need to enter our password again to complete the installation of Homebrew.  

The installation of Homebrew will take a while, please wait.   

Now we need to install **XQuartz**, a dependency of Wine.  

```bash
brew install --cask xquartz
```
This will take a while.  

Then add the taps for Wine:
```bash
brew tap homebrew/cask-versions
brew tap gcenx/wine
```
Now:  
```bash
brew install --cask --no-quarantine wine-crossover20.0.2
```
!!! note "macOS Sierra"  
	You need to do `brew install --cask --no-quarantine wine-crossover` instead.  

We are all done with the Terminal now!    

#### Step 3. Using PlayOnMac  

Download and install PlayOnMac here: [[Download PlayOnMac]](https://www.playonmac.com/en/download.html)  

Make sure you have your downloaded VN already at hand. Mount the .iso file if you haven't already.  

!!! info ".MDF/.MDS files"  
	If you have .MDF/.MDS files, you can use The Unarchiver to just extract the MDF file and you'll be fine. If you want to make an ISO, then you can just rename the .mdf to .iso, if that does not work then you can do `brew install mdf2iso` and then `cd` into your directory and do `mdf2iso <file>.mdf <new file>.iso`  

1. Open PlayOnMac
2. Click "Install a program", then "Install a non-listed program"
3. Keep clicking Next until you reach *Install a program in a new virtual drive*. Choose that.
4. Put any name. I put *VN* because we will be using this virtual drive for *multiple applications*  
5. Click next, then click next again
6. Choose 32 bits Windows installation
7. Now where it says *Please select a set-up file* to run, **Don't do anything yet.**
8. We need to install Japanese fonts into your virtual drive now, download [[this .zip file]](https://drive.google.com/file/d/1OiBgAmt3vPRu08gPpxFfzrtDgarBGszK/view?usp=drivesdk)  
9. On the main PlayOnMac main window, click Configure, choose your virtual drive (mine is **VN**), click on the *Miscellaneous* tab and click **Open virtual drive's directory**. Put the fonts in the `drive_c/windows/Fonts`  folder.
10. Now we need to set Japanese DOS environment variables. 
11. On the main PlayOnMac main window, click Configure, choose your virtual drive (mine is **VN**), click on the *Wine* tab and click **Registry Editor**
12. In HKEY_CURRENT_USER, click on Environment, right click, New > String value. Make the name **LC_ALL**
13. Now double click it, set the value to **ja_JP.UTF-8**
14. Exit.  
15. Now back in PlayOnMac, where it says *Please select a set-up file*, click **Browse**
16. Navigate to your VN's installation files, and choose the .exe or .msi file. 
17. Now click Next.  
18. Proceed with the Windows installation.  
19. After it is done, make the shortcut for it, BUT do not launch it yet!  
20. We need the set the VN to launch with Japanese locale now.
21. On the main PlayOnMac main window, click Configure, choose your virtual drive (mine is **VN**), click on the *Miscellaneous* tab and in the box where it says "Command to exec before running the program", type THIS: `LC_ALL="ja_JP.UTF-8" TZ="Asia/Tokyo"`.
22. Now we need to install libraries that will allow the VN to run properly. 
23. Download [this dependencies pack]ILL ADD THE LINK LATER OK. Put the folder in a memorable location on your Mac. 
24. On the main PlayOnMac main window, click Configure, choose your virtual drive (mine is **VN**), click on the *Wine* tab and click **Command Prompt**
25. In the command prompt. Use `CD` (CHANGE DIRECTORY) to the location of the "dependencies" folder. E.g. `CD Z:/Users/shoui/Downloads/dependencies`
26. Run `install.bat` by typing install.bat, hit ++enter++.
27. Wait for install
28. Done, now just launch your VN!!!!!!

!!! failure "BORKED: WHY APPLE"
	THIS WAS SUPPOSED TO WORK BUT I RAN INTO SOME UNPREDICTABLE ERRORS JUST WAIT UNTIL THIS MESSAGED IS REMOVED OK
	OR JUST USE A DAMN VIRTUAL MACHINE!!! OR BOOT CAMP!!! YOU DONT EVEN NEED WINDOWS!!! LINUX WITH WINE WORKS AMAZINGLY!!! 
	WINE ON MAC IS A NIGHTMARE!! ARGHHH1!!!!!

## GNU/Linux

Visual novels are only Microsoft Windows applications, therefore you must use Wine in order to run them. This works exceptionally well on Linux.  

### Wine

Follow the steps below to run VNs on Linux. 

#### Step 1. Install Dependencies

**Arch**

You will need to enable multilib before running this command. To do this, uncomment the `[multilib]` section in `/etc/pacman.conf`.

```bash
sudo pacman -S wine winetricks giflib lib32-giflib libpng lib32-libpng libldap lib32-libldap gnutls lib32-gnutls mpg123 lib32-mpg123 openal lib32-openal v4l-utils lib32-v4l-utils libpulse lib32-libpulse libgpg-error lib32-libgpg-error alsa-plugins lib32-alsa-plugins alsa-lib lib32-alsa-lib libjpeg-turbo lib32-libjpeg-turbo sqlite lib32-sqlite libxcomposite lib32-libxcomposite libxinerama lib32-libgcrypt libgcrypt lib32-libxinerama ncurses lib32-ncurses opencl-icd-loader lib32-opencl-icd-loader libxslt lib32-libxslt libva lib32-libva gst-plugins-base-libs lib32-gst-plugins-base-libs lutris cdemu-client cdemu-daemon
```

!!! info "Custom and LTS Kernels"
	If you are using a custom kernel such as Xanmod, install `vhba-module-dkms`. Otherwise, install `vhba-module`.  

You can then enable the CDEmu daemon by running:

```bash
sudo systemctl enable --now cdemu-daemon
```
**Debian/Ubuntu**

First you will need to enable 32-bit architecture.  
```bash
sudo dpkg --add-architecture i386
```  
Download the WineHQ repository key:  
```bash
wget -nc https://dl.winehq.org/wine-builds/winehq.key
```  
Now add the WineHQ repository key:  
```bash
sudo apt-key add winehq.key
```  
Add the repository:  

!!! info "Ubuntu 20.10"
	If you are on Ubuntu 20.10 you must do `sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ groovy main' -y` instead. 
```bash
sudo add-apt-repository 'deb https://dl.winehq.org/wine-builds/ubuntu/ focal main' -y
```
Add PPA's for Lutris:  
```bash
sudo add-apt-repository ppa:lutris-team/lutris -y
```
Add PPA's for CDEmu:  
```bash
sudo add-apt-repository ppa:cdemu/ppa -y
```
Update packages:  
```bash
sudo apt update
```
Now install the stable version of Wine:  
```bash
sudo apt-get install --install-recommends winehq-stable -y
```
Now install Lutris, CDEmu and some needed libraries:  
```bash
sudo apt-get install lutris gcdemu cdemu-client libgnutls30:i386 libldap-2.4-2:i386 libgpg-error0:i386 libxml2:i386 libasound2-plugins:i386 libsdl2-2.0-0:i386 libfreetype6:i386 libdbus-1-3:i386 libsqlite3-0:i386 libgstreamer-plugins-good1.0-0:i386 ocl-icd-dev:i386 -y
```
Now we need to install `winetricks` manually because the one on the repository already is outdated and causes errors.  
First, wget the binary:  
```bash
wget https://raw.githubusercontent.com/Winetricks/winetricks/master/src/winetricks
```
Use `chmod` to make it into an executable:  
```bash
chmod +x winetricks
```
Now copy it to your `/usr/bin` so it can be used in a command line.  
```bash
sudo cp winetricks /usr/bin
```  
All done!  

**Gentoo**

Make sure your kernel is compiled with the following options enabled:

1. `CONFIG_BLK_DEV_SR`
2. `CONFIG_ISO9660_FS`
3. `CONFIG_UDF_FS`

It is recommended to have the following global use flags in your `make.conf`:

1. `X`
2. `pulseaudio`
3. `jpeg`
4. `png`

```bash
sudo emerge -av virtual/wine games-util/lutris app-cdr/cdemu app-emulation/winetricks
sudo modprobe vhba
```

Edit your `/etc/conf.d/modules` file and add this:

```toml
modules="vhba"
```

In order for the CDEmu daemon to be started automatically on boot, you will need to have dbus enabled. You can enable it by running:

```bash
sudo rc-update add dbus default
```

#### Step 2. Configure Wine and install runtimes

First we need to create a 32 bit Wine prefix, this has the best compatibility and 64 bit is unnecessary for VNs.

```bash
WINEARCH=win32 wineboot
```
Now we need to install the common redistributables such as DirectX, Visual C++ Runtimes and .NET Framework 3.5 and other things that make video cutscenes work. 

!!! tip "Optional: Font smoothing"
	You can do `winetricks fontsmooth=rgb` because without it, the font is simply awful.  

!!! tip "Optional: GUI Improvments"
	You can open the Registry Editor using `wine regedit` and import [this .reg file](https://cdn.discordapp.com/attachments/813105334763126814/813105422285799464/wine_breeze_colors.reg), the GUI should look nice and clean then.  

```bash
winetricks ffdshow quartz wmp10 lavfilters d3dx9 dxvk dotnet35 vcrun2003 vcrun2005 vcrun2008 vcrun2010 vcrun2012 vcrun2013 vcrun2015
```
Then, run this command to disable DLL overrides:

```bash
winetricks alldlls=default
```

You need to install Japanese fonts to Wine now. Please download the pack below.  
[[Google Drive]](https://drive.google.com/file/d/1OiBgAmt3vPRu08gPpxFfzrtDgarBGszK/view?usp=drivesdk)  
Unzip the file and move the font files to your `Fonts` folder in `~/.wine/drive_c/Windows/Fonts`    

!!! question "Why not install `cjkfonts` in winetricks?"
	Because it doesn't work properly for VNs.

If your Wine Windows version was set to XP, set it back to 7 using:  

```bash
winecfg -v win7
```  
It is useful to know that changing the Windows version in Wine does not change the way Wine behaves, rather, it only changes what it reports to the application, since 99% of VNs recommend Windows 7, we will be using that.  

Once thats done, we can setup Lutris.

Open Lutris, and click the plus icon in the top left corner, and click Install runners.

![Image](img/vnlinux1.jpg)

Scroll down to the bottom and find "Wine" and click the cog icon next to it.  

![Image](img/vnlinux2.jpg)  

Now go to System options and set the environment variables as shown below and click Save.  

![Image](img/vnlinux3.jpg)  

#### Step 3. Installing the visual novel

I will be using 古色迷宮輪舞曲～HISTOIRE DE DESTIN～ for this demonstration. Visual Novels usually come in .ISO files and if not, an .MDS/.MDF file which can be converted to an .ISO using tools such as mdf2iso.  
In the case of 古色迷宮輪舞曲～HISTOIRE DE DESTIN～, the install files came in an .ISO, so we got lucky here.  

Navigate to the path of the .ISO  

```bash
cd /path/to/visualnovelfolder
```

Load the .ISO file with CDEmu
```bash
cdemu load 0 file.ISO
```

Create a mount point for the ISO file.

```bash
sudo mkdir -p /media/cdrom0
```
Now we can mount our ISO to our mount point.  

```bash
sudo mount -o loop file.ISO /media/cdrom0
```  

If all went well, you will be able to see the ISO contents like:  

![Image](img/vnlinux4.jpg)

Next, we will run the setup file using `wine`:

```bash
LC_ALL="ja_JP.UTF-8" TZ="Asia/Tokyo" wine launcher.exe
```

Proceed with the installation. The game may be installed in `~/.wine/drive_c/Program Files` or wherever you chose to install it.

Now we can add the game to Lutris so we can launch it quickly.  

Back in Lutris, click the plus icon in the corner, add the name of the VN, choose Wine as the runner and under "Game Options" navigate to the game's executable. You should also change the prefix architecture to 32-bit.

![Image](img/vnlinux5-sup.jpg)  

![Image](img/vnlinux5.jpg)  

!!! warning "Vulkan Unsupported Systems"
	If your system does not support Vulkan, you must disable DXVK in "Runner options", this will fallback to regular D3DX9. DXVK is a Vulkan implementation of Direct3D so we will be keeping it on even though Vulkan may not make much of a difference.  

Now you can just launch it in Lutris!  

![Image](img/vnlinux6.jpg)  

and viola!  

![Image](img/vnlinux7.jpg)

Now go back to [Visual Novel Guide](https://learnjapanese.moe/vn/#looking-up-words-in-vns-using-yomichan-and-textractor) to learn how to use Textractor, it works perfectly under Wine.

### Troubleshooting: Linux

#### Shift-JIS

When you've done everything correctly but your VN text still looks like this: ????? ?????????? ???????????? 
This means your VN needs to use ja_JP.sjis instead of ja_JP.UTF-8.  

You need to download ja_JP.sjis from [here](https://cdn.discordapp.com/attachments/813105334763126814/825472692558889022/ja_JP.sjis.zip) first.  

Unzip it to a memorable location on your computer and `cd` into that directory.  

```bash
cd /path/to/ja_JP.sjis
```

Now compile the locale using `localedef`:
```bash
localedef  -i ja_JP  -f SHIFT_JIS ./ja_JP.sjis --no-warnings=ascii
```

Using `sed`, edit your locale.gen to include ja_JP.sjis:

```bash
sed -i '/ja_JP.UTF-8 UTF-8/a ja_JP.SJIS SHIFT_JIS  ' /etc/locale.gen
```
Now generate locales:

```bash
locale-gen --no-warnings=ascii
```

You can then change the `LC_ALL` environment variable in Lutris to `ja_JP.sjis`.
 
## BSD (FreeBSD)

Visual novels are only Microsoft Windows applications, therefore you must use Wine in order to run them.

### Wine

TBA

## Android

### Using PPSSSPP Emulator

There are a couple of native Android visual novels but these are usually spin-offs/gacha cash-grabs.  

The best option is to use [PPSSPP](https://play.google.com/store/apps/details?id=org.ppsspp.ppsspp) emulator and download PSP ROMs.

PSP games are probably the best quality visual novels you can get on a mobile device.

![Image](img/vnpsp1.jpg)  

## iOS

### Non-jailbreak: Using PPSSPP Emulator

Again, there *are* in fact native iOS visual novels, but I feel like emulating PSP visual novels is a better idea, just because the games on a PSP console are just going to be *so* much higher quality than games made for phones.

It is a little more tricky to get PPSSPP working on iOS without a jailbreak, but it is definitely possible.  
You will need:  
[AltStore](https://altstore.io/) - check the [FAQ](https://altstore.io/faq/) on the website for instructions  
[PPSSPP IPA](https://build.ppsspp.org/builds/iOS/ppssppbuildbot-org.ppsspp.ppsspp-dev-working-ios.ipa)

### Jailbreak: Using PPSSPP Emulator

PPSSPP can be installed via Cydia package by adding the repository: `https://cydia.ppsspp.org/`.

## Emulators

TBA

## Windows XP Virtual Machine

### Requirements
	
Oracle VM VirtualBox [(Link)](https://www.virtualbox.org/wiki/Downloads)  

Windows XP Professional SP3 Disc Image (.ISO) (Will not be provided here due to copyright, contact me at the Discord)  

At least 4GB RAM (Recommended)  

At least 30GB free disk space. (Recommended) 

Virtualization technology enabled in your BIOS. (Highly Recommended, you can search on Google how to do this for your computer.)  


### Full Setup

Here I'll walk you through the entire process. From installing Windows XP to getting a VN hooked and working.

1. Install Oracle VM VirtualBox  
2. Acquire a disc image for Windows XP Professional SP3  
3. Open Oracle VM Virtual Box, at the top, click the blue "New" button.  
4. You can set any name you wish.  
5. Make the "Type" `Microsoft Windows` and the "Version" `Windows XP (32-bit)`. Click next.   
6. For the memory size, make it at least `768` MB. Click next.  
7. Keep on clicking next until you reach the "File location and size". Over here you'd want to set the size of the virtual hard disk to `30.00 GB`. Now click Create.  
8. Now double click the virtual machine that has now appeared in the left menu to run the virtual machine.    
9. In the "Select start-up disk" dialog box, click the little folder icon, and then click "Add".  
10. Navigate to the disc image (.ISO) for Windows XP Professional SP3, open it and then click "Choose".  
11. Now click "Start" and wait for Windows XP to boot into the installation.  
12. You will be greeted with a blue installation screen. Don't worry. Just keep hitting the ++enter++ key.  
13. When the initial setup is complete, Windows XP will boot into another installation screen. Wait it out.  
14. Before installation finishes, it will ask for your name, computer name, password. Just do whatever. I put "shoui" for every field. You will be asked to set a time zone too, do Tokyo because some VNs actually check for Japanese time zone.
15. Once it finishes installation and reboots, you will be greeted with Windows XP setup. Enjoy the music!  
16. Click Next, then Yes, then Next, then No, then Next, then No, then put your name, then Finish.  
17. Wait until Windows XP boots into the desktop. Nostalgic isn't it?  
18. Turn off your Windows XP virtual machine. ++alt+f4++ > Turn Off  
19. We will now increase the specs of your VM. Click on the VM on the left menu, then click the orange "Settings" button.  
20. Go in System > Processor, and increase the CPU core count to whatever is on the green bar. For me it's `2` CPUs. If you want to use more than 4GB of memory on this VM, enable PAE/NX too.
21. Now go in Display and enable 3D acceleration and set video memory to `128 MB`
22. Now launch your VM again by double clicking it in the left menu.
23. Once you are in the XP desktop. On the VirtualBox window, click "Devices" and then click on "Insert Guest Addons CD Image"  
24. It will now automatically run VBox Guest Additions setup, install it and reboot your VM. Go in Devices again and set Drag and Drop to Bidirectional. This will allow us to drag and drop files from our actual PC to our VM.  
25. Now we will enable Japanese locale. Again in "Devices", click on Optical Drives > select the disc image you used to install Windows XP. Exit setup when prompted.  
26. Now open a Run dialog box, by doing ++windows+r++, and enter `intl.cpl`. Go in the `Languages` tab and check "Install files for East Asian languages" now hit Apply. Do not reboot yet.   
27. Go in the Regional Options tab and set format to Japanese and location to Japan. Hit Apply.  
28. Now go in the Advanced tab and set "Language for non-Unicode programs" to Japanese. Hit Apply. Now reboot your VM when prompted.  
29. Now go and install some software. I recommend you download these on your actual PC and just drag and drop it into your VM.  
		[7-Zip (32 bit)](https://www.7-zip.org/a/7z1900.exe)  	
		[Mozilla Firefox 52.9.0 ESR](https://ftp.mozilla.org/pub/firefox/releases/52.9.0esr/win32/en-US/Firefox%20Setup%2052.9.0esr.exe)  - Most recent browser that supports XP.  
		[ITHVNR](https://cdn.discordapp.com/attachments/715225470798659667/799731133683728404/ITHVNR-3.4524.1-win32.7z) - because Textractor is not supported on XP. Install vcredist_x86 to make it work.  
		[MacType](https://github.com/snowie2000/mactype/releases/download/2019.1-beta6/MacTypeInstaller_2019.1-beta6.exe) - Fix pixelated CJK font. Also recommend on Win10. Use registry mode. :slight_smile:  
30. In "Devices" enable bidirectional clipboard.
31. Download your visual novel of choice and drag and drop it to your VM. If it needs to be installed, then install it.
32. Open ITHVNR and your VN. In ITHVNR, go in "Process", find the process of the VN, then click "Attach" and "OK"
33. Advance some text in the VN. Now cycle through the hooks in ITHVNR and find the right hook.
34. ITHVNR will automatically copy text to your clipboard, which is shared with your actual PC. I recommend you use [Yomichan](/yomichan)'s clipboard monitor :)
35. Phew, that's pretty much it, have fun!
![Image](img/winxp1.jpg)
*from vm*
![Image](img/winxp2.jpg)  
*from actual pc*

## PC-98

TBA