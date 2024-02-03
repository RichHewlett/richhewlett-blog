---
layout: post
title: Coding in Spectrum Basic Again
date: 2021-06-12 17:16:41.000000000 +01:00
type: post
parent_id: "0"
published: true
password: ""
status: publish
categories:
  - Software Development
tags:
  - Spectrum
meta:
  _last_editor_used_jetpack: block-editor
  _thumbnail_id: "2280"
  _publicize_job_id: "59514537702"
  _publicize_done_external: a:1:{s:7:"twitter";a:1:{i:23564039;s:58:"https://twitter.com/richhewlett/status/1403748099718369281";}}
  _publicize_done_22491951: "1"
  _wpas_done_23564039: "1"
  publicize_twitter_user: richhewlett
  timeline_notification: "1623514603"
permalink: "/2021/06/12/coding-in-spectrum-basic-again/"
---

My first computer was a Sinclair ZX Spectrum (16k) with rubber keys which is an icon of the innovative 1980's micro computer market.

![]({{ site.baseurl }}/assets/2021/06/zxspectrum.jpg?w=576)

Sinclair ZX Spectrum

On it I learned to code in Sinclair Basic either by reading the manual or typing in programs from the Spectrum magazines of the time. It wasn't long before one Christmas my ultimate gift arrived...a ZX Spectrum 128k +2....now that was a machine!

![]({{ site.baseurl }}/assets/2021/06/zx_spectrum_plus2.jpg?w=1024)

ZX Spectrum 128k +2

It's probably no surprise that the main purpose of my Spectrum was to play games and I played for many hours, but I also learned to program, create databases and do word processing on my Citizen 120D dot matrix printer. All this just seemed like fun at the time but turned out to be useful skills, which I guess is the benefit of combining gaming with utility uses in modern devices like the Raspberry Pi.

![]({{ site.baseurl }}/assets/2021/06/citizen120dprinter.jpg?w=600)

Citizen 120D Printer

Recently I've been getting nostalgic and rekindle my love of coding on for a Spectrum, but now in the modern PC era we have many many options for how to do this. We have emulators and IDEs and free resources to download quickly (no 10 minute load time :-) ). In this post I'm covering a few options to quickly and easily getting started on coding in Sinclair Basic, mostly so I don't forget when I get nostalgic again in the future.

The most traditional and authentic approach would be to setup an original Spectrum machine and code directly on it, but this is not the easiest option, especially if you don't have a working spectrum sitting around at home. So we are going down the emulator route here.

Essentially there are two key things we need to code and run our basic program. Firstly we need a compiler to compile our program down into binary and secondly we need an emulator to run the compiled, program. There are lots of options here, and I'll post links later for where to look for alternatives but below are my current choices.

### SpectNetIDE - An all in one solution that runs as a plugin in Visual Studio.

[SpecNetIDE](https://dotneteer.github.io/spectnetide/) is a Visual Studio 2019 plugin enabling you to code your Spectrum program in the excellent Visual Studio IDE and it also includes an emulator so you can run and debug all in one place. Check it out here: [https://dotneteer.github.io/spectnetide/](https://dotneteer.github.io/spectnetide/)

![]({{ site.baseurl }}/assets/2021/06/spectnetide1.png?w=620)

SpectNetIDE

If you already have Visual Studio installed then installing this trying it out is quick and easy. If you dont have Visual Studio then you download the Community edition free from Microsoft. Note this is a Windows only option. Assembly and Basic is supported with basic being implemented via the widely used Python based [Boriel compiler](https://www.boriel.com/pages/the-zx-basic-compiler.html) which complies Basic down into Z80 Machine code.

After a few [setup steps which are well documented](https://dotneteer.github.io/spectnetide/getting-started/setup-zx-basic#article) then you're away and coding. Make sure you install V2 if you plan on coding in Basic. Follow the [simple documentation](https://dotneteer.github.io/spectnetide/getting-started/create-a-basic-program-2#article) to get started with a ZX Basic program. There are some links at the end of this post for guides to coding in ZX Basic and many of the 1980's manuals are available to download for free.

![]({{ site.baseurl }}/assets/2021/06/spectnetide_rh1.png?w=1024)

Once you've completed your program you can create TAP file (the equalivant of an old data tape) and play it on other emulators.

## 'VS Code > Command Line > Emulator' option

An alternative option that I have been using is to use VS Code (or any text editor, including Notepad) and then using [Boriel compiler](https://www.boriel.com/pages/the-zx-basic-compiler.html) via the command line to compile the code to a TAP file and then loading the TAP file into one of the many available emulators. This option runs on Windows and Linux and Mac.

Ewhilst any text editor can be used to code your program, VS Code is argubly the best code editor there is, plus you can install ZX Spectrum plugins to make your programming easier. The one i use is [ZX Basic](https://marketplace.visualstudio.com/items?itemName=jsjlogin.zxbasic) which provides syntax highlighting.

![]({{ site.baseurl }}/assets/2021/06/vscode-zx.png?w=1024)

Next we need to be able to compile this down so we install [Boriel Compiler](https://www.boriel.com/pages/the-zx-basic-compiler.html) from the [downloads](https://zxbasic.readthedocs.io/en/latest/archive.html) section (this Python compiler is open source on github [here](https://github.com/boriel/zxbasic)). Check out the installation and quickstart guide on the [GitHub page](https://github.com/boriel/zxbasic). Once its extracted you can call the compiler via the command line with something like this (which will create a tap file):

./zxb.exe ./code/helloworld.bas --tap --BASIC --autorun

Once compiled into a TAP file then we can run this on any Emultor you like that supports TAP files (which the majority do). My current favourite is the JavaScript based _[Qaop/JS](http://torinak.com/qaop)_ as it runs in your browser. Click on the sides of the window to open the menu and choose to 'Open' your TAP file, and watch your amazing program run in all its 1980's glory.

![]({{ site.baseurl }}/assets/2021/06/qaopjs_rh.png?w=1024)

Now I just need to learn to code better programs than I did as a child....the links below should help.

## Useful Links

- SpectNetIDE: https://dotneteer.github.io/spectnetide/
- Boriel Compiler: https://github.com/boriel/zxbasic
- Qaop JS Emulator: http://torinak.com/qaop
- ZX Basic VS Code Plugin: https://marketplace.visualstudio.com/items?itemName=jsjlogin.zxbasic
- ZX Basic: https://zxbasic.readthedocs.io/en/latest/index.html
- JS Speccy Emulator: https://jsspeccy.zxdemo.org/
- ZX Coding Jam & example apps: https://itch.io/jam/zx-spectrum-basic-jam
- Sinclair Basic Info: https://worldofspectrum.org/faq/reference/BASICReference.htm
- BASin: https://documentation.help/BASin/index.html
- Spectrum 48 Basic Manual: https://dotneteer.github.io/spectnetide/spectrum/basic-toc.html
- ZX Basic Manual: https://worldofspectrum.org/ZXBasicManual/
- World of Spectrum: https://worldofspectrum.org/
- Emulators: https://worldofspectrum.org/tools/emulators
