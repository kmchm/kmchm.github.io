---
layout: post
title: "How to make icons in the menu bar smaller on your Mac?"
---

Once upon a time, there was a Mac user named little John, who loved keeping his computer neat and tidy. One day, he noticed the icons in his menu bar were so large, that some of them didn’t fit and were forced to hide under the notch!

How do I fix it and save the icons ?  —  thought little John.

![](../assets/images/make-menubar-icons-smaller/before.jpg)
*Little John’s menu bar before — not all icons are displayed, is boring, taking up too much space, so default, ugh.*

Well, that is easy.

You just open your terminal of choice (iTerm for me) and type in these two commands:

```sh
defaults -currentHost write -globalDomain NSStatusItemSpacing -int 6

defaults -currentHost write -globalDomain NSStatusItemSelectionPadding -int 4
```

Then you log out, and log back in.

![](../assets/images/make-menubar-icons-smaller/after.jpg)
*Little John’s menu bar after — mindful, demure, cutesy, and all of the icons are displayed!*

If you decide you don’t like it, change the values from 6 and 4 to something else. If you want to revert back to the OG Tim Cook way, just use these:

```sh
defaults -currentHost delete -globalDomain NSStatusItemSelectionPadding

defaults -currentHost delete -globalDomain NSStatusItemSpacing
```

Then log out, and log in.

Yeah, and that’s it. Go back to work now.
