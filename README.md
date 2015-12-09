# styleguide


[![Stories in Ready](https://badge.waffle.io/bvn-architecture/styleguide.png?label=ready&title=Ready)](http://waffle.io/bvn-architecture/styleguide)

[![Throughput Graph](https://graphs.waffle.io/bvn-architecture/styleguide/throughput.svg)](https://waffle.io/bvn-architecture/styleguide/metrics)



##Installation
* For an instalation guide on vanila jekyll: http://jekyllrb.com/docs/installation/
* Install kramdown: gem install kramdown
* For windows: http://jekyll-windows.juthilo.com/
* Install Github desktop: https://desktop.github.com/
* Install Git-for-windows (better than windows CMD): https://git-for-windows.github.io/
* Jekyll for Github: https://help.github.com/articles/using-jekyll-with-pages/

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
Synicning your files with Git-Hub will allow you to work on a project with multiple people and keep track of every change
* Open git-hub for desktop,
* Press the "+" sign at the top left,
* Select "clone",
* Pick the repository to work on and press clone,
* Select location on your computer to create the files, press OK.

##Pushing and pulling changes on Git-Hub
* Press "Sync" in the top right to receive changes to files
* Commit a change to officially note the changes to github: Insert a summary and press "Commit to ___"
* Press "Sync" in the top right to upload and receive files.
