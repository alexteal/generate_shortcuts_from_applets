# generate_shortcuts_from_applets

So the name is backwards, but the idea still works.

## Description

This script will generate a \*.app with the same name as the shortcut it
emulates. It pulls a list of all Apple Shortcuts from your library, then
links them as a bash script inside of an applet. It then links this directory
of applets to your ~/Applications/, giving the spotlight index engine access to
the names of the files.

## Usage

```bash
./generate-shortcuts [-h help] [-d directory for applets]
./generate-shortcuts -d ~/applets
```

Since Spotlight's engine ignores anything with a '.' prefix, it's not a great
idea to name your directory with a '.'.

DON'T

```bash
./generate-shortcuts -d ~/.applets
```

DO

```bash
./generate-shortcuts -d ~/applets
```

## why did i make this?

Because Alfred (the greatest Spotlight replacement) allows you to run
applets quickly. I didn't have a good way of porting shortcuts over to my mac,
so this was the best worst way of making it work.
