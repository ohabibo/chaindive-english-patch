# Frequently asked questions

## What do I need?

Your own copy of ChainDive (Japan), serial SCPS-15054, dumped to an ISO file, and PCSX2 (or a PlayStation 2 that can run backups). The patch contains no game files, so it cannot be used without the game.

## Which ISO does the patch work with?

Only a complete 1:1 dump of the Japanese disc. Every good dump of that disc is the same file: 1,232,306,176 bytes, which Windows Explorer shows as 1,203,424 KB. The patcher checks this for you and tells you when the file is different. The checksums are in the [README](../README.md#what-you-need) if you want to check them yourself.

## The patcher says my ISO is not the right one. What now?

Your file is not a complete, unchanged dump. The usual reasons:

- It is compressed (CHD or CSO). Convert it back to a plain ISO first, for example with `chdman extractdvd` for CHD or maxcso for CSO.
- It was trimmed, or patched before (with another patch or by a tool that changes the disc).
- The dump has read errors. Dump your disc again.

## Does it work on a real PlayStation 2?

It should: the patch only changes the game's own data, in the game's own formats, and nothing depends on the emulator. It has not been tested on a console yet. You need a PlayStation 2 that can run backups, for example with Open PS2 Loader from USB, a hard drive or the network, or a modified console with a burned DVD. If you try it, please tell us how it went.

## Which PCSX2 settings do I need?

None. The English version was tested with the default settings of PCSX2 2.x. If you made settings for the Japanese game, they stay: the English version looks like the same game to PCSX2.

## Can I keep my Japanese save?

Yes. The English version uses the same save data as the Japanese game.

## Windows says "Windows protected your PC". Is the patcher safe?

The patcher is not code-signed, so Windows does not know it yet. Click **More info** and then **Run anyway**. The patcher only reads your ISO and writes a new one next to it; your original ISO is never changed. If you prefer, `apply_patch.py` in the download does exactly the same and is plain, readable Python.

## Can I use it on Mac or Linux?

Yes, with Python 3: put `ChainDive-English.cdpatch` next to `apply_patch.py` and run `python3 apply_patch.py "ChainDive (Japan).iso"`. It writes the same English ISO as the Windows patcher.

## Is the voice acting in English?

No, the Japanese voices stay. The English text works like subtitles: the dialogue boxes are in English, and the spoken lines in the opening and ending movies have English subtitles.

## Why is the last stage called "Title Space 12 Chars"?

That is a translation of the Japanese name. The developers left a placeholder there ("title space, twelve characters"), and Japanese players see it too, so the English version keeps it.

## Can I share the English ISO?

Please do not share patched ISO files; they contain the whole game. Share the patcher instead, so that everyone patches their own copy.

## I found a mistake in the translation.

The translation was made by someone who does not speak Japanese, with the help of a translation tool, so mistakes are possible. Corrections are very welcome, especially from Japanese speakers: open an issue in this repository and quote the line.
