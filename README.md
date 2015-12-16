# styleguide [![Stories in Ready](https://badge.waffle.io/bvn-architecture/styleguide.png?label=ready&title=Ready)](http://waffle.io/bvn-architecture/styleguide)

This is the repository behind the BVN styleguide. It's job is to allow the whole world to see how we use our assets.

If you would like to make a contribution then there are two ways:

1. If it's a simple change, something like a typo, then you can just use the GitHub interface to submit a pull request.
2. If it's more complicated then follow the instructions below

##Installation
Most of the instructions below are for Windows. If you are lucky enough to be using a unix machine then you are probably smart enough to figure it out on your own.

###Get git & GitHub
* Install [Git-for-windows](https://git-scm.com/download/win)
* Install [Github desktop](https://desktop.github.com/)

###Cloning the project from GitHub
You need to get the project from GitHub before you can work locally:
* Open GitHub for desktop,
* Press the "+" sign at the top left,
* Select "clone",
* Pick the repository to work on and press clone,
* Select location on your computer to create the files, press OK.

###Installing the necessary files to run Jekyll
* Download and install Ruby [32bit](dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.0.0-p647.exe) or [64bit](dl.bintray.com/oneclick/rubyinstaller/rubyinstaller-2.0.0-p647-x64.exe). Tick "Add Ruby executables to your PATH"
* Download Ruby Dev Kit [32Bit](dl.bintray.com/oneclick/rubyinstaller/DevKit-mingw64-32-4.7.2-20130224-1151-sfx.exe) or [64bit](dl.bintray.com/oneclick/rubyinstaller/DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe). Extract at 'C:\RubyDevKit\'
* Move/copy 'gemfile' from cloned GitHub folder (styleguide) into 'C:\RubyDevKit'
* Open cmd.exe and run the following lines separately (NOTE: The software [Avast](https://www.avast.com/en-au/index) is know to have problems with installing gems, disable before installing Ruby gems.): 
```
    cd C:\RubyDevKit
    ruby dk.rb init
    ruby dk.rb install
    gem install jekyll
    gem install bundler
    gem install rdiscount
    bundle install
```
* Install Python v2.7.11 [32bit](https://www.python.org/ftp/python/2.7.11/python-2.7.11.msi) or [64bit](https://www.python.org/ftp/python/2.7.11/python-2.7.11.amd64.msi) At "Customize Python", click on 'Add python.exe to path' and choose 'Entire feature will be installed on local drive'
* Download [pip.py](https://bootstrap.pypa.io/get-pip.py) and move it into 'C:\Python27'.
* Open cmd.exe and run the following lines separately:
```
    cd C:\Python27
    python -m pip install Pygments
```
*Indept guide for troubleshooting: [Windows](http://jekyll-windows.juthilo.com/) [Mac and Linux](http://jekyllrb.com/docs/installation/)

##Editing files
Sublime Text 3 is an excellent editor for SVG, markdown and html, you can get the software at: http://www.sublimetext.com/3

##Known window problems
There are some compatibility issues with ruby and jekyll for windows operating systems. If you are running on Linux or Mac OS, ignore this stage.
* Reference file directories do not need any "../" indicating a move out of folder. It works as a local host in windows but will not work in GitHub.
* There are occasions where the GitHub gem would not be installed into ruby. Use 'Git Bash' as the command prompt.

##Testing server on local
To test your Jekyll files on you computer before syncing:
* Run line in GitBash: `bundle exec jekyll serve`
* Navigate in chrome or Firefox to: http://localhost:4000/styleguide/
* Adjust changes as above before pushing the changes

##Pushing and pulling changes on GitHub
Synchronising your files with GitHub will allow you to work on a project with multiple people and keep track of every change. Sync regulary to keep local files up tp date
* Press "Sync" in the top right to receive changes to files
* Commit a change to officially note the changes to Github: Insert a summary and press "Commit to ___"
* Press "Sync" in the top right to upload and receive files.

We use Waffle to prioritise issues, to see what we think needs to be worked on next [go to the board](https://waffle.io/bvn-architecture/styleguide)

[![Throughput Graph](https://graphs.waffle.io/bvn-architecture/styleguide/throughput.svg)](https://waffle.io/bvn-architecture/styleguide/metrics)
