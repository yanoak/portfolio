---
title: #100DaysOfCode Progress - Days 0 to 20
slug: 100daysofcode-progress-days-0-to-20
date_published: 2018-01-07T00:57:44.000Z
date_updated: 2018-01-07T02:00:26.000Z
---

I signed up for this challenge on a whim on my birthday last month.

> I turn 31 today. That&#39;s like the maximum number of days in a month. Gonna give myself a challenge and start a [#100DaysOfCode](https://twitter.com/hashtag/100DaysOfCode?src=hash&amp;ref_src=twsrc%5Etfw). Please watch my github and bug me if I slack off: [https://t.co/4Jntfl4Oet](https://t.co/4Jntfl4Oet)
> &mdash; Yan (@yanoak) [December 17, 2017](https://twitter.com/yanoak/status/942211320195067904?ref_src=twsrc%5Etfw)

I felt like it would be good to have some sort of a way to coerce myself into being productive, and I especially wanted to [spend some time in 2018 working on open sourced community tech and data projects](http://blog.yanoak.me/looking-back-at-2017/).

It's worked out pretty well so far. I only skipped 2 days out of the first 21 days. But I've managed to coax github into thinking that I've pushed code every single day :wink:

![Yay look at all the green at the end](/content/images/2018/01/100daysofcode_day20.png)

I managed to work on 2 projects which were both for the jade data portal that I'm working on for my [School of Data Fellowship](https://schoolofdata.org/fellowship-programme/). There is a question of whether I could count my "work" projects towards #100DaysOfCode, but I'm just going to count any project that I work on that is open source and freely accessible for the public as counting towards it.

## Project 1: Company Networks Explorer

The first project is an exploratory data tool for civil society, journalists and others to explore networks of companies and their directors who are involved in the jade, gems and mining industries in Myanmar.

You can check out the prototype [here](https://yanoak.github.io/jade-company-network/network-test/) and the repo [here](https://github.com/yanoak/jade-company-network).

![Prototype of networks explorer](/content/images/2018/01/networks_prototype.gif)

The data scraping was done some time ago using [morph.io](https://morph.io/yanoak/dica_myanmar_company_directors), and was cleaned with pandas python and made into a network with the [NetworkX package](https://networkx.github.io/). The tool was built with D3.js and plain javascript.

It's the first real interactive network visualisation I've built. I often find interactive network vizes hard to use and understand because it becomes hard to obtain useful information from them once the networks become big. One way that I've tried to manage that here is by giving the user an option to choose how many degrees of separation they want to display spreading out from the main individual or company they want to display. I found that it does make it simpler to visually figure your way around smaller networks but for some really highly connected people it still devolves into a big mess. I might try to implement a different way of visualising the network in the form of concentric circles of nodes if I have time later this month.

One UI feature I added is a list of nodes in addition to the network that highlights when you mouseover the nodes in the work and vice versa, and locks when you click. Another feature is a little "+" button beside a node if that person/company also has a network in the database, and when you click it opens up a new network with that node as the center. The idea is to let users really explore the connections on a simple app with no backend (each network's data is a seperate tiny json file) that loads very quickly.

I still think it's a bit clunky at times but I'd like to show the tool to more potential users before committing more time to make fixes based just on what I think.

## Project 2: Mining Licenses Explorer

The second project is less fancy and more pedestrian really, but I think it will definitely be a useful tool.

It's another exploratory data visualisation, but this one is of mining licenses and which companies own them, in the form of a filterable, interactive dashboard.

You can check out the prototype [here](https://yanoak.github.io/jade-company-network/network-test/) and the repo [here](https://github.com/yanoak/jade-company-network).

![Prototype of licenses explorer](/content/images/2018/01/licenses_prototype.gif)

I actually repurposed the code I wrote for another project I did in early 2017 for this. The data is from the appendix of the [2014 EITI report](https://eiti.org/myanmar). The dashboard was built using [DC.js](https://dc-js.github.io/dc.js/), which is definitely one my favorite libraries built on top of D3. If I have time this year, I'd love to explore it further.

## Up Next

So, not too bad so far. My plans for the next 20 days are to add another exploratory viz tool that I'm going to repurpose from another old project, and (I'm really excited for this), some [scrollytelling](https://pudding.cool/process/how-to-implement-scrollytelling/)!
