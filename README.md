# Basci dev environment setup for Mac
This is a setup process I like to use, doesn't make it the best environament but it works for me.

## Download iTerm2
I prefer this terminal over the standard one which comes with mac. But this is optional.<br>
[Download from here](https://www.iterm2.com/)

## Install Xcode
First thing you've gotta do is install Xcode.<br>
[Download from here](https://developer.apple.com/download/)


Useful links:<br>
[https://wiki.wxwidgets.org/Installing_Xcode](https://wiki.wxwidgets.org/Installing_Xcode)

### Install Xcode Command Line Tools
Open up a terminal window and type:<br>
```curl
xcode-select --install
```

<br>

If you see this: <br>
```curl
xcode-select: error: command line tools are already installed, use "Software Update" to install updates
```

<br>
You've most likely already got it installed.

If not a dialog box will popup prompting you to install the command line tools. Follow these promts to install.<br>
When the installation is complete run this:<br>
```curl
xcode-select -p
```
<br>

Which should have outputed something like:<br>
```
/Applications/Xcode.app/Contents/Developer```


## Install Homebrew
Homebrew is a very useful package manager.<br>
To install run this in a terminal window:<br>
```curl
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
<br>

Now we need to tell the system to use programs installed by Hombrew (in /usr/local/bin) rather than the OS default if it exists. We do this by adding /usr/local/bin to your $PATH environment variable:<br>
Run this command:<br>
```curl
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.bash_profile
```
<br>


After this has finished doing it's thing, run this command to check that it's been installed:<br>
```curl
brew doctor
```

<br>

#### Using brew
Now that brew is installed you can use this to install packages.<br>
Commands:<br>
```curl
brew install PACKAGE_NAME
```
<br>
Packages can be found at these places:<br>
- [Brew Formulas](http://formulae.brew.sh/)
- [Other Brew Formulas](http://brewformulas.org/)

```curl
brew update
```
 - this will update all your packages for you