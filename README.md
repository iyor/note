# notes
A command line utility simplifying the management of notes and note-taking in vim! 

Based on a script by [connermcd](https://github.com/connermcd/notes)

## Installation
Simply clone the repo and place a symlink to note manually in your path or run the install.sh script which will place a symlink to note in /usr/bin/local/.

## Usage
note is a simple way to structure notes with the command-line.

Begin by typing `note -i <course name> <path (optional)>`. This will initiate the base structure for a notes directory named `<course name>` at `<path>`. Should `<path>` be omitted, the notes directory will be created in the current working directory.

Start a new note-taking session (for example, at a new lecture) by giving the command `note -n`. This will create a new markdown file. Typing `note -no` will create a new note session and open it in vim in one fell swoop.

By typing `note -c` all note-taking sessions will be compiled and outputted into a pretty pdf file complete with boilerplate text, such as a title page and a table of contents.

It is possible to search for occurences of certain keywords with the command `note -s <pattern>`.

The default folder structure is 
```
notes_dir/
  |-images/
  |-assignments/
  |-misc/
  |-s1.md
  |-s2.md
  |-s3.md
  ...
```
where s*.md are the different note-taking sessions. Images, graphics and figures that are not easily translatable into markdown can be placed and referenced to in the images/ directory.

## Dependencies
note needs:
  * getopt (GNU version, not the outdated BSD version shipped with FreeBSD, OSX etc)
  * ack
  * pandoc
  * LaTex/basicTex

## Future Development
To satisfy more flexible needs each note directory will also contain a .note_conf file. This file will enable users to configure note to their own specific needs, including
* default text editor
* output style (font, margins, etc)
* default folder structure

This will be implemented should I ever feel I have too little to do.
