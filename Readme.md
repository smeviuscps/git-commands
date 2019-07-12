# git-commands
## git-release

### What it does

This script helps you to fasten up your release, it is doing the following steps

 - get latest Tag from master
 - increment tag (patch, minor or major)
 - create releasebranch release/newTag if not exist, else its switching to it
 - execute git write changelog and save Release Message
 - iterate version in ext_emconf.php
 - commit with message
 - if option -f is set, release will also be finished and tag set

### Installation

Mac:
 - copy git-release file /usr/bin and make it executeable

Windows:
 - copy git-release file to C:\Users\Username\AppData\Local\Atlassian\SourceTree\git_local\mingw32\libexec\git-core and make sure this path is in $PATH environment variable

after this you should be able to type
```sh
$ git release -h
```
or
```sh
$ git-release -h
```

| Options | description |
| ------ | ------ |
| \-h | show help |
| \-\-minor | increment minor tag |
| \-\-major | increment major tag |
| \-e | specify path to ext_emconf.php ($PATHext_emconf.php) |
| \-f | finish release |
