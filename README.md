# Introduction

EasyMotion provides a much simpler way to use some motions in vim. It
takes the `<number>` out of `<number>w` or `<number>f{char}` by
highlighting all possible choices and allowing you to press one key to
jump directly to the target.

When one of the available motions is triggered, all visible text
preceding or following the cursor is faded, and motion targets are
highlighted. (Customization by @laughinghan: instead of the 26 letters
in alphabetical order, my motion targets are the homerow keys from
left-to-right, then the same keys with Shift in reverse order, so even
if you mistype you'll end up near your intended destination.)

EasyMotion is triggered by one of the provided mappings.

# Important notes about the default bindings

**Note by @laughinghan: I've set `<Space>` as my default Leader key.**

**The default leader has been changed to `<Leader><Leader>` to avoid 
conflicts with other plugins you may have installed.** This can easily be 
changed back to pre-1.3 behavior by rebinding the leader in your vimrc:

	let g:EasyMotion_leader_key = '<Leader>'

All motions are now triggered with `<Leader><Leader>` by default, e.g.
`<Leader><Leader>t`, `<Leader><Leader>gE`.

## Usage example

Type `<Leader><Leader>w` to trigger the word motion `w`. When the motion is
triggered, the text is updated (no braces are actually added, the text
is highlighted in red by default):

	<cursor>Lorem {a}psum {b}olor {c}it {d}met.

Press `c` to jump to the beginning of the word "sit":

	Lorem ipsum dolor <cursor>sit amet.

Similarly, if you're looking for an "o", you can use the `f` motion.
Type `<Leader><Leader>fo`, and all "o" characters are highlighted:

	<cursor>L{a}rem ipsum d{b}l{c}r sit amet.

Press `b` to jump to the second "o":

	Lorem ipsum d<cursor>olor sit amet.

Jeffrey Way of Nettuts+ has also [written
a tutorial](http://net.tutsplus.com/tutorials/other/vim-essential-plugin-easymotion/)
about EasyMotion.

## Two Character Combos

Two character combo support was added by Yan Pritzker (@skwp). This changes the
default behavior of EasyMotion to highlight everything with a two-key combo. This
makes it possible to immediately reach any location without going through multiple
rounds of typing and looking, making usage much faster. This change is currently
available only on the @skwp fork of easy motion. It is not currently possible 
to disable this behavior.

## Animated demonstration

![Animated demonstration](http://oi54.tinypic.com/2yysefm.jpg)
