My personal UNIX working environment manifest for auto-deployment

Installing Repo
---------------

Repo is a tool that makes it easier to work with Git in the context of Android.
For more information about Repo, see [Developing](http://source.android.com/source/developing.html) section.

To install Repo:

* Make sure you have a bin/ directory in your home directory, and that it is included in your path:
  ```
  $ mkdir ~/bin
  $ export PATH=~/bin:$PATH
  ```

* Download the Repo tool and ensure that it is executable:
  ```
  $ curl  http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
  $ chmod a+x ~/bin/repo
  ```

Initializing a Repo client
--------------------------

After installing Repo, set up your client to access the android source repository:

* Create an empty directory to hold your working files. If you're using MacOS, this has to be on a case-sensitive filesystem. Give it any name you like:
  ```
  $ mkdir -p WORKING_DIRECTORY
  $ cd WORKING_DIRECTORY
  ```

* Run repo init to bring down the latest version of Repo with all its most recent bug fixes:
  ```
  $ repo init -u https://github.com/chenkaie/manifest-unix-env-deploy.git
  ```
Downloading the Source Tree
-----------------------------------

* To pull down the source tree to your working directory from the repositories as specified in the default manifest, run
  ```
  $ repo sync
  ```

