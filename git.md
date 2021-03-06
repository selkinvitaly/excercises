### differences with the previous commit
You just did `git pull`, saw a few files changed and would like to know exact details

```
# contents difference
git diff HEAD@{1}
git diff HEAD@{1} filename

# just the filenames
git diff --name-only HEAD@{1}
```

Get back one file

```
git checkout filename

#if `filename` matches branch name:
git checkout -- filename
```

Get back all to last commit

```
git reset --hard
```

### Not so Git stuff

# fun with `ls` colors

```
LSCOLORS="ExGxBxDxCxEgEdxbxgxcxd" ls -laG
```

Now you have control over `ls` colored output!

And colors, for reference:

a = black
b = red
c = green
d = brown
e = blue
f = magenta
g = cyan
h = grey
A = dark grey
B = bold red
C = bold green
D = yellow
E = bold blue
F = magenta
G = cyan
H = white
x = default

and order

directory
symbolic link
socket
pipe
executable
block device
character device
executable with setuid set
executable with setguid set
directory writable by others, with sticky bit
directory writable by others, without sticky bit


## Sublime Text

Make it available from the CLI:
```
sudo ln -s /Applications/Sublime\ Text.app/Contents/SharedSupport/bin/subl /usr/bin/sublime
```

now just `sublime .` being in the desired folder would do the trick.


Cmd-K Cmd-B - open/close sidebar (yes, it is a two-stroke command)

## Mocha

Installation is dead simple

```
sudo npm install mocha -g
```

Start using it right away:

```
echo -e "var assert=require('assert');\ndescribe('cool', function () {\n  function it ('things happen', function () {assert.equal(2+2, 4);})});" > test.js ; mocha test.js
```

Get reporters list `mocha --reporters` and use one of them like so:
```
mocha -R spec .
```

