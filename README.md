# Setup your machine!

Welcome to this setup where we are going to install the tools required to make your machine a true developer environment :muscle:



## Prerequisites

Before we start it is important that you meet those prerequisites to make sure that everything run smoothly during this setup.
Take your time to read through everything and don't hesitate to ask for help if you feel stuck.
Ready? Let's go :sunglasses:



## Latest version of Windows

For this setup, you need to run the latest version of Windows.

This means that you need to run Windows 10 with all the latest updates installed.

You can check that it is the case by clicking on **Start>Settings>System>About**, locate where it says *edition*. If you see something that starts with "Windows 10..." you're good to go :muscle:.

Not the case? Don't panic :scream: You can always install windows 10 from [microsoft]( https://www.microsoft.com/en-gb/windows/get-windows-10) and click on *Check for Updates* then follow the instructions on the screen. Come back to this setup when Windows 10 is installed.

When you are sure that you're running Windows 10, it is time to check that you are running the latest updates. For this click on **Start>Settings>Updates & Security>Windows Update** then click on **Check updates**. If you have updates available please install them then reiterate until it says that you are up to date :star:



## The insider program

As the developer that you are, you always want to get the beta version of everything :nerd_face:.

It is also the case of Windows so we are going to sign up to their beta program, the **Insider program** .

Go to **Start>Settings>Updates & Security>Insider Program**

Click on **Get Started**. it will ask you to **Link an account**; follow the instructions on the screen. You will then be prompted to choose your insider parameters, choose the recommended one, the **Slow** one :snail:. Then confirm et restart your computer when you are prompted to do so.

After your computer has restarted you can double-check that you are now part of the insider program by clicking on **Start>Settings>Updates & Security>Insider Program**, you should now be prompted with the insider parameter that you chose earlier (**slow**).

It is now time to do the last updates to get the new content that you have unblock by joining the insider program. Go to **Start>Settings>Updates & Security>Windows Update**, you should see new updates available.
:warning: These updates can be very long (more than 30 minutes) so make sure your computer has battery and that you wont have to close it during the installation :warning:

Start the update and go grab a coffee :coffee: or a tea :tea:.

After the computer restarted, go to **Start>Settings>System>About**, this time locate the *Version*, if it says at least 2004, you are good to go :sunglasses:.



### Windows Subsystem for Linux

WSL is the development environment you are going to use, you can learn more about WSL [here](https://docs.microsoft.com/en-us/windows/wsl/faq).

Click on **Start** and type **powershell**. Right click on **Windows Powershell (x86)** then click on **Run as administrator**. A blue box will appear, copy paste the following command in it:
```Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux```

Press **enter** to run the command. You will be prompted to restart your computer, type **y** and **enter** to agree.

When your computer has restarted, click on **Start** and type **Microsoft Store**. Launch it. In the search bar, type **Ubuntu**. Click on the first result **Ubuntu**, not **Ubuntu 18.04 LTS**. Click on **Install**.

:warning: There is no progress bar for this installation, when it is done you will be prompted on the bottom right corner to launch it.

The first time you open WSL - it should ask you to choose a username :warning: Your username should be **one word**, **downcased** and no **special characters** :warning:

It will then prompt you for a password, when you type it will not appear on the screen, this is a security feature to make sure than if anyone where to walk behind you right now, they wouldn't be able to look at your password.

You will have to retype your password and the installation will be successful.

You can close the terminal, WSL is now installed on your machine.



### Upgrade to WSL 2

By default WSL is in its first version, **1**.
Let's upgrade it to it's **version 2**.
For this, we need to update it's kernel, follow this [link](https://aka.ms/wsl2kernel). Click on the offered link to download the update package. When the download is over, please open the program downloaded. Click on **next** then **finish**.

Click on **Start** then type *cmd*, open the **Command Prompt**
You can list all the WSL installed on your machine with the command

```wsl -l -v```

You should see the Ubuntu that you have installed before.

Let's upgrade it to the version 2, run the following command

```wsl --set-version Ubuntu 2```

A message will appear telling you that the conversion is in progress and that it will take a few minutes.
