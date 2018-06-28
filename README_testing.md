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


## Testing in container using Docker

```
docker run --rm -it centos-source:Dockerfile
```

```
[root@80fe6dc2536a lrose-blaze-20180627.src]# /usr/local/lrose/bin/HawkEye     
QStandardPaths: XDG_RUNTIME_DIR not set, defaulting to '/tmp/runtime-root'
qt.qpa.screen: QXcbConnection: Could not connect to display 
Could not connect to any X display.
[root@80fe6dc2536a lrose-blaze-20180627.src]# ls /usr/local/lrose/share/
doc  hdf5_examples  info  man  udunits
[root@80fe6dc2536a lrose-blaze-20180627.src]# history
    1  which wget
    2  wget https://github.com/NCAR/lrose-alpha/releases/download/lrose-blaze-20180627.src.tgz
    3  wget https://github.com/NCAR/lrose-alpha/releases/download/lrose-blaze-20180627/lrose-blaze-20180627.src.tgz
    4  ls
    5  more Dockerfile
    6  tar xvfz lrose-blaze-20180627.src.tgz 
    7  ls
    8  cd lrose-blaze-20180627.src
    9  ls
   10  more build_src_release.py 
   11  ls
   12  more README.md
   13  ls
   14  build_src_release.py --help
   15  build_src_release.py -help
   16  .build_src_release.py --help
   17  ls share
   18  ls share/color_scales/
   19  ls
   20  ls build
   21  more README.md
   22  ls
   23  more build_src_release.py 
   24  ls
   25  ./build_src_release.py 
   26  ls -lrt /usr/local/lrose
   27  /usr/local/lrose/bin/RadxPrint -h
   28  /usr/local/lrose/bin/HawkEye
   29  ls /usr/local/lrose/share/
   30  history
   ```
