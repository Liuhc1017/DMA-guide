# DMA-guide
This is a guide to dual boot with Singapore MOE DMA, without removing any files and the normal DMA via Dual Boot.
Introduction 
Instead of a normal computer booting only one OS, we can partition the disk and boot multiple OSes, including a fresh copy of any OS you want and normal MOE DMA. This inmproved method still allows you to login to your MIMS account and have a computer of your own that you can do whatever you want on.
I am not liable for any damages caused. Exercise your own discretion.


Dependencies:
  USB drive: at least 8 GB of space as of 13/2/2026 (everything will be erased)
  Password to Admin account on DMA
  Windows 11 Multi edition ISO image or any Disk image of an OS of your choice(Optaining the windows image will be covered in this guide)

  
#You might need the administrator password for this
Downloading Windows 11 Multi edition ISO image:
  1. Visit https://www.microsoft.com/en-us/software-download/windows11.
  2. Scroll down to this page:
  3. Select "Windows 11(multi-edition ISO for x64 devices)".
  4. Press confirm, choose your language and press confirm.
  5. After loading is finished, click on "64-bit Download" and wait for the download to be done.


Creating a bootable USB
  1. Visit https://rufus.ie/en/.
  2. Scroll down to the downloads page.
  3. Choose the exe file corresponding to your needs (Usually its Windows x64 Standard).
  4. Click on the download link and wait for the exe file to download.
  5. After download is finished, click on the exe file and follow the instructions for the setup process. At the end, lauch rufus.
  6. Plug in your USB drive (at least 8 GB; everything on it will be erased). 
  7. Open Rufus (if Windows asks for permission, click Yes).
  8.In Rufus:
        Device: select your USB drive
        Boot selection: choose Disk or ISO image
        Click SELECT and pick your downloaded Windows 11 ISO
        Partition scheme / Target system
        If your PC uses UEFI (most modern PCs):
  9.Partition scheme: GPT
        Target system: UEFI (non CSM)
        If your PC is older and uses Legacy BIOS:
        Partition scheme: MBR
        Target system: BIOS (or UEFI-CSM)
        (If you’re unsure, GPT + UEFI is usually correct for Windows 11.)
  10.Volume label: optional (e.g., WIN11_USB).
  11.File system: keep default (usually NTFS).
        If Rufus asks about UEFI:NTFS, allow it (that’s normal).
  12.Click START.
  13.If Rufus shows “Windows User Experience” options, you may see checkboxes like:
        Remove requirement for TPM / Secure Boot / RAM
        Remove requirement for Microsoft account
        Choose what you need. I suggest unchecking them.
  14.When warned that the USB will be erased, click OK.
  15.Wait until it says READY, then click CLOSE. Safely eject the USB.
  16.Windows 11 Pro will be the preferred OS. To install windows 11 pro, put the file "ei.cfg" found in this repository into your USB --> Sources.

        
Partitioning the disk
  1. Press  Win+X and go to Disk management.
  2. Right click on you C Drive and click shrink volume. Wait for a while
  3. Choose how much space you want for a fresh new windows 11 and click Shrink.
  4. Wait for the shrink to complete.


Installing Windows 11 on the new disk partition
  1. Plug your USB in.
  2. Restart your computer and try to enter the boot screen. Search the key you need to press(normally F2 or F12)
  3. Change the boot order to boot with your USB.
  4. Follow the instruction and choose the empty partition when prompted where to install windows 11. You might need ethernet for this.
  


    
  

