86Box
=====
**86Box** is a hypervisor and IBM PC system emulator that specializes in
running old operating systems and software designed for IBM PC systems and
compatibles from 1981 through fairly recent system designs based on the
PCI bus.

86Box is released under the GNU General Public License, version 2. For more
information, see the `LICENSE` file.

The project maintainer is OBattler.

Community
---------
We operate an IRC channel and a Discord server for discussing anything related 
to retro computing and, of course, 86Box. We look forward to hearing from you!

[![Visit our IRC channel](https://kiwiirc.com/buttons/irc.ringoflightning.net/softhistory.png)](https://kiwiirc.com/client/irc.ringoflightning.net/?nick=86box|?#softhistory)

[![Visit our Discord server](https://discordapp.com/api/guilds/262614059009048590/embed.png)](https://discord.gg/Es3TnUH)

Building
--------
In order to compile 86Box from this repository, please follow this step-by-step 
guide:
1. Download the development environment from http://tinyurl.com/de86box. 
   Afterwards, extract it to your desired location.  Of course, also clone 
   the repository in your desired location. Downloading ZIPs is not recommended,
   as it makes it more inconvenient to keep the code up-to-date. To avoid
   issues, make sure neither path has spaces in it.
2. In the extracted environment folder, you will find a script called
   `mingw32_shell.bat`. Launch it. There are other shell launching scripts
   in there, but you should not use them.
3. Once launched, run `pacman -Syuu` in order to update the environment.
   Depending on the state of the downloaded DE, you may need to run it twice
   (once initially, and then again after re-entering the environment). Make sure
   to keep the enviroment up-to-date by re-running the command periodically.
4. Once the environment is fully updated, `cd` into your cloned `86box\src`
   directory.
5. Run `make -jN -fmakefile.mingw` to start the actual compilation process.
   Substitute `N` with the number of threads you want to use for the compilation
   process. The optimal number depends entirely on your processor, and it is
   up to you to determine the optimal number. A good starting point is the total
   number of threads (AKA Logical Processors) you have available.
6. If the compilation succeeded (which it almost always should), you will find
   `86Box.exe` in the src directory.
7. In order to test your fresh build, replace the `86Box.exe` in your current
   86Box enviroment with your freshly built one. If you do not have a
   pre-existing 86Box environment, download the latest successful build from
   http://ci.86box.net, and the ROM set from http://tinyurl.com/rs20180914.
8. Enjoy using and testing the emulator! :)

If you encounter issues at any step or have additional questions, please join
the IRC channel and wait patiently for someone to help you.

Nightly builds
--------------
For your convenience, we compile a number of 86Box builds per revision on our
Jenkins instance.

| Regular | Optimized | Experimental |
|:-------:|:---------:|:------------:|
|[![Build Status](http://ci.86box.net/job/86Box/badge/icon)](http://ci.86box.net/job/86Box)|[![Build Status](http://ci.86box.net/job/86Box-Optimized/badge/icon)](http://ci.86box.net/job/86Box-Optimized)|[![Build Status](http://ci.86box.net/job/86Box-Dev/badge/icon)](http://ci.86box.net/job/86Box-Dev)

### Legend
* **Regular** builds are compiled using the settings in the building guide
  above. Use these if you don't know which build to use.
* **Optimized** builds have the same feature set as regular builds, but are
  optimized for every modern Intel and AMD processor architecture, which might
  improve the emulator's performance in certain scenarios.
* **Experimental (Dev)** builds are similar to regular builds but are compiled
  certain unfinished features enabled. These builds are not optimized.

Donations
---------
We do not charge you for the emulator but donations are still welcome:
https://paypal.me/86Box .
