# Action Kernel Rebaser
Start your first kernel development by rebasing your oem release kernel using Github Action.

# Inputs
* `KERNEL_VERSION`: Check your Makefile in kernel's root directory to see which version your kernel has.
* `CAF_TAG`: Go to CAF/CLO's repository, pick your device's tag.
* `COMMIT_SHA`: Pick where point in git commit history you want your kernel use as base.
* `OEM_KERNEL_TREE`: Your OEM release kernel source URL, untouched yet.
* `OEM_KERNEL_BRANCH`: Just your OEM release kernel source branch, again, untouched yet.
* `GIT_CONFIG_NAME`: Your Github Name.
* `GIT_CONFIG_EMAIL`: Your Github Email.

# Notes:
* To better know which CAF_TAG you should use, just go to CAF/CLO's Telegram Release Channel, search your SoC's name, and you'll see bunch of tag for your SoC.
* To better know which COMMIT_SHA you should use, check your OEM Kernel release commit history, look for the most recent commit before OEM commits, look for the same commit in CAF/CLO's (of your chosen kernel version and caf tag) repository commit, use that commid ID.
* If, and only if, your OEM Kernel release do not have commit history, you can try to use best-caf-kernel.py from LineageOS' scripts, to see which caf tag to use.
* Rebased Kernel were uploaded as tar.gz in release instead of pushing it as Repository, download and push it on your own.
