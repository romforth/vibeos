VibeOS
======

Wouldn't it be nice to just do a git pull and then run make to create your
very own personalized linux distro? This is my attempt at creating such a
thing. I'll count NetBSD, Gentoo, Gobolinux and Nix as the distros that will
shape the outcome of what this distro might eventually look like.

Rather than do the hard work, I've tried to take the easy way out and see
how far vibe coding it as a Perl script will get me. For lack of a better
name (trust me, I asked ChatGPT for name suggestions as well), I'm calling
it VibeOS. Since I'm not thinking of this as a throwaway script, I'm not
sure if this can be literally called vibe coding but I'll make do for now.

Rationale
=========

There are a zillion linux distros out there already. So why another one?
Well, my ChatGPT based research tells me that nothing meets my particlar
requirements and since vibe coding is all the rage now I've decided to dip
my toes into it to see how it pans out. My earlier experiment with "vibing"
(see https://github.com/romforth/slop16) didn't end very well (to put it
mildly) but then, hope springs eternal.

So, what then are my (fairly modest) requirements that ChatGPT thinks are not
quite met by any of the existing distros? Let me list them here for the record:

I'd like to have a distro which is:
1. small(ish)
2. uses git to keep track of the code for the packages used in it
3. uses git tags for version control of those packages
4. can be rebuilt by running make
5. uses zig cc to build all of the stuff that needs C (optional?)

NetBSD might be perfect but I've had trouble with missing drivers that are
seemingly only available on Linux (add printer support as well). Gentoo almost
fits the bill but I'm trying to see if rebuilding the entire thing by running
`make` is workable and I also want to explore a more Gobolinux type file system
layout. I love the declarative style of Nix but I hate the grotesquely bloated
monstrosity ISOs I end up with. I'm not sure if I can solve all (or even any)
of these issues but I'm hoping that our AI overlords can make it a much easier
experience by making it trivial to experiment and prototype my way into
something workable/usable.

For some of my older experiments with trying to find a small distro for an
ancient laptop, see https://ces.mataro.blog/blog/distro_hoppingmd/ and for
a "note to self" to build an extremely minimal kernel+initrd, see
https://github.com/romforth/tlb about which I've blogged at
https://ces.mataroa.blog/blog/tlb-tinyconfig-linux-build/

I may lose interest in this when the nitty-gritties of maintaining a distro
actually sets in, but for now, this is just a lark with ChatGPT doing most
of the leg work so I don't mind the small mods that I will need to maintain.
If I end up debugging most of the code, then it really becomes a throwaway
script and I may just move on to something mainstream.

License
=======
Copyright (c) 2025 Charles Suresh <romforth@proton.me>
SPDX-License-Identifier: AGPL-3.0-only
Please see the LICENSE file for the Affero GPL 3.0 license details
