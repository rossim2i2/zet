# Git Repo on a USB Stick

After months of trying and failing, I finally had the time to really
look into and test the ability to create a git repository on a USB
drive, where I can store private information I do not want on
Github.com.

While I linked to the article the eventually helped me the most, I want
to memorialize this process in this zet for future reference, in the
event the site is taken down or the link no longer works.

First off, you need to mount the USB drive though the VM. I wrote a
script to automate this, which can be found below.

With the USB mounted, for this example, at /media/usb, create a bear
repo.

```bash
cd /media/usb
mkdir /media/usb/foo
git init --bare /media/usb/foo
```

Now that the repository is created on the USB drive, the repo can be
cloned.

```bash
git clone /media/usb/foo
```

That is it. From here you can create any additional files, add them to
the repo, commit them to the repo and push them to the repo.

* [Original Website]
  (https://en.wikibooks.org/wiki/Git/Repository_on_a_USB_stick)
* [20220427150546](/20220427150546/) How to Mount a USB Drive via Ubuntu VM
* [20210503112220](/20210503112220/) Git Notes
* [20210723182348](/20210723182348/) Seven Rules of a Great Git Commit Message
* [20220325124245](/20220325124245/) Switch Local Git Repos to use SSH

    #linux #localrepo #barerepo #usb #virtualmachine #vm
