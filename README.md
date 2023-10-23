# Project ReiDU
ReiDU is a toolkit used for development, distribution and installation of modifications for games based on the Infinity Engine.

Inspired by [WeiDU](https://weidu.org/) (the code also
[being available](https://github.com/WeiDUorg/weidu) on Github).


## Motivation
This project was inspired by WeiDU and is to eventually provide the same
functionalities that WeiDU does, but using different tools. Most notably,
WeiDU is using OCaml, Perl and C++ toolchain (indirectly, via Elkhound).

The name "ReiDU" is (rather obviously) meant to be visually similar
to "WeiDU", but there are three more reasons I had in mind for picking it:
* "Rust" + "WeiDU" --- self-explanatory.

  "I like WeiDU, but C++ is not my fav, so I'm creating ReiDU"
* "Rei" + DU (dialog utility) --- with "rei" here being kanji 礼,
  meaning "gratitude".

  "I'm grateful for WeiDU, so I'm creating ReiDU"
* Some may notice that "rei" is pronounced rē (with long "e"),
  making it "rēdu" --- which sounds similar to how "redo" may be pronounced
  if one has a heavy Polish accent (which I definitely don't have... right?).

  "I wanted to redo WeiDU, so I'm creating ReiDU".

One of the main problems with creating other tools for Infinity Engine is that
there are so many mods written in it already! Who has time to rewrite it all
to another project?

An obvious solution to that problem would to simply reimplement WeiDU using
another toolkit, but still sticking to the same language(s) it uses. That
was my first thought, but I quickly realised that it would mostly only benefits
its developers, if at all. But there is another way of maintaining
backwards-compatibility: translation.

It would also be nice if it reduced the number of tools one needed to use
in development, as WeiDU was usually used with other tools, such
as NearInfinity --- mainly because WeiDU doesn't really provide
a playground/exploratory mode, which may be fine for dialogue files,
but not so much for e.g. item or spell files.

ReiDU, therefore, needs:
1. A development tool with similar functionalities to WeiDU.
2. A translator from WeiDU language(s) to the new language(s) or DSL(s).
3. A playground/exploratory mode, perhaps similar to what is provided
   by [NearInfinity](https://github.com/Argent77/NearInfinity)


## Dependencies
ReiDU is to use the following:
1. [Rust](https://www.rust-lang.org/) --- for the more computation-heavy parts,
   if needed.
   * [mdbook](https://rust-lang.github.io/mdBook/) --- for documentation
2. [Python](https://www.python.org/) --- as its dynamic language of choice,
   to provide easy scripting. Typed Python will be heavily preferred.
3. [Markdown](https://www.markdownguide.org/) --- for easy docs generation.
   LaTeX and asciidoc were also considered, but markdown is both simpler
   than LaTeX and more widespread than asciidoc.
