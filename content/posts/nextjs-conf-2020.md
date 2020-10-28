---
title: "Nextjs Conf 2020"
date: 2020-10-27T23:37:30-05:00

---

# The NextJS Conference 2020: 70K registered and saw so many people on Discord

## A new blog for a new leg of my journey

I am super excited to write my first personal blog post about my experiences at a conference in my new industry: the first ever [NextJS Conference](https://nextjs.org/conf/)! This was by far the largest virtual event I have taken part in and it was super well organized and flowed really well. While 70K had registered, I believe I saw one place that there were 'only' around 2,300 on the Discord instance.

While I have ducked in and out of several virtual WordCamps and Drupal events over the last year, I have not been writing about them. Not even [Midcamp](https://www.midcamp.org/), which I helped organize. We were the first 100% virtual Drupal camp on earth I believe. If you want to read about my previous adventures,  you can check out [my previous event/travel blog](https://mcdwayne.com) . 

{{< tweet 1321125558747570177 >}}


## No in person stuff, but Discord was there for flavor

As you can imagine, with this large of an event, there was a lot of chatter and conversations going on at once across dozens of Discord channels and Twitter.  I started following a number of folks on social media I met in the General and Introduction channels. Not quite the same as meeting and chatting in person for sure, but networking all the same.  

There was also the traditional ['Expo Hall'](https://nextjs.org/conf/expo) set up but with a one day event and so much to see I didn't get the chance to set up a demo or even interact with any of the vendors directly. This is concern to me as someone who loves event marketing. How can sponsors reap the benefits of foot traffic at such events? This is a hard question that I have not seen a compelling answer for just yet.  I will say however, I do plan on looking into the companies from that expo list that I do not yet recognize.  The JS space has a lot of players and it is good to have any kind of resource for who is doing what. 

## So many talks and so many things written down

With over 60 talks scheduled for a one day event, of course it would be impossible to see everything. Good thing for us they are all recorded on the [conference's Youtube channel](https://www.youtube.com/c/ZEITHQ/videos)

A quick note on style: If you were a reader of my previous event/travel blog you will know it is my preferred style to share my raw notes as well as a summary of what I generally took away from the sessions. I want to share as much of my experience as possible and this also makes it way easier for me to find notes on a subject later on. Not only is my site online, but also stored in MD files locally and grep is a magical tool. Raw Notes are labeled as such.  


### Keynote

[Guillermo Rauch, CEO at Vercel](https://twitter.com/rauchg)
[Belén Curcio, Solution Architect at Vercel](https://twitter.com/okbel)
[Tim Neutkens Head of Next.js at Vercel](https://twitter.com/timneutkens)


I thought my sound was out for the first 10 seconds as they did a super slick polished video of Guillermo checking his phone, noticing we were there and then welcoming us to the conference. I really enjoyed the production value as well as the announcements he and his team made about Next.js 10, released the same day as the conference.  Biggest take aways are new auto optimizing Image to use instead of regular img, Internationalization tooling built in for domain routing and translation and the biggest add in my mind, the Web Vitals integration. You can read much more about these things on the [Next.js release blog](https://nextjs.org/blog/next-10)

Two data points that really stuck out to me were about updated site user patience stats and how much ecommerce has exploded recently. First. for every 10 milliseconds of load time, the average person is 1% more likely to leave. This is quicker pace than the old metric of '1 second = 7% traffic loss'. We are becoming more impatient it seems.  The other astounding number was that before Covid, ecommerce accounted for 16% of total retail sales. Last month it was 34% of that total.  So much has changed so fast.       


RAW NOTES:

Nextjs 10

update easy

many benefits

Images

hard

Images vs img

I18n

Translation and routing

Language detection and Routing

static generate what is needed

lan-region

nl-NL vs nl-BE

domain routing top level domain, 

dynamic rendering

content duplication avoided by language i18n tagging automatically

static or staying fast over time

performance monitoring as part of the workflow

been checking performance wrong

NextJS 10 analytics

measuring continuously

from all devices

from the actual regions people are in

deeply understanding is critical

Google came up with critical metrics

Web Vitals

perceived loading speed

LCP - largest contentful paint

cart count First Input Delay FID

Layout shift (annoying when buttons move while loading)

emulated testing can not predict this stuff

Users needed to get real data

nextjs/analytics

Ecommerce space

bevore 16 vs 34%

10 yers in a few months

10/th second is 1% drop

powerful new tools images, i18n, real analytics

Nextjs.org/Commerce

new super fast options, best in class ecommerce store

ships with componenets just ready to go, cart, wishlist

optimized

Tomorrow job fair


{{< tweet 1321120962675384321 >}}

### [When Not to Use Next.js](https://nextjs.org/conf/speakers/jescalan)

[Jeff Escalante](https://twitter.com/jescalan)
Hashicorp

I had a feeling after the first 10 minutes of this one that, as one commenter on the Discord chat put it, "I bet the big reveal is there is never a good time not to use it." Turns out, no. There are some times when using it as a hammer is the wrong move. But with tooling this powerful, it is important to know what it is really good at before you can start quantifying use cases it is bad for.  

The biggest take away from this talk was his perspective on how cloud vendor creep and data source creep are things that need addressed over time as a result of growth.  Tools like Next.js are built to deal with this. Turns out, if you need simplicity but don't need to scale and/or have no budget, maybe spending the cycles to leverage this power is too much. But you won't know unless you learn what it can do though.  


Raw Notes:

How is he even giving this talk? 

He has thought much about it

it's all about balance

one key philosophical idea 

interesting features

Hybrid Architecture

a key aspect of nextJS philosophy

Frameworks tend to couple to one architecture

dynamic (WP, PHP, Rails) 

Static (Gatsby, Hugo, Jekyll)

People like to talk about this

Mullenweg vs Biilmann - Netlify conference

Both are blondish gents with beards, in front of decorative bookshelf

Next.js don't care (like the honey badger)

You can make static before deployment or you could make a dynamic page on every
 load, depends on how you use NextJS

You can take a path in between extremes

Don't @ me about caches, IT IS NOT binary static/dynamic

caching blurs it

caches are not easy to deal with

with nextjs this is not the case, DOM manipulation

but you are not calling the shots, like back with Backbone you had to write out
 the dom interactions

React more declarative models, 

There is caching happening, but there is no need to manually fuss with it

Hashicorp Multi Architecture (not a plug, no one asked him to drop this in)

On prem vs Cloud - analogy

Quickly on prem becomes mostly and clear cloud is the better approach

Used to be people deployed code to own servers, then amazon, but really
 multiple other plays, more complex

Even if a company govern to make only one choice, M&A gets the multi cloud
 problem...

any sufficiently large company has to eventually deal with multiple cloud
 vendors

Hashicorp tools can interface with all the cloud providers and only one single
 set of tools/resources 

that shift is how Hashi has succeeded

back to the point

dev -> static/dynamic/etc

no longer have to logically make those splits and try to manage it

Next serves the same function as Hashi, one mental model to deal with multiple
 ways to do apps

Hi team does Hashicorp websites

they are building 14 sites

diversity of different needs

docs, ot marketing, to conference websites

all unique site needs

across those sites a wide range of challenges

only 7 devs, for a very fast growing company

how they even keeping up?

share the most things they can between all the sites

shared platfrom approach

Shared - foundation, tooling, components, knowledge, dev resources

thousands of pages, public user profiles, custom search, custom content based
 on user

OK, back to the talk, we drifted pretty far with basic concepts

the X for Everything problem

a pervasive issue in tech

Rails as example

Rails has 'everything you need' example articles/posts he shows

Jamstack solves everything!

Where NextJS shines:

Flexibility, Scale, Active Maintenance

Where NextJS does not shine

Small, simple sites

No plans for aggressive growth and scale (the largest part of the internet,
 super important)

not frequently updated/maintained

no need for react in the first place 

but please experiment!

the line is drawn when people paying to do certain work, 

ply it in the right way

next.js hybrid architectures, abstracts a level up

this is effective for high flex/scale

it is not the solution for all problems. 

maybe not for small sites with no scale needs


{{< tweet 1321134168974254082 >}}

### [Everything Is a CMS](https://nextjs.org/conf/speakers/jescalan)

[Sean C Davis](https://twitter.com/seancdavis29)

Of all the talks I saw that took full advantage of being recorded before hand, Sean took the possibilities the furthest.  I thought I had switched over to watching a [Polygon youtube written by Brian David Gilbert](https://www.youtube.com/playlist?list=PLaDrN74SfdT7Ueqtwn_bXo1MuSWT0ji2w) for a moment. If there is higher praise I don't know how to bestow it. 

This talk was a brilliant overview of the difference between API and Git based CMS approaches. Given that you can treat every data source imaginable as one or the other, so long as you ingest them through some ingestion layer, you can make anything a CMS! Even Trello! Even Google Sheets!  Not that you should.  But if you are in need of a good talk about how to evaluate CMS options, this is the best vid I have seen about that.  

This talk also had the effect of making me order a sandwich for lunch.  

Raw Notes:
 
Quirky funky intro, reminds me of BDG humor

SCD C makes his name totally unique

Ample - Cinci Ohio

does a lot of things with tech

the 29 comes from his birthday, leap day, 8 birthdays

Stella his dog

one talent, balance on her head

1. How do we ge the right CMS

How doe we minimize rework when making changes

considering Data source no matter what you choose

two types of CMS (ignorming the monoliths)

API driven or Git Based

Everything is how consumed and stored

API-Driven 

data in the DB,

Content consumed by an API

Contentful, Agility, Dato, Sanity and even WP can do it

Git based 

data stored in MD, YML, JSON, etc

Content is assumed by reading the data file

Forestly, NetlifyCMS

Prose sits above github

you can have people edit from withiin the repo

Choose the best tool fo the job, consider the requirements

There is a problem, NOT a productive way to work

WE generally get a set of preferred tools to solve most of the problems

Those don't solve every problem

Evaluate on preferred set of tools, choosing from prevetted tools

Evaluate? 

Cost, Pricing model, Support, SLA, SSO, SDK

Type(Api vs Git)

Editing Experience

Preview-abilityy

publishing workflow/scheduling

single instance models

Localization

image transformation

Some unknowables

What is the editing experience

what is the dev experience?

Meet your editors where they already are

if using WP, just maybe leverage WP with your front end

you get new tool in your belt

What content management system

What if the best CMS is NOT meant to be a CMS

Trello, Asana, Jira, 

Fauna, MongoDB, AWL

Spreadsheets? (DON"T DO IT THOUGH)

Dropbox, Backblaze, Drive, etc

local apps or editors, files

MD, YML, Bear editor, VSCode

Sandwich time!

seancdavis/everything-is-a-cms on github

Contentful as the CMS -  sandwiches

drop pages in the pages directory, 

demo of building simple page

good

until next project

now editors using Trello

talk to the Trello API instead of the Contentful API

works 

but we duplicated code

separate repos 

one file in example, silly

add it all up, so much to rewrite

eventually you would need to touch so many parts of an application

Data source are painful

How to minimize work on reworks?

Build an  engine that consumes data for your NextJS applications

drivers to support data sources

2 engines possible, file based and API based

wait, that is CMS...

API based transforms and makes available with REST or GraphQL

Better with working on dynamic/real-time data

File based pulls from various sources normalize it and write to files, 

Great for static

example of workflow for the app

no perfect data source for your project

evaluate based on criteria important to you and your project to find a balance
 between picking the best tool for the job and working efficiently

consider meeting your data and/or editors where they are, rather then moving
 all content into a single source

You may have to swap out or add data sources, thats OK, build an engine that
 processes and makes it less painful

no matter what though, remember above all else, have fun

{{< tweet 1321147635202445325 >}}

### [Why Real Time Matters](https://nextjs.org/conf/speakers/svale)
(Simen Svale Skogsrud)[https://twitter.com/svale]

This seemed to be a 'sponsored session' where we saw a demo of the new Sanity collaboration tools than a look at Real Time conceptually.  I have no issue with this, especially as it was a really well done demo. I walked away looking forward to testing Sanity.io and discussing it when the need for better content collaboration comes around on my team.  

Raw Notes:

Simen, Knut (dev Rel), Espen(dev)

Sanity demo

Visual editor, easy to manipulate

rich text type editor, but just json under the hood, easy to conceptualize from
 Dev perspective

no copy/paste weird markup - transportable as heck

Review changes are important

'how can we know' if reviewed changes?

Git diff like changes

Real time collaboration 

see what others are doing

not messing around too much in production for this demo

ecommerce studio demo next

watching changes happen between viewers is powerful for collab

how did they do it?

Map preview custom element

as an author and editor, how will it affect people and be interpreted

Demo site reflecting changes while working with editor

fastest preview

next-sanity tool kit

{{< tweet 1321152249859506176 >}}

### [How to Learn React/Next.js or Anything](https://nextjs.org/conf/speakers/arunoda)

[Arunoda Susiripala](https://twitter.com/arunoda)

I was kinda hoping this would have been more about the theory behind learning things in general. While that was covered and did give me valuable insight into his thought process as a student and as a teacher, it seemed more a commercial for his React training materials. I guess I was hoping for a study on instructional design and delivery theory.  Still, his three reasons why something is hard is something I will be keep in mind as I write docs, guides and instructional materials from here on out and focus on the 20% critical points rather than boiling oceans.  

Raw Notes:

How to learn these things

Why learning X is so hard

he is trying to learn something new everyday

1. Need Prior Info

2. Poor educational Content

3. overcomplicated API/UX

These are his observations not scientific research

blender FPS example - DAIN

he read whitepaper, math was beyond him

OK, let's apply this to React

1 - need to understand JS and web basics

2 - confusing educational content - so many peices of content, not all good,
 many outdated, hard to find good resources - using react classes vs hooks which
 is modern

3 - React is not that complex but issue is to many tools in the ecosystem,
 historical reasons obscure why you needed them, harder to learn alll the things

We need to understand 20% to get 80% done

We need a tutorial!

Just React course/tutorial

to get things done his way

deep dive on the first page, scares people

So many things you can learn about, where to start is the issue

diving into the most bare bones basics and moving from there

Next is practice

{{< tweet 1321170623025025030 >}}


### [(Choosing our own) Adventures in Next.js](https://nextjs.org/conf/speakers/cassidoo)

[Cassidy Williams](https://twitter.com/cassidoo)

If there was one person I was going to see 'live' at this event it was going to be one of the most awesome internet celebrities I follow on twitter. If you have not seen her amazing comedy video posts, you are missing out.  Turns out she is a great presenter too.  Something happened at some point in my note taking it it wiped out like the last 1/3 of my notes. That was the stuff with the code walk through and her awesome conclusion talking about how it is good to know CS basics when thinking through the logic of a problem, like she did with graphs. 

[Ya know what, just go watch this one. I will wait.](https://www.youtube.com/c/ZEITHQ/videos)

Raw Notes:

Working at Netlify

Choose your own adventure books for inspirations

Picking a data structure

Linked List?  No cause it is not linear

Trees?

Branching and so many choices 

BUT CYO adventures are not always in one direction

branches converge

Graph?

Any which way you want to go you navigate bouncing around

but we want to have specific paths

no undo button overuse, want to be specific

Directed Graph

graph with arrows, 

state machine, never in multiple states at once

"user input driven state machine"

now pick tools 

XState  - state machine lib

reducers 

+ React

+ NextJS

add crowdsourcing

Netlify forms

HTML + data=true - Netlify picks it up with a function

Hasura for the DB

and a spooooky story

Demooooo!

So much cool code. 

notes missing and conclusion oh no!

{{< tweet 1321180890832293889>}}


### [Building Next Generation Apps with Next.js and MongoDB](https://nextjs.org/conf/speakers/kukicado)

[Ado Kukic](https://twitter.com/kukicado)

Now normally, if I don't get to see the whole session I don't include it.  But this time, I am because the reason I didn't see the end should be shared. Lesson learned here: if you are watching a youtube live presentation and are a bit behind, when the live broadcast ends, so does your access to that vid.  Now, they did post it later but it was a jarring experience and I will avoid being behind on the last session from now on.  

What I did see though was interesting look at how to leverage Next.js and MongoDB, which I have never used before.  The examples were getting pretty deeply technical when it cut out. One to go back and rewatch later I guess.    


Raw Notes:

Don't like slides but

Why did devs like NextJS?

SSG and SSR?

Zero Config

File system routing 

API Endpoints to expose backend functionality

no one in isolation

it is something more

Related to the Dunning Krueger effect

Seems to know a lot, powerful, rock star from the initial look at the tutorial

then build real thing and feel dumb

then work through it and learn what you need

NextJS is a rare framework that is complex but so much attention to dev
 experience, it is suberb

easy to master and extend

MongoDB Atlas

not just a cloud DB

Atlas provides Lucene search

Serverless

Multicloud env.

code example

the app - property booking

connect booking to MongoDB

search and find experience for end user

and then it ends???

{{< tweet 1321196791015055360 >}}



## Wrapping Up

I had a great but exhausting time in this surprisingly short but jammed packed conference. The whole experience was only 5 hours, but it was a non-stop as fast as you could go 5 hours.  It informs me that online conferences can do more in smaller time frames than traditional conferences but the experience is so vastly different to the in person ones. I can't imagine going at this break neck speed if physically there, as there were no breaks, just 'bam' 'bam' 'bam' all day.  But for some reason this worked out well online and I felt engaged the whole time.  I would 100% attend again!  

