# RealworldCTF 3rd BoxEscape

## How this challenge works

> Contact: ChenNan in discord
Email: demo@realworldctf.com



You send me an email with subject `RealworldCTF-3rd-BoxEscape` to demo@realworldctf.com
It should contain your `exploit archive file` and `usage documentation`.

Your email should at least contain the following text, in the precise format shown
below:

 - Name: <your team name>
 - Token: <your team token from platform>
 - Contact: <your email>
## Goal

Please escape VirtualBox and spawn a calc("C:\Windows\System32\calc.exe") on the host operating system.

You have the full permissions of the guest operating system and can do anything in the guest, including loading drivers, etc.
    
But you can't do anything in the host, including modifying the guest configuration file, etc.

Hint: SCSI controller is enabled and marked as bootable.
    
## Environment
In order to ensure a clean environment, we use virtual machine nesting to build the environment.
The details are as follows:
- VirtualBox:6.1.16-140961-Win_x64.
- Host: Windows10_20H2_x64 Virtual machine in Vmware_16.1.0_x64.
- Guest: Windows7_x64 7600.16385.090713-1255_x64fre Virtual machine in VirtualBox_6.1.16_x64.
    
We provide download links for all the above environments, please see the `Reference` section.
    
## Verification process

Here is what I will do when I receive your `exploit` files. (possibly replacing steps 1&2 after the first time)
    
1. Download and import the challenge VMware image
2. Take a VM snapshot
3. Open Virtualbox and run a guest(Windows7 Virtual machine).
4. Copy your `exploit files` to the guest through Virtualbox file sharing.
5. Next, I will follow the `exploit usage document` you provided.
6. Check if the goal is reached.
7. Restore VM snapshot and try again.

If the calc is spawned, I will reward you with the flag by email.

**I will keep trying for a total of 3 times before I give up.**
    
**The running time for each try cannot exceed 3 minutes.**

**I will not accept more than 3 emails per team.** If you really need more, you
will need to explain to me in detail why you messed up your first 3 tries and
convince me that you deserve a 4th chance.

## Reference

### Attachment download    

The complete environment can be downloaded from the link below:

https://drive.google.com/drive/folders/155luapTB4zshnofB-0pgPHfc0ne7NE7Z

or

链接:   https://pan.baidu.com/s/1Pb289urLyZzS2sxeH_db4A 
提取码: rwct 

### Attachment description

You can import the `complete environment` below, no need to install separately:

***It is strongly recommended to use this packaged environment, because our verification environment is also derived from this.***
    
- *rwctf_virtualbox.zip*: 
  Packaged environment
  Vmware complete environment image(ovf)
    

    
You can also install `independent components` separately, including the following:
    
- *VMware-workstation-full-16.1.0-17198959.exe*:
    https://download3.vmware.com/software/wkst/file/VMware-workstation-full-16.1.0-17198959.exe

In order to ensure a clean environment, we use virtual machine nesting to build the environment. All the components below are installed on vmware.
    
- *19042.631.201119-0144.20h2_release_svc_refresh_CLIENTENTERPRISEEVAL_OEMRET_x64FRE_en-us.iso*: 
    Host system installed on vmware
    Edition	Windows 10 Enterprise Evaluation
    Version	20H2
    Installed on	1/6/2021
    OS build	19042.631
    Experience	Windows Feature Experience Pack 120.2212.31.0
    https://software-download.microsoft.com/download/pr/19042.631.201119-0144.20h2_release_svc_refresh_CLIENTENTERPRISEEVAL_OEMRET_x64FRE_en-us.iso
    
- *VirtualBox-6.1.16-140961-Win.exe*: 
  VirtualBox that need to be escaped installed on host system.
  Consistent with the official
  https://download.virtualbox.org/virtualbox/6.1.16/VirtualBox-6.1.16-140961-Win.exe

- *7600.16385.090713-1255_x64fre_enterprise_en-us_EVAL_Eval_Enterprise-GRMCENXEVAL_EN_DVD.iso*:
  Guest system(Windows7_x64 7600.16385.090713-1255_x64fre) installed on virtualbox http://care.dlservice.microsoft.com/dl/download/evalx/win7/x64/EN/7600.16385.090713-1255_x64fre_enterprise_en-us_EVAL_Eval_Enterprise-GRMCENXEVAL_EN_DVD.iso

- *win764.vbox*:
  Configuration file of virtualbox virtual machine(guest).
  The file cannot be modified.

###  This is the md5 of each file：

- VirtualBox:6.1.16-140961-Win_x64.
  MD5 (VirtualBox-6.1.16-140961-Win.exe) = f6f6a4e5aebca49e025ba76f9a41507a

  
- Host: Windows10_x64 Virtual machine in Vmware_16.1.0_x64.
  MD5 (19042.631.201119-0144.20h2_release_svc_refresh_CLIENTENTERPRISEEVAL_OEMRET_x64FRE_en-us.iso) = 3b5da0c84dacdb89abf4502d79cf0ca4

  

- Guest: Windows7_x64 7600.16385.090713-1255_x64fre Virtual machine in VirtualBox_6.1.16_x64 
  MD5 (7600.16385.090713-1255_x64fre_enterprise_en-us_EVAL_Eval_Enterprise-GRMCENXEVAL_EN_DVD.iso) = 1d0d239a252cb53e466d39e752b17c28

  

- win764.vbox （virtualbox configuration file )
  MD5 (win764.vbox) = 002a15f672717599bbf8ee5c63dee915

  

- packaged environment: rwctf_virtualbox.zip  (Vmware complete environment image(ovf)
  MD5 (rwctf_virtualbox.zip) = 30bb7fc03529f0686e3aeff38442b2e2