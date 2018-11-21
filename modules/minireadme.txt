miniscript.dll r1
limpid - limpid@w2s.com
http://www.v-active.com/litestep/
----------------------------

i just thought of this and coded it up real quick. its a loadmodule that will
let you create 'miniscripts' in your steprc. no, these arent really cool
scripts like your probably thinking. there not really scripts at all, just
a series of ls commands :). useful if you want to do more than one thing off
of one event i guess.

to load it, put this in your step.rc:
LoadModule x:\path\to\miniscript.dll

and to create scripts do this in your step.rc:

*miniscript start "example"			<<start of a miniscript named 'example'
	*miniscript "!About"			<<first command...
	*miniscript "notepad c:\config.sys"	<<second command..
	*miniscript "whatever"			<<you get the idea... up to 10 commands..
*miniscript end					<<end of script.

this will create one miniscript named 'example' (you can have up to 15 total miniscripts in your steprc)

syntax to run a miniscript:
!miniscript scriptname

now, when you run '!miniscript example' it will execute the commands defined in that script.
this is just an example - i couldnt think of anything more useless

the limit of commands in each miniscript is 10
the limit of total miniscripts is 15

for some reason !easteregg likes to crash ls.... not my fault
also on the weird side, !run will halt your script until the run box is closed.
this isnt my fault, its something with lsapi.

maybe if i added the ability to pass variables to scripts and some other stuff it would be cool?

is this one of the most useless mods youve seen? maybe, but if you find a good use for it please tell me :)

for some strange reason whenever i hear 'miniscript' i tend to think of those
little mini cinnamon rolls (and they sure are mini) you get at burger king.
because of this, after writing this readme, i am very hungry.