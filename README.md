Here are some firmware files that I've built with my extensions.

So far these all have double-tap-and-hold auto-repeat. It's
variable speed: these ones repeat at double the speed you tapped.
They work with sequences of up to eight chords as well: write the
sequence, then press and hold the first chord again.

The other extension that I've written is to send the chord when
you release its first key, rather than waiting until all keys have
been released. This is great for fingerspelling and navigation,
since it allows you to hold the common part of the chord and just
tap the keys that change. But a few people have had problems with
this so in addition to the "1up" versions I've also built the
standard "0down" ones.

----

I added *UNTESTED* firmware builds for the SOFT/HRUF Splitography.
I didn't feel like back-porting my extensions to the old version
of QMK that the splito code uses, so I copied the keyboard code
into my current QMK, added a `LAYOUT()` for the key matrix, and
defined `BOOTLOADER halfkay` instead of manually defining the
`BOOTLOADER_SIZE`. Hopefully neither of those are dangerous things
to do but I don't actually know what I'm doing...

----

The Uni builds are untested but they're current code so I didn't
have to do any tweaks: presumably they should be fine.

----

The Georgi has two thumb positions. Your home position can be with
your thumbs out (spread more away from your hand) or in (tucked
under your hand). So far I've only built the thumbs-out one since
that's my preference: I'll get around to building the others
soon-ish.

----

I'm also planning to build firmwares for other QMK-based hobbyist
steno boards as I get around to it, and can find people with those
boards to test them...
