---
title: "My current keyboard layout"
date: 2019-06-10T21:09:56+02:00
draft: false
language: en
images:
tags:
  - vim
  - keyboard
  - efficiency
---

As you may have realized based on my previous post, I'm really into improving my
efficiency when it comes to programming and using the keyboard in general.
That's why I got into Vim and that's why now I'm into keyboard stuff.

When I was little I remember my dad teaching me to touch type, we didn't even
have a computer at home, but my dad thought it was important for me to learn to use
a keyboard and brought an old typewriter home. He had an old book that I used to
practice touch typing and I remember how I spent hours typing repeatedly the
same blocks of text. Eventually the typewriter went away and I got to use my dads
work laptop, in which I (sometimes) cheated by copy pasting the exercises.

I'm so grateful that I got to learn to touch type so young, I can't recall
exactly, but it was around the age of 8. I got a base in touch typing, I could
type quite fast for my age and I never got to develop bad habits.

## What has changed since then

Fast forward to today and I'm a programmer, the keyboard is my main tool for
work and coincidentally gaming is also a hobby of mine. I spend **a lot** of time
in front of a computer. If you're interested I average 80 wpm, it's not
ultrafast, but I think it's good enough that I don't feel like it's a bottleneck.

I have changed quite a lot of things whenever I felt like something made me
slow in regards to typing. First it was Vim, or modal editing, that made me
realize how awesome it was to not have to move your hand away from the keyboard
so much.

Then when you spend hours coding in the default spanish keyboard layout,
you start to realize how it never was intended to be used for coding.
For some reason you have the most useful coding characters behind third layer
modifiers, and at the same time you have `ñ` and `ç` as no mod characters
instead of having them behind AltGr shortcuts. I could even argue that accented
vowels are occupying the precious spot of the most used characters in
programming. Needless to say I moved away from that layout, I'm now using the US
International layout, which has the standart US layout but you can also get
special latin characters with AltGr combinations. So I still have `ñ` behind
`AltGr + n` and accented vowels behind `AltGr + vowel`.

After this changes I got super comfortable with my typing experience inside my
code editor of choice. But there was still a big problem, when I was out of Vim,
say in the web browser sending an email or when I found myself in a word
processor like Libre Office.

## Where are my Vim bindings!

No more waiting, I'm going to go straight to the point of this post. How did I
end up being at peace (not really) with my keyboard use outside of Vim? Behold
my current layout:

### Main layer

<center>![Main layer](/img/posts/keyboard-layout/keyboard-layout-0.png)</center>

This is a blueprint of my keyboard configuration. The keyboard I'm using is a
TADA68, which is a 65% keyboard. I don't even make use of the arrows or the
first column on the right side of the keyboard. The important part of my
keyboard is that you can flash whatever configuration you want into the board.
And so when you take it anywhere, say work or when traveling, you keep the key
configuration as you wanted when you flashed it. This is made possible by
[QMK](https://github.com/qmk/qmk_firmware/), but if you don't have a QMK
compatible keyboard you still can change things up by software.

Let me go into the *why's* of my configuration:

- I used to have the *Esc* key where the *Caps Lock* key is, but now that I have
    the possibility, I have both *Ctrl* and *Esc* key in the *Caps Lock*. The key
    works as *Esc* when you tap it and as *Ctrl* when you hold it. This is
    possible thanks to *Tap Dance*, which is a concept introduced by the QMK
    firmware configuration.

- Because I now have the *Esc* and *Ctrl* in a single key I'm free to put back
    the *Grave/Tilde* key back on top of *Tab*. I also make use of the *Ctrl*
    position to have access to the second layer which we will take a look at
    later.

- The main feature of this configuration is the *Space* key. Which acts both as
    a *Space* when tapped and as a layer 1 access key when held. Layer 1 gives us
    access to some keys that enable us to not have to move our hand away from
    the main row while having access to every single key you can find in a full
    size keyboard, numpad included.

### First layer

<center>![First layer](/img/posts/keyboard-layout/keyboard-layout-1.png)</center>

I don't have every key configured into this layout, just the ones I use the
most. There are also some keys with no resoning behind them besides being in
convenient positions. The *whys* to this layer:

- I have *hjkl* as arrow keys, with this I have Vim style movement keys in every
    single place text input is expected at.

- As in Vim, *b* and *e* work as word wise motions backwards and forwards.

- The *y* key copies, acting as `Ctrl + Ins` which also works for the console
    and Emacs, unlike `Ctrl + C`. And on the contrary the *p* key pastes, acting
    as `Shift + Ins`.

- Finally we have *Home* and *End* keys in intuitive positions, also an
    alternative *Enter* key close to my index finger. The *Function* keys are
    accessible through the numbers now.

### Second layer

<center>![Second layer](/img/posts/keyboard-layout/keyboard-layout-2.png)</center>

This layer is just for convenience, but has a couple of interesting uses.

- Without moving my hand I have access to a numpad, only inconvenience is that
    is not ortholinear, but maybe will be soon :eyes:.

- Now that my Caps Lock key doesn't actually act as intended, I have it mapped
    to `Layer2 + c`.

- I almost never use media keys but they're there, I suppose I'll have too look
    at the binding whenever I want to use it.

- Lastly I have a key to change my default layout to a gaming layout, that is
    one where I don't really want to have *Control* at *Caps Lock* and also have
    *Space* acting as normal. You'll have a screenshot below but I don't think
    it needs much explanation. I just activate it whenever I need it and change
    it back when I finished playing.

<center>![Gaming layer](/img/posts/keyboard-layout/keyboard-layout-3.png)</center>

## Conclusion

I went down to a 65% keyboard and it's been one of my biggest leaps in regards
to productivity. I can't recommend QMK firmware keyboards enough, they're so
awesome. I never knew I needed it and now I can't go back. The amount of
customization available to you is huge and everything is flashed into the
keyboard, no need for software after that, just take it anywhere.

As I said before, I'm really comfortable with this configuration and it really
has improved my productivity by a lot. But now I feel like there are a lot of
useless keys in my keyboard. And my question is, could I go even smaller?

## Links of interest

- [QMK firmware webpage.](https://qmk.fm/)
- [Mechanical Keyboards'
    subreddit](https://old.reddit.com/r/MechanicalKeyboards/)
