# styleguide


[![Stories in Ready](https://badge.waffle.io/bvn-architecture/styleguide.png?label=ready&title=Ready)](http://waffle.io/bvn-architecture/styleguide)

[![Throughput Graph](https://graphs.waffle.io/bvn-architecture/styleguide/throughput.svg)](https://waffle.io/bvn-architecture/styleguide/metrics)


##Installation
###Installing the necessary files to run jekyll
* To install jekyll for windows: http://jekyll-windows.juthilo.com/
* http://jekyllrb.com/docs/installation/


1. Download and install [Ruby](https://cache.ruby-lang.org/pub/ruby/2.0/ruby-2.0.0-p647.tar.gz "Title"). (Tick "Add Ruby executables to your PATH")
2. Download Ruby Dev Kit [32Bit](dl.bintray.com/oneclick/rubyinstaller/DevKit-mingw64-32-4.7.2-20130224-1151-sfx.exe) or [64bit](dl.bintray.com/oneclick/rubyinstaller/DevKit-mingw64-64-4.7.2-20130224-1432-sfx.exe). Extract at 'C:\RubyDevKit\'
3. Open cmd.exe and run the following lines seperatley:
		'cd C:\RubyDevKit'
		'ruby dk.rb init'
		'ruby dk.rb install'
		'gem install jekyll'
		'gem install kramdown'
4. Install Python v2.7.11 [32bit](https://www.python.org/ftp/python/2.7.11/python-2.7.11.msi) or [64bit](https://www.python.org/ftp/python/2.7.11/python-2.7.11.amd64.msi) At "Customize Python", click on 'Add python.exe to path' and choose 'Entire feature will be installed on local drive'
5. Open cmd.exe and run the following lines seperatley:
		'cd C:\Python27'
		'python -m pip install Pygments'



###Git-Hub software required to participate
* Install Github desktop (Easy to use for beginers): https://desktop.github.com/
* Install Git-for-windows (better than windows CMD): https://git-for-windows.github.io/
* Jekyll for Github: https://help.github.com/articles/using-jekyll-with-pages/
* Pull files from Git-Hub

###This repository uses certain gems
* Install kramdown: *gem install kramdown*
* 

##Editing files
Subline Text 3 is an excellent editor for SVG, markdown and html, you can get the software at: http://www.sublimetext.com/3

##Known window problems
There are some compatibility issues with ruby and jekyll for windows operating systems. If you are running on Linux or Mac OS, ignore this stage.
* "Base URL" must be commended out in the file "config.yml". **Do not commit this change,** it will not work with 'Git-hub pages.' Simply untick "config.yml" or right click and discard changes before a commit.
* Refrence file directories do not need any "../" indicating a move out of folder. It works as a local host in windows but will not work in Git-hub.
* There are occasions where the 'git-hub gem' would not be installed into ruby. Use 'Git Bash' as the command prompt.

##Testing server on local
To test your jekyll files on you computer before syncing:
* Run line in GitBash: **bundle exec jekyll serve**
* Navigate in chrome or firefox to: http://localhost:4000
* Adjust changes as above before pushing the changes

##Syncing Git-Hub
You must receiving files from Git-Hub to work locally:
* Open git-hub for desktop,
* Press the "+" sign at the top left,
* Select "clone",
* Pick the repository to work on and press clone,
* Select location on your computer to create the files, press OK.

##Pushing and pulling changes on Git-Hub
Synicning your files with Git-Hub will allow you to work on a project with multiple people and keep track of every change. Sync regulary to keep local files up tp date
* Press "Sync" in the top right to receive changes to files
* Commit a change to officially note the changes to github: Insert a summary and press "Commit to ___"
* Press "Sync" in the top right to upload and receive files.
