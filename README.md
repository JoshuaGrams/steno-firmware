I've made two extensions to the QMK steno code.

One sends the chord when you release its first key, allowing you
to hold down common keys in between chords. So you can (for
instance) fingerspell by holding down `*` and tapping the letters
with the left hand. Add `#define STENO_1UP` to your `config.h` to
enable this feature.

The other is auto-repeat: double-tap and hold a chord, and it'll
repeat (currently) 4x as fast as your double-tap (currently capped
at 50 chords per second). You can also repeat sequences up to
(currently) 8 chords long. Write the sequence, then press and hold
the first chord again. For instance, write `SUD/-PB/HREU`, then
hold `SUD` to repeat "suddenly". For multi-chord outlines you have
to write the chords at an even pace: if you hesitate or speed up
too much it'll break the sequence.  Add `#define STENO_REPEAT` to
your `config.h` to enable this feature.

----

I have now built firmware for all four QMK-based hobbyist steno
boards. The EcoSteno firmware is still untested but the others
seem to work. The TinyMod doesn't use QMK, so porting it to that
would be a whole other project.


Georgi
------

This is my daily driver, so I'm using the `out-1up-repeat`
variant, and can confirm that it works. Not sure I've tried all
seven (!) other variants, but they should be fine.

These should be basically the same version as the 1.1 "ClayM"
firmware from the gBoards page.

The Georgi has two configurations for the thumb home position
between the vowel keys: thumbs spread `out` or thumbs tucked `in`.


SOFT/HRUF Splitography
----------------------

Aerick checked the `1up-repeat` version briefly and said it seemed
to work.


The Uni
-------

Peter tried out the repeat (and helped me squash a bug), so these
seem to work now.


EcoSteno
--------

These built without errors but haven't been tested.


TinyMod
-------

The TinyMod has custom firmware that is *not* based on QMK: I may
port my extensions over at some point, but don't hold your
breath...

I do own a StenoMod hinge, and I originally wrote these extensions
as a full [custom
firmware](https://github.com/JoshuaGrams/paper-steno/blob/master/paper-steno.ino)
for that. So if you own a StenoMod (they've been discontinued for
several years), grab the Arduino IDE and tell it to build/upload
the linked `.ino` file.
