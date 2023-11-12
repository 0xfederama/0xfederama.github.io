---
title: Learning and configuring nvim
date: 2023-01-18
tags: ['nvim']
thumbnail: "vim-nvim.jpg"
---

In my first blog post I want to document my journey learning vim and nvim.

![nvim-nvim](/vim-nvim.jpg "{width='50%'}")

Because of its steep learning curve, I have never really considered it. But after watching [The Primeagen](https://twitter.com/ThePrimeagen) flying through the terminal with nvim, I decided to give it a try. I followed some of his videos to learn about vim motions and [this video](tab:https://www.youtube.com/watch?v=w7i4amO_zaE) to learn how to configure nvim.

## First attempt

This journey started on my 23rd birthday, seeing a vim motions video explaining how vim works. Then, I started browsing some of the files with vim on my computer to see if the various commands where as difficult as it seemed from the outside. Sure enough, I found the vim concept quite clever and useful: having two modes, one for inserting and one for commands and browsing, is in fact quite useful.

After that, I started watching some videos, including the one mentioned above. I setup the directories and learned how nvim works; after 4 minutes, I gave up. Too much information, in a language that I didn't know (lua) and a directory structure I didn't understand. All that while trying to modify everything in vim to start to get used to it.

A couple of days later, I watched this TJ DeVries [video](https://www.youtube.com/watch?v=stqUbv-5u2s) about an instant IDE setup for nvim. For those who don't know him, he's one of the main developers of nvim, so a quite trustworthy source about this topic. After watching that video, I went on documenting more about nvim and why it uses lua, among other things. In that video, TJ DeVries linked a repository containing a basic setup for nvim, that I just needed to copy and paste in order to make it work.

Learning from previous experiences, as much as it's easy and fast to copy and paste things without even reading, it doesn't work in the long-term. So, I decided to go back to ThePrimeagen video setup to use it as a solid base for an nvim setup and to learn-by-doing, in order to learn and be able to modify the setup further by myself along the way.

## Second attempt

I started again from the beginning, this time with a different approach: write down the commands and shortcuts, stop the video at every modification to really understand the what and the why and write this blog post in the meanwhile to document everything. Things started to clock a lot better: I was understanding a lot better and I learned a lot more.

After a couple of hours, things started to get really complicated, with the author adding things like his personal remaps etc. So, I decided to follow his setup but only add the remaps that I think I would use. At the end of the video, he links also the [kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim) repository made by TJ DeVries, saying that it is made to be more familiar for users coming from vscode and other editors. Thus, next thing on the list is going through the simples TJ setup and compare it with mine, in order to simplify and tune my setup a little bit more.

### Difficulties and solutions

While following the video to create my setup, I found myself struggling with the most simple vim motions (`hjkl`), so I gave [vim-be-good]() a try to get the hang of it. So I modified `init.lua`, restarted nvim, entered `:PackerSync` to download the new plugin and... `E429: Not an Editor Command: PackerSync`. So I tried to use the remapped ` ps` to fuzzy find packer in the directory and... another error. Maybe the `after` directory wasn't loading properly? Searching online I did everything as it should be, so maybe I forgot something in the ThePrimeagen video. Moving through the directories, I realized also that I added some plugins like [harpoon](https://github.com/ThePrimeagen/harpoon) (a really good plugin indeed) that are not useful in a basic setup. I just followed the video caught up in enthusiasm, thinking that I needed a super fine-tuned setup.

The smartest way to setup nvim and make it really useful for me (and easy to use, since I struggle even with vim motions), is to start from TJ DeVries kickstart setup and tune it up a bit, adding some things from ThePrimeagen. To be honest, this is what I should have done days ago...

## Final setup

My final setup is a little bit of both worlds: simple, but tuned with useful plugins and remaps. You can find it on my GitHub in this [repository](https://github.com/0xfederama/dotfiles/tree/main/.config/nvim), that I will keep updated with new plugins and settings.
Below there's a list of all the plugins I wanted at the start of my setup (i.e. the first commit on the repo):
- [vim-be-good](https://github.com/ThePrimeagen/vim-be-good)
- [lsp-zero](https://github.com/VonHeikemen/lsp-zero.nvim)
- [treesitter](https://github.com/nvim-treesitter/nvim-treesitter)
- [telescope](https://github.com/nvim-telescope/telescope.nvim)
- [vim-fugitive](https://github.com/tpope/vim-fugitive).

Other than these plugins, I also kept these one from TJ's video: vim-rhubarb, gitsigns, lualine, indent-blankline, comment and vim-sleuth.

## April '23 update
I changed everything. Kickstart.nvim has been updated, and I'm now using [lazy.nvim](https://github.com/folke/lazy.nvim). Therefore my whole repo structure changed and the plugins used are different. Now I'm with my own personal setup and I fine-tuned it to my likings.

