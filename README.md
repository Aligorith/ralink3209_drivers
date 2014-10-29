ralink3209_drivers
==================

Patched version of Ralink Linux drivers, which works on the RT3290 wifi card on my HP Envy 17

Usage
-----
Checkout the "**x64_PanicFixesPorted**" branch. Do NOT use master, as this does not contain the patch/fixes needed to prevent
kernel panics when using this driver.

Notes
-----
* Some of the details below are a bit fuzzy, since it's been over a year since I actually compiled/used this code.
  Secondly, I had originally been intending to use this patch locally only, since I wasn't sure whether it would
  work at all. Thus, I didn't really care that much about carefully documenting where stuff came from - just
  getting my blasted wifi working was more important!

* The patch here is taken from a forum post for //another// Ralink card (IIRC, rt3573sta instead). It turns out that
  although these are different Ralink cards, they still share the same core Ralink driver code - the differences
  being that the different codebases include/exclude different side modules.
* I had to hand apply this patch to this repository, as the patched repository I got this off was a much older
  codebase which hadn't been updated for Linux 2.6+ support.

* It shouldn't be necessary to tweak any of the WPA_SUPPLICANT crap or any of the other config stuff, unless you really   
  want/need to do so for whatever reason. The base repository should already have all the stuff needed to get some sane
  defaults out of this thing.
