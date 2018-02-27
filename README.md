# GW2-Build-Template
A template for GW2 WvW builds hosted on GitHub. Here's an example of the one I made: [tgdm.github.io](https://tgdm.github.io/).

#Getting Started
Go here and set up a GitHub account and repository (it has step-by-step instructions): [pages.github](https://pages.github.com/)

##How To Edit These Files
You're going to want a text editor with formatting support like [Notepad++](https://notepad-plus-plus.org/) or [Atom](https://atom.io/). Atom is probably not as newbie friendly but it has great support with GitHub in general.

#Getting Familiar With the API
Try not to get overwhelmed - it's easier to use than it looks. You're pretty much going to be changing numbers occasionally and copy&pasting.

The stuff this template has is basic. If you want to add more complex embeds take a look at the [official documentation](https://wiki.guildwars2.com/).

##Finding API Codes
You can find almost all codes on [wiki.guildwars2.com](https://wiki.guildwars2.com/wiki/Main_Page) by going to the specific page for an item, skill, or trait. There are a few exceptions and for those I've added reference .txt files in the "Reference Files" folder. For class specialization codes, use reference-specs.txt. For item stat assignments, use reference-stats.txt. You can also use the .html files to preview what they look like.

##Changing API codes
I've left in placeholders for you to change as you see fit. You can add more embeds, remove embeds, add more *within* an embed - all up to you. The two most important things are changing the embed type and the item being called.

```html
data-armory-embed="__EMBED_TYPE__"
data-armory-ids="__API_CODE_HERE__"
```

For this template, you are going to be using mostly 1 of 3 embed types: `items`, `skills`, `traits`. Make sure it's assigned to what you want. Some parts, like the trinket items or specializations, will need secondary API codes to work. After that, plug in the API code you need to call the item.

```html
data-armory-embed="specializations"
data-armory-ids="31"
data-armory-31-traits="296,325,1510"
```

In this example, we're calling the API `31` to pick the specialization we want to add. After that we pick the traits for `31` on the line `data-armory-____-ids=`. You'll have to manually change the 31 on both the middle and bottom line to get the spec and traits to properly work.

Make sure you do not delete `"` or `>` by accident!

#Customizing Tabs and colors
This template comes with 3 tabs. If you only want 1 tab, 2 tabs, or if you want 4 tabs, you'll have to modify both the index.html and the style.css (found in /assets/stylesheet/). Add or subtract rows with the index.html near the top, assign names/colors on style.css near the bottom. If adding or subtracting tabs, adjust `.tablink` in the CSS file

If you don't like the colors I used for the template (they're terrible), modify it to what you like - but make sure you edit both documents.

##Tips and Practices for Adding Text
You're going to want to learn about <p> paragraph tags and <a> link tags. When you want a line break, add <br> to the end.

Google is your friend if you need help to do something. [w3schools](https://www.w3schools.com/) is a great resource.
