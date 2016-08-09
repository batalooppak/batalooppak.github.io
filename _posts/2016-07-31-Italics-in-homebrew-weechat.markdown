---
layout: post
title:  "Displaying italics in brewed weechat"
date:   2016-07-31 09:05:00
categories: IRC, osx
---
## Displaying **italics** in weechat (OSX)

To be able to display italics in brewed weechat first we need to have a terminal
that is able to do so.

To make sure if your terminal is able to do it run this escape command:

```bash
echo -e "\e[3mDo I have italics?\e[0m"
```
The result should look like this:
```
**Do I have Itaclis?
```

