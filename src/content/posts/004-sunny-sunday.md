+++
date = '2026-05-05T21:26:02Z'
title = 'A free, self-hostable alternative to Readwise'
description = 'Send Kindle highlights back to your device with a free, self-hosted Readwise-style recap. Customizable, private, and open-source.'
url = 'free-selfhosted-readwise-alternative'
tags = [
  "ai",
  "relego",
  "readwise",
  "kindle",
  "side-project",
  "github",
  "note-recap"
]
+++

About a month ago, I was lying on my bed reading *[Geopolitica dell’intelligenza artificiale](https://www.amazon.it/Geopolitica-dellintelligenza-artificiale-Alessandro-Aresu/dp/8807174731)* (2025, Aresu A.) on my Kindle. I don’t remember the topic covered in that particular chapter, but it was certainly interrupted by one of the hundreds of digressions of the author. Don’t get me wrong: it’s a nice book, full of interesting facts and arguments. However, the message is often lost among topics and stories stacked on each other, and sometimes the overall point is hidden or only hinted at. As I am not a philosopher nor an expert reader, at the end of the day I hadn't engaged with the book much, and I remember just a bunch of insignificant details after reading more than 600 pages.

Anyway, as I reached the end of the chapter, I wanted to read my [Readwise](https://readwise.io/)'s daily recap. However, my iPhone was in other room. I didn’t want to get up; I was tired.

> I have my Kindle in my hands; I want to read. Why do I still need my phone?

I didn’t get up to get my phone immediately. Instead, I thought a little about my issue. I’m an IT guy and I have AI at my disposal. Is Readwise hard to replicate? What do I need to build it? Do I have time? How do I send notes to my Kindle? Well, the truth is that it’s not hard to replicate, especially in the AI era. I do not have enough time to write every single line of code, documentation, product specifications, and more, but AI can help me. I can use the technology stack I know very well ([dotnet](https://dotnet.microsoft.com/en-us/)) to iterate quickly and spot AI errors easily.

So, the project began.

A few days later, I defined the product specifications ([PRD](https://en.wikipedia.org/wiki/Product_requirements_document)) with Claude (free tier) and then, I moved to GitHub Copilot (the subscription I own) to define `DX.md` and `ARCHITECTURE.md` as well. Once done, I created a repository, but I did not have a name yet. Then, I thought about the day that I had: it was a lovely spring Sunday spent with my wife and friends strolling through my city, Milan. In short, I had good vibes. *Sunny Sunday* perfectly depicts that day with its deep blue sky, and that's why I chose this codename for the project.

To make things even more interesting, I've been using *[spec-kit](https://github.com/github/spec-kit)* for the first time, a GitHub framework to implement the [spec-driven development](https://developer.microsoft.com/blog/spec-driven-development-spec-kit) methodology through Gen AI. I found it generally useful, although it's only for a side project and few considerations must be taken in advance. I’ll blog about it and the development flow in the coming weeks.

Yesterday, I’ve released the *MVP* of *Sunny Sunday*, a fully working version that allows you to upload all your Kindle highlights and send them back to your Kindle through a daily or weekly recap like Readwise does. The entire experience is highly customizable: you can choose the recap frequency and time of the day, the number of the highlights in the recap, exclude books or authors, and adjust the likelihood that a highlight or book is included in the recap. At the moment it supports Kindle only, but the plan is to integrate more platforms, as inputs and outputs as well.

Generally, existing platforms provide daily recap via paid subscription on managed SaaS, which also raises privacy concerns. For these reasons, I'm releasing *Sunny Sunday* for free and self-hostable. Usage guide and source code are available on [GitHub](https://github.com/Krusty93/relego).

If you want to try it and provide feedback, feel free to comment on this post or create an [issue](https://github.com/Krusty93/relego/issues).

In the near future, next steps include an improved and simpler setup, a landing page, and a more suitable product name. Do you have any ideas? Share them in the comments below!
