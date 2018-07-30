{section:frontmatter, sample:true}
# About This Book
This is a **continually-published** book, sold only via [Leanpub](http://leanpub.com/powershell-by-mistake). Although you only pay a single, one-time price to purchase the book, you'll have access to new chapters each time they're published, long into the future. It's recommended that you permit Leanpub to notify you, via e-mail, when new chapters are posted. That way, you'll know it's time to come get the latest. If you don't explicitly opt into those notifications, be sure to check back at least monthly for new content.

There's no change-log for this book; each new "build" published on Leanpub will contain a new chapter.

My commitment is to publish at least 12 new chapters a year, or one chapter for every 25 readers this book accumulates, whichever is more. So you can help keep the book growing by referring your friends, coworkers, and colleagues! This book's Leanpub web page contains the official reader count near the top of the page.

{sample:true}
# Introduction
Human brains are funny things. At the end of the day, our brains are still wired the same way they were when we were cavemen trying to survive in the wild. Anything relevant to our immediate survival tended to "stick" in our brains, and anything not relevant tends to slip past. Tell a child, "don't touch that hot pot on the stove!" all you want to, they're still likely to touch it - once. 

This book is the hot pot on the stove.

In this book, I've collected edited versions of posts from the PowerShell.org Q&A forums and other online forums. I've anonymized these, although nothing in this book should _ever_ be construed as criticism of the original posters. We _all_ make mistakes, and thanks to the way our brains work, making mistakes and solving them is the best way for us to learn. So in each chapter, I'll present a new problem from the forums, and I'd like you to take the time to try and figure it out for yourself. I'll also present a solution, along with explanations. 

This book is _not_ a how-to, and I presume that you already have a decent amount of basic PowerShell education under your belt. This book is not about how to make Active Directory work, or Exchange Server, or SharePoint Server, or anything else; this is about _PowerShell_. So you're going to see problems that relate to the core of how PowerShell works. Many of these problems spring from "gotchas" in PowerShell, while others have their origin in very common misunderstandings about how the shell works.

If _you_ feel that you learn best by getting your hands dirty, making mistakes, and figuring them out, then this book is for you.

{sample: true}
# How to Use This Book
Read each chapter. Pore over the code (if you prefer to look at the code in an editor, which I recommend, you'll find the code downloadable from [GitHub](http://github.com/concentrateddon/powershell-by-mistake-code), with each chapter's code samples in their own folder). Read it all _thoroughly_. Try to figure out what's wrong. That's really the point of this book: taking the time to understand the code, and to see if you can figure out the "fix."

Each chapter ends in a "Spoiler!" section, which contains a possible solution. Use this to check yourself, but know that most problems can be solved in a number of ways, so if you came up with something different, you're not necessarily wrong.

It is **hugely important** that you make the effort to understand the problem code and solve it *before* looking at the solution. This is a fundamental part of how human brains work! If you just skip ahead and read the solution, _you won't actually learn anything_. You'd be cheating yourself, and you shouldn't do that. Treat each chapter as a puzzle, and make the effort to try and solve each one.

{sample:true}
# A Note on Code Samples
Printing code in a book is a huge pain in the neck. E-readers format it however they darn well please, giving authors no control. PDF is okay, but consider this:

```
Import-CSV users.csv | Select @{n='samAccountName';e={$_.name}},Name,Department,City,Title | New-ADUser -PassThru | Export-CSV output.csv
```

That backslash you see at the end of the first line isn't a typo, it's the code-formatter's way of saying, "this didn't all fit on one line, so I'm wrapping it to the next line, but you shouldn't do that if you're typing this in yourself." I can't fix that because there's no other reasonable thing to do.

Backslashes cause another problem, as in C:\Program Files\WindowsPowerShell:

```
C:\Program Files\WindowsPowerShell
```

See, in a lot of instances the backslashes get removed, because Markdown considers them to be escape characters. If you notice this happening, drop me a line using the "Email the Author" link on this book's page on Leanpub.com. Tell me where the problem occurs (which chapter; your page numbers won't line up for me), and I'll replace them with / forward slashes.

As you can see, reading code in a book can be a pain. Instead, I recommend grabbing the code downloads from [GitHub](http://github.com/concentrateddon/powershell-by-mistake-code) so you can see the code in its "unadulterated" form. Or, just learn to deal with the foibles of printed code listings!

{sample: true}
# Contacting Me
I cannot help with technical Q&A via email, so please don't use the "Email the Author" form on this book's Leanpub page, and please don't tweet questions to me @concentratedDon. I do love hearing from people via those channels, but they're not suitable for technical Q&A. Instead, please use the Q&A forums on [PowerShell.org](http://powershell.org/forums) for technical Q&A.

That said, if you found a typo or something, use the "Email the Author" link on the book's Leanpub page to let me know. I do appreciate it, and I'll make corrections for the next build of the book. As a "continually published, Agile book," there's not really an opportunity for an editor to step in and fix those things ahead of time (and financially, this book wouldn't be worth doing if an editor needed to be paid), so it's really awesome of you to let me know if you find things. I also appreciate your patience with my typos!

