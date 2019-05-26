---
title: "Modal editing, the superior way of editing"
date: 2019-05-26T15:29:34+02:00
draft: false
language: en
tags:
- vim
- emacs
---

<center>![Vim
logo](https://lcom.static.linuxfound.org/images/stories/vim-logo.jpg)</center>

Well ok, I might have exagerated. I actually don't care what text
editor you use, just use the one you feel most comfortable with.  What
I really want to transmit with this text is that there are more ways
to edit text than *the traditional way,* the one most people use when
they learn how to use a computer.

I don't want to make anyone feel bad with this post. This is not an
editor war, neither about how you have to edit text. If you're reading
this it's because you're interested in learning about a concept that's
not common or you want to know what all this is about.

This is also not a tutorial about how to use *Vim*, I want to focus on
what implies using a modal text editor and in the *why*, *how* and
*how not*. I'm trying to give some guidance, resources and ideas so
that if you're interested in learning about it you have some
preconceived knowledge about modal editing's purpouse.

<center>![Vim editing
demo](/img/posts/modal-editing/vim-demonstration.gif)</center>

## The philosophy

Modal editing was born out of the necessities programmers had back
when the only way of interacting with the computer was through the
*command line interface*. There was no mouse you could use because
there even weren't any graphical interfaces you could scroll
through. This is when out of these needs people started to find a way
to optimize how they edited text through the keyboard.

So well, what's the philosophy behind modal editing? We can summarize
it in a few lines, but I'll probably forget something.

- Optimize the use of the keyboard.
- Minimize the distance our hand travels from what we call the *home
row*. This is our keyboard's main row, in which our hand normally
rests.
- Make use of modes (this is where *modal editing* comes from), that
change the behaviour of the different keys in our keyboard so we can
make use of the specific functions our text editor gives us.
- Understand that, either writing or programming, we actually spend
more time editing text than adding it, and for that reason the
optimization of it should be prioritized.
- Reduce the amount of repetitive actions we perform. For this, modal
editors give us *macros*, that really facilitates this matter.

The main caracteristic that defines the philosophy is *modes*. Let's
say modes are a way to differentiate introducing text from the rest of
functions we make use of to edit text. If we take a look at *Microsoft
Word*, for example, we can see that we have a main way to interact
with text, while we also have some shortcuts to act on our text. We
can select text with our mouse, move around with the arrow keys... All
this adds up to an intuitive way to edit text, but, is it really an
efficient way to do it?

### How do the controls we all know translate to a modal editor?

At first glance, modal editing controls may appear unintuitive or just
weird. Modal editors make us of mnemonics to try to make it intuitive
for us to learn the commands. Sounds doubtful, but believe me when I
say that it's just about undertanding the logic behind it, after that,
everything in modal editing follows the same principles.

I'm going to make use of *Vim* to explain my point, just because I
think the sucessor of an edit born in the 70s that's still relevant is
a good enought reason for me to have it as a reference. And yes, *Vi*
wasn't the first modal editor, but it's the one which got popular to
the point that a lot of people still use it today.

<center>![Vim mode
demonstration](/img/posts/modal-editing/vim-modes.gif)</center>

*Vim* (Vi IMproved) tries to take *Vi* and improve it. Mainly they are
similar, but I think it's weird to talk about *Vi* having *Vim*
available to us.

This are the modes that *Vim* has available to us:

- `Normal mode`: This mode is the main one, in normal mode we can move
around the document, search for text, find characters, delete text or
tell our editor which part of our text we want to modify... This mode
makes use of mnemonics to assign functions to the alphanumeric keys of
our keyboard, for example `d` for `delete`, `p` for `paste`, etc. To
move around the document we can use `h` to move left, `j` to move
down, `k` to move up and `l` to move right. Again, this may some weird
but we can move around our document without even reaching for the
arrows.
- `Insert mode`: Every person know this mode, it's the one every
modern text editor uses, where you can just type alphanumeric
characters and they will appear on the screen. We still have some
shortcuts available to us, but the main purpouse of this mode is just
introducing text.
- `Visual mode`: This mode exist just for text selection, we still
have the `normal mode` movement keys to move around and select
text. This is a really powerful mode as we can make use of the
searching fuctionality to move our cursor, and so select whats between
our starting point and our actual cursors position.
- `Visual block mode`: This mode is exactly like the last one, but we
can now select text in blocks, this is really useful if we want to
select text separated by columns, like in data tables.
- `Replace mode`: I've actually never used this mode, it works as when
you let find your insert key is turned on in *Microsoft Word* and just
replaces text as you write. It doesn't offer much as you probably
prefer to use normal mode editing functions to replace text.

There are more modes to *Vim*, like `command mode`, `^X mode` or `Ex
command mode`, but they are much more advanced and I think it's better
not to think about them when you're first learning *Vim*.

## The language

I've been talking about modal editing for some time, but I can't
forget to talk about what makes modal editing actually be useful and
intuitive. I'm talking about the *Vim* language, it's what *Vim* uses
for it's *commands* or *shortcuts*. As I said before `insert mode` is
the one we use to introduce text, but to make use of the magic that
*Vim* is known for we have to take a look at `normal mode`. Every
*command* is formed by three parts: a *verb*, a *subject* and
optionally a *movement*. This makes the automation and repetition of
this *commands* so easy. You can now use *macros* around this
*commands*. Let's take a look at some examples.

<center>![Vim command
structure](/img/posts/modal-editing/vim-words.png)</center>

How is it possible to memorized every single *Vim* command, how can
we, for example, delete two words? Well, we want to **delete**,
**two**, **words**. We have *delete* as a verb, *word* as a subject
and *two* as a movement. It's so easy as positioning our cursor behind
the first word we want to delete, and in `normal mode` type `d2w`. Is
it really that easy? what does that mean? Literally *delete two
words*. That's how vim commands work. How can we change a word? `cw`
(*Change Word*), delete an entire paragraph? `dip` (*Delete Inside
Paragraph*), change the content of a quoted text? `ci"` (*Change
Inside "*). We could spend the entire day listing example, but you get
the point.

## Why make use of modal editing?

Even though behind the philosophy there is no focus in health, it's
inherent that moving your hand and specially your wrist less, makes
for a healthier typing experience. There is no real scientific study
behind it but it's well known that it can help with wrist pains
derived from having to move your hand so much between your keyboard
and the arrow keys or the mouse.

Speed is one of it's main advantages. Once you learn the basic
movement keys and the purpouse of the several modes available to us,
every action is at most at two keys of distance of our fingers.

Learning to use modal editing is tedious, you have to change your way
of thinking, a bit like when you learn to program, but when you start
to have some agility it's easy to see the benefits. In my case, I
started learning *Vim* because I got interested in improving my speed,
every travel to they mouse or arrow keys feels cumbersome and made me
feel clumsy.

If I'm honest with you, I don't think learning it is difficult at all,
once you learn the main concepts it's all about logic to keep making
sense of the commands.

## How not to learn about modal editing?

I've said *Vim* is not hard, yes, but it requieres a learning
period. You shouldn't force yourself to use it at work or in a project
that requires to be productive, at least give it some time before you
start depending on it.

<center>![Learning
curves](https://proxy.duckduckgo.com/iu/?u=http%3A%2F%2Fergoemacs.org%2Femacs%2Fi%2Femacs_learning_curves.png&f=1)</center>

You don't actually have to use `vim` to learn modal editing, every
decent and modernt text editor has some kind of plugin to get modal
editing working for it. *Visual Studio Code* has one for it, start
using that and maybe move towards *Vim* progressively.

## How to actually learn about modal editing?

If you're inclined to learn *Vim* you can make use of `vimtutor` in
the console, which is a really good resource that guides you through
vim while you learn about it's controls and commands. `vimtutor` comes
installed with `vim` and if you're using any *linux* distro it's
probably available to you.

If you end up deciding to use `emacs`, which by default is not a modal
editor, it's `evil` packages might be helpful to you. They turn
*Emacs* into a full fledged modal editor based on *Vim*
controls. *Emacs'* `evil` packages have `evil-tutor`, which is just a
translation of `vimtutor` that comes with `evil`.

As I said before, any decent known text editor has a plugin that
implements modal editing to it. Make use of that plugin. I don't have
a tutorial for each of them but you can start to try writing small
texts, twitts, maybe emails or whatever motivates you to keep
learning.

You can also play, yes, play! There are some simple games that make
use of *Vim* movement keys and several others to try and make you
comfortable moving around with them. There are lots of them, I
recommend you [this one.](https://vim-adventures.com/).

One of the resources that helped me most was the
[ThoughtBot](https://www.youtube.com/user/ThoughtbotVideo/) youtube
channel, which normally upload videos of the talks they host, where
some of them are about *Vim* and *Emacs*. The ones I recommend the
most are [*"learning Vim in a
week"*](https://www.youtube.com/watch?v=_NUO4JEtkDw) and [*"How I
Learned to Stop Worrying and Love
Emacs"*](https://www.youtube.com/watch?v=JWD1Fpdd4Pc).

This [other
text](https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118)
comes into detail about how you can make use of `vim` beyond what most
people know about it, in a really advanced way.

If you end up using *Vim* or *Emacs*, the posibilities this text
editors offer us are inmense, they introduce a programming language
interpreter that let us expand the functionalities of this editors
with the only limit of our imagination. It's also because of this that
we can feel intimidated coming into this editors, they have to much to
offer but also so much to learn, I recommend you learn the basics and
learn little by little how you can improve your speed and
functionalities that could come in handy to you.

## Conclusion

This is the end of my text, if you were coming for an answer on how to
get out of *Vim* it was `:q`. With this post I wanted to abstract
myself from the technical questions. It's possible that in the future
I'll write something more technical, but there are already tons of
resources on how to learn *Vim* so you will probably have to wait.

## Links of interest

- [2019 text editor popularity survey by Stack
  Overflow.](https://insights.stackoverflow.com/survey/2019#development-environments-and-tools)
- [The Wikipedia page of Vi, the predecessor of
  Vim](https://en.wikipedia.org/wiki/Vi)
- [Vim, **the** modal text editor.](https://www.vim.org/)
- [Link to my emacs config file, adapted for modal
  editing.](https://github.com/eli-rodriguezperez/dotfiles/blob/master/init.el)
- [Link to my vim config
  file](https://github.com/eli-rodriguezperez/dotfiles/blob/master/.config/nvim/init.vim)
- [Vim-adventures, a game that makes use of vim controls to teach you
  vim.](https://vim-adventures.com/)
- [A post that tries to teach us about the advanced ways we can make
  use of vim.](https://stackoverflow.com/questions/1218390/what-is-your-most-productive-shortcut-with-vim/1220118#1220118)
