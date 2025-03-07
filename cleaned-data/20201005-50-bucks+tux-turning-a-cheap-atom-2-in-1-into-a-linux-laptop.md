It all started with a goal. When I wake up late at night and can't go back to sleep (which happens way too often tbh), I wanted something I could write on. Something compact and light but with a keyboard. Basically I wanted a barebones, ultra-compact laptop that was cheap. You may have at some point in the distant past seen something that fits this description called a [netbook](https://en.wikipedia.org/wiki/Netbook). Well, those don't really exist anymore. So I ventured to make something like that.

## Finding the laptop
### Requirements
* It had to be cheap. The maximum I'd be willing to spend was $200. $100 or less would be even better.
* It had to be small. I didn't want anything with a screen over 11", nothing under 8". The more compact the better, but under 8" would be difficult to use IMO.
* It had to have an [x86](https://en.wikipedia.org/wiki/X86) processor. I wanted to run a non-mobile OS, probably Linux, because I really don't like any version of Windows that I've used since Windows 7 (really since XP).
* I had to reasonably believe I could get it up and running with my browser of choice, [Chromium](https://www.chromium.org/Home), and a lightweight text editor with integrated terminal, preferably [VS Code](https://code.visualstudio.com).

The search for a laptop that fit these requirements was kinda long. I looked on all the major laptop vendors' sites (e.g. HP, Dell, Acer, Asus, Lenovo, etc.). Then I scoured the big box stores' sites (e.g. Best Buy, Target, Costco, Walmart, etc.). Then I searched Amazon, but decided that anything I bought for cheap off Amazon would be a bad idea. Then I searched refurbished laptops across all the manufacturers and stores. I considered several and almost pulled the trigger on one that was close to $200 until I came across a refurbished, economy 2-in-1 tablet/laptop. There were a whole lot of sacrifices, but it satisfied my requirements. It wasn't much, but it was cheap, tiny, and had potential.

### The laptop
**[Ematic EWT826BK](https://ematic.us/product/ematic-8-hd-windows-10-tablet-32gb-with-wifi-intel-atom-z3735g-processor-docking-keyboard-ewt826bk/)**
\[[refurbished from Walmart.com](https://www.walmart.com/ip/Ematic-EWT826BK-8-32GB-Windows-Quad-Core-Tablet-Black-Refurbished/454553155)\]
* **Price:** $57.66 ($49.00 purchase price + $4.66 sales tax + $4.00 merchandise fee) -- also fuck whatever a merchandise fee is. I almost didn't buy this laptop because of this stupid $4 fee.
* **CPU:** 1.3 GHz Intel Atom Quad-core
* **RAM:** 1GB DDR2
* **Storage:** 32GB SSD
* **OS:** Windows 8.1
* **Other Specs:** 8" touchscreen @ 1280x800, 802.11b/g/n wifi, Bluetooth v4.0, 1xMicro USB 2.0 port, 1xmicroSD card slot, back and front 2MP webcams, 1x3.5mm headphone jack, keyboard case included.

*I didn't have a banana, so I used a quarter for scale instead.*

I bought this 2-in-1 refurbished from walmart.com. It was dirt cheap, super small due to the keyboard case and 2-in-1 form factor, and ran an x86 Intel Atom processor. Another big plus was that it came with  Windows 8.1 installed. I never had any intention of keeping or even using Windows, but having it installed meant that a full-featured, non-mobile OS install was possible.

The reviews on it weren't great. The positive reviews were pretty much all around the size of the device. The much more numerous 1-star reviews were primarily around the device being slow and first-run Windows updates taking up 80% of the disk space and leaving the device near useless due to slow application load times.

I didn't let the bad reviews deter me. I'm pretty well-versed in OS's, and was pretty confident a lot of the speed and performance issues were caused by Windows. If there's one thing I know about Windows it's that it will absolutely update itself into a state of inoperability on hardware that barely clears the minimum specs. That's what this was. I could fix it with Linux.

## Choosing the right Linux distro
### [Lubuntu](https://lubuntu.me)
Choosing the right distro was extremely important. This is a low-end device. I needed lightweight. My first inclination was Lubuntu, the lightest weight, official [Ubuntu](https://ubuntu.com)-based distro. It being Ubuntu-based is a big benefit. It meant I wouldn't have to deal with a lot of issues installing Linux comes with (e.g. abandoned distros, lack of hardware support, difficult install process, etc.). So I decided to give it a try.

I got Lubuntu installed and running without too much trouble. Restarting and launching the live USB via the 32-bit UEFI that came with this 64-bit machine, was a bit of a trick (I'll cover the install process in the next section) The touchscreen didn't work though. This device came with a keyboard case but didn't have a mouse. I figured I'd need the touchscreen (I was wrong). So I tried out a few different distros in hopes of finding one that worked decently on this device and supported its touchscreen.

### [KDE Neon](https://neon.kde.org)
In my research, I'd read that the KDE desktop environment was much less resource intensive than it traditionally has been. I also read that KDE Neon was a better experience than Kubuntu and was similarly based on Ubuntu.

I got the live USB to boot, but the install failed at the requirements check and didn't allow the install to start (which is weird, because most Linux installs I've run usually let you continue).

### [Kubuntu](https://kubuntu.org)
Since KDE Neon didn't work, I installed Kubuntu. It is the official Ubuntu distro that includes the KDE desktop environment. So very similar to KDE Neon.

Kubuntu installed fairly easily. Similar to Lubuntu. After install, the touchscreen still didn't work and it was sluggish. It was sluggish to the point that launching Firefox and browsing would frequently lock the device up. Successful install, beautiful UI, but still a downgrade from Lubuntu for this device.

### [Ubuntu Touch](https://ubuntu-touch.io)
Since Ubuntu Touch is the mobile and tablet version of Ubuntu (not official but kinda official) I thought it might work. Nope. The device wasn't supported.

### [Peppermint OS](https://peppermintos.com)
Peppermint OS is a distro based off of [Linux Mint](https://linuxmint.com). It is meant to be web-centric and lightweight, kinda like Chrome OS but more legit Linux,

It was tricky getting it to boot to the live USB, but managed it with the process I'll detail later in this post. The install was slow but had no issues until after completion, when it presented an error dialog about [GRUB](https://www.gnu.org/software/grub/) not installing correctly. After that error, it only gave me options to reboot. So I did, and it almost bricked the device. GRUB didn't install fully. So I was presented with the GRUB rescue prompt, but without any of the standard tools that come with it. So I couldn't really do anything from here. I spent hours trying different things, and nothing worked from this prompt. Recovering from this was a major effort.

### [Fedora Workstation](https://getfedora.org/en/workstation/)
After I figured out how to get out of the GRUB rescue prompt and to the UEFI setup screen, I gave Fedora a shot. Fedora uses [GNOME 3](https://www.gnome.org/gnome-3/) as its desktop environment. GNOME is not lightweight, but it is supposed to support a lot of touchscreens. So I wanted to try it out.

Installation was easy. The live USB supported 32-bit UEFI out of the box, so that made live simple. Install went without a hitch. After install, the touchscreen still didn't work, and it was ultra slow.

This is when I gave up on the touchscreen. For what I wanted this for, I didn't really need a touchscreen anyway. I did some research and learned about [i3](https://i3wm.org), a tiling window manager that was lightweight, keyboard-centric, and pretty popular. So I decided a lightweight distro with i3 was the way to go.

### [ArchLabs Linux](https://archlabslinux.com)
ArchLabs Linux is a distro based on [Arch Linux](https://www.archlinux.org). I'm really curious about Arch. It's lightweight, bare bones, very manual, but very configurable. ArchLabs came with i3 by default. So I thought it might be a good fit.

I couldn't get the live USB to boot. I tried several different approaches, but no luck.

### Which distro I finally chose (Lubuntu + i3)
In the end, I went back to Lubuntu. It was easy to install and performed the best of all of the distros I tried. No touchscreen support, but I decided installing i3 and setting it to the default window manager would solve that issue.

After I installed Lubuntu (again), I...
* Used the default package manager, Muon, to remove every program that I saw no use for.
* Fully updated my system via Muon.
* Installed the [Snap Store](https://snapcraft.io/store), because I wanted Chromium and VS Code, and Snap makes installing both easy. Snap comes pre-installed on all official Ubuntu distros. Installing the store just gave me a pretty, easily searchable UI for it.
* Installed Chromium and VS Code via the Snap Store.
* Installed i3
* Set my default window manager to i3 in the Session Settings section of `lxqt-config`.
* Restarted.

And it worked. It worked well. Chromium ran well. I installed the [Vimium](https://vimium.github.io) extension in Chromium to make navigating the web via keyboard easier. VS Code ran fine. I cloned my personal website repo from GitHub, and it downloaded fast. Now it's exactly what I was looking for. An ultra-compact, ultra-cheap laptop that ran a non-mobile OS that I could use Chromium and VS Code on to write and occasionally do some light coding with.

## Why all of this was So difficult (32-bit UEFI on a 64-bit machine)

*Pretty much all of the info below was gleaned from a post by Intel titled* ***[Why Cheap Systems Run 32-bit UEFI on x64 Systems](https://software.intel.com/content/www/us/en/develop/blogs/why-cheap-systems-run-32-bit-uefi-on-x64-systems.html).***

The big obstacle to installing Linux in this device and many other small, inexpensive 2-in-1's that run an Atom processor is that they run 32-bit UEFI for firmware with a 64-bit processor. The reason these devices are built like this is simple, cost vs. performance.

Devices with less than 4GB of RAM don't benefit from having a 64-bit processor, and almost none of these 2-in-1 devices have that much RAM. Windows 8.1 (the OS pre-installed on my device) began offering a cheaper, 32-bit version targeted at devices like this even, which was a benefit because it performed the same but took up less disk space and was less expensive than the 64-bit version. A device's firmware and it's OS architecture need to be the same. So inexpensive 32-bit Windows requires a 32-bit UEFI. The selection of 32-bit Linux distros is limited in comparison with 64-bit distros. The Atom processor is x86 though, meaning it can operate in 16-, 32-, and 64-bit modes. So you can run a 64-bit Linux distro on the device, but installing it via the 32-bit UEFI is the challenge as most distros don't support this mixed architecture.

### How I installed 64-bit Linux with a 32-bit UEFI

* Download the Linux distro ISO you want to install.
* Make an editable, bootable live USB from the ISO. Partition scheme should be GPT. File system should be FAT32.
  * For Windows, use [Rufus](https://rufus.ie).
  * For Mac, use [UNetbootin](https://unetbootin.github.io). A lot of how-to's recommend [balenaEtcher](https://www.balena.io/etcher/), but it never left me with an  editable, bootable USB.
* Download a [bootia32.efi](https://github.com/jfwells/linux-asus-t100ta/blob/master/boot/bootia32.efi) file. This file will let your 64-bit OS live USB boot on a 32-bit UEFI. I used the jfwells one, because it is the most referenced in forums.
* Copy bootia32.efi to the `/EFI/BOOT/` directory on your live USB.
* Restart in UEFI settings (which is where you can launch your live USB from).
  * If Windows is still installed, hold the Shift key and restart using the Windows UI. This boots into Advanced Startup Options. From here select Troubleshoot > Advanced Options > UEFI Firmware Settings.
  * If Linux is installed, open a terminal, enter ‘systemctl reboot --firmware-setup’.
  * If no OS is installed, plug in an external USB keyboard via USB-to-Micro USB adapter, hold the Esc key, and restart (a hard restart is fine). The included keyboard doesn’t have an Esc key, so an external is required. After landing on the UEFI boot menu, remove the keyboard from the adapter and insert the live USB.

You can boot from your USB via the UEFI boot menu. It's pretty straightforward after that. Most distros, at least the primarily Ubuntu-based ones I tried, had no issue starting their live USB from here. ArchLabs wouldn't, and Fedora had booting to 32-bit UEFI out-of-the-box, but all of the others I tried booted via this method.

## How's it work?

It works fine. It's not fast, but it's not super slow either. It hasn't crashed since I started it. I haven't had to hard reboot it a single time. I wrote about 1/3 this blog on it, another 1/3 on my iPhone, and the last 1/3 between my personal MacBook and my work MacBook.
 

*Here's a screenshot of me writing this post in Chromium.*

*Here's my website in VSCode.*