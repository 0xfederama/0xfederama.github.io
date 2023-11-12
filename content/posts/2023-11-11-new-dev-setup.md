---
title: My dev setup using VSCode and nvim
date: 2023-11-11
tags: ['nvim', 'vscode']
---

Back in January I made a [post]({{< ref "/posts/2023-01-18-nvim-setup.md" >}}) on how I was learning and configuring vim and neovim. After 10 months, during which I focused on University and didn't write code 24/7, I found myself more and more going back to VSCode. So I decided to fine-tune VSCode to my likings, and simplify nvim to use it when I need to modify some files from the terminal.

In the last few months, I realized that in my 4 years of using VSCode I never customized it (aside changing theme) and I filled it with a lot of bloat. In this post I'm going to explain how I simplified and tuned both VSCode and nvim.

## Why I decided to move back to VSCode
During these 10 months of learning vim and using nvim, I found myself constantly worrying about something wrong in my nvim setup. For example, I had issues with conflicting themes between my terminal (iTerm on macOS) and nvim, I had issues with the bufferline, I had issues with the neotree plugin, I had issues with the Option key, I couldn't drag and drop, and some other minor things. Since starting with nvim, I have fixed a lot of problems, changed the setup a lot of times (even a full rewrite of it), and above all, _lost a lot of time_ doing it.

Don't get me wrong, I love nvim, tmux and being able to only use the keyboard, but I have to admit that a lot of these issues are not present in VSCode, while some of the pros are there. I don't need the performance of the terminal on my computer, I don't have strong feelings against VSCode, and I found myself more and more going back to it, just for the ease of use.

## VSCode
Starting with VSCode, I began by scrolling through extensions and keeping the only ones that I'm actually using, knowing that I can always reinstall an extension with 30 seconds and a Wi-Fi network.

Then I simplified a lot the `settings.json` file, which was full of default options and deleted extensions, and added a couple of new settings.

Finally, I installed the vim plugin to be able to define and use my favourite vim keybindings, in the hope that this will ease my transition back to VSCode.

The final `settings.json` file can be found [here](https://github.com/0xfederama/dotfiles/blob/main/settings.json).

## Nvim
For the moment of writing, I'm currently not modifying my nvim installation because I want to try for some time the new VSCode settings. If I will simplify it, I will go back to this post and explain how I have done it.

I don't want to preclude anything and I want to have both VSCode and nvim up and running, if I ever need them. One thing I know for sure is that by coding in VSCode I will miss tmux the most, so we will see where all this will get me and I will come back to nvim and tmux...