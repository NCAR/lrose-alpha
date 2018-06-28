## Testing on a MacBook Air

Install rose-blaze
```
    1  which ruby
    2  which curl
    3  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
    4  which wget
    5  brew install wget
    6  which wget
    7  cd Downloads
    8  pwd
    9  wget https://github.com/NCAR/lrose-alpha/releases/download/lrose-blaze-20180627/lrose-blaze.rb
   10  ls
   11  brew install --verbose --compile-from-source ./lrose-blaze.rb
   12  history
   13   brew cask install xquartz	# needed to install quartz
   14  brew install --verbose --compile-from-source ./lrose-blaze.rb 	# needed to edit the url in the .rb file
   15  brew install --verbose  ./lrose-blaze.rb
   16  brew install --verbose --compile-from-source ./lrose-blaze.rb
   17  ls /usr/local/lrose	# No such file or directory
   18  which RadxPrint	# /usr/local/bin/RadxPrint
   19  RadxPrint -h 		# help info printed in terminal
   20  HawkEye   		#  GUI displays
```

```
macbook-air:Downloads candyoh$ brew install --verbose --compile-from-source ./lrose-blaze.rb
lrose-blaze: XQuartz 2.7.11 (or newer) is required to install this formula. X11Requirement unsatisfied!
You can install with Homebrew-Cask:
 brew cask install xquartz
You can download from:
 https://xquartz.macosforge.org
Error: An unsatisfied requirement failed this build.
```

#### I had to change the url for the source to lrose-alpha  from lrose-core in the .rb file
