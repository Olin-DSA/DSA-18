# Git Setup

### Forking the DSA-18 Repository
To set up your DSA repository, first fork `Olin-DSA/DSA-18`, which you can find [here](https://github.com/Olin-DSA/DSA-18).  Then clone your forked repository to your machine.

```
cd some_directory # wherever you want to put the DSA-18 repo
git clone https://github.com/YOUR_GIT_USERNAME/DSA-18.git
```

### Adding a Remote Repository 
In order to pull any updates that we make to the original DSA-18 repository down to your own local copy, you need to link `Olin-DSA/DSA-18` as a remote.  When you clone a git repo, the remote **origin** is created for you automatically and links to the on-server repository that you cloned.  You can also add other remotes to push to or pull from using `git remote add remoteName serverURL`.  In this case we want to configure a new remote with the name **upstream** and the server URL https://github.com/Olin-DSA/DSA-18.git. Use one of the following commands to add the upstream remove (if you're not sure which one to use, use the first one).

```
git remote add upstream https://github.com/Olin-DSA/DSA-18.git # if you are using HTTPS
git remote add upstream git@github.com:Olin-DSA/DSA-18.git # if you are using SSH.
```

`git remote -v` will list all of your configured remote names as well as the server URLs that they are linked to, so you can use this to check that you successfully added the `Olin-DSA/DSA-18` repository as **upstream**. Your terminal output should look like this:

```
$ git remote -v
origin	https://github.com/gitusername/DSA-18.git (fetch)
origin	https://github.com/gitusername/DSA-18.git (push)
upstream	https://github.com/Olin-DSA/DSA-18.git (fetch)
upstream	https://github.com/Olin-DSA/DSA-18.git (push)

```

### Updating DSA-18
Now that the remote has been added, you can pull updates from **upstream** at any time using `git pull upstream master` on top of pushing to and pulling from your forked repository (**origin**) as usual.
