---
title: "Veterans Day, testing out AgilityCMS and manually deploying my first Netxt.js site anyhow"
date: 2020-11-11T13:45:53-06:00
---

I took most of Veterans Day off. I did not serve in the military myself, instead doing civil service through [Americorps](https://www.redcross.org/local/california/los-angeles/volunteer/americorps.html), but I am grateful for those who did go off to war and defend the ideals I get to enjoy. I like to review history of service on this day. Learning from history will hopefully help us all avoid mistakes in the future. So I canceled all my meeting and dedicated some time to reflection.  

## A Reddit rabbit hole

I also used the day to catch up on some reading from all the bookmarks I have been making lately. I was catching up on Reddit and came across a post that at first [seemed like a dev who found a neat tool](https://www.reddit.com/r/JAMstack/comments/jrz0wq/quick_nextjs_blog_starter_with_automatic/):

> Quick next.js blog starter with automatic deployment to Vercel and Preview
Hello! 📷 I just tried this quick next.js blog starter with automatic deployment to Vercel with headless CMS and Preview amd Page Management and boom Published - Live! wow it made me feel smart and efficient so fast :)))) 📷 just wanted to share... 📷 [https://agilitycms.com/starters](https://agilitycms.com/starters)


Then I noticed this was published by u/agility-cms. And I thought "OK, maybe this is a pull from a testimonial", so I clicked the link, read a little more.  When I could not find that quote anywhere on that page or on that site, a little suspicion set in that this might not be a legit quote. But I work in the world of marketing and decided to just try it for myself. 

## Overwhelmed by options

The link provided actually took me to a screen that made me choose between [Next.js](https://nextjs.org/) and [Gatsby](https://www.gatsbyjs.com/) for my blog site. Clicking on either took me to a landing page with a preview of the theme. From there it was to another page to generate the needed repository.  

As I was about to generate the repo, I noticed I could select other [SSGs](https://jamstack.org/generators/). Like a LOT of them; 29 static site generators listed plus an 'other' option. I had already picked Next.js when I read the Reddit post. Then I had to choose between Gatsby and Next. And then this many options? I love the freedom of choice but this overwhelmed me. As a curious person I started opening new tabs and reading about things like [Sapper](https://jamstack.org/generators/sapper/), [Docusaurus 1 and 2](https://jamstack.org/generators/docusaurus/), [Middleman](https://jamstack.org/generators/middleman/) and a few others I had not run across yet.  Not going to count these side adventures in my overall time estimate for building a site.  

As a tinkerer I am a little torn on this point. If I was a dev for a real project, I would just ignore all the others. But as someone trying to learn all I can I was sent on a path of learning many new things while I was attempting to focus on one thing.  There is good and bad to this.

Next, I generated a new repo. No issues. 

After that, I created a [Vercel](https://vercel.com/) account to 'install on my Github account'? I have granted read/write permissions before for other services, but I wondered 'what is it going to install exactly?' Maybe just poor wording? It seems on par with permissions I gave to Netlify, so i went to click Confirm.  

But at the bottom of the screen was "User Permission - Read access to emails".  I supposed from an automation standpoint this makes sense as emails contain sometimes needed auth codes but I am not sure I am comfortable with this. Only options are cancel or install.  Dear reader, I hit install without stopping to search for what this means and what security issues might happen. 

![Vercel app persmission screen to connect to github](https://i.imgur.com/fWloXYv.png)

Now, once again I was asked to confirm the repo I wanted to deploy.  All good.  

And I get to a.... wait for it.... "Error connecting to Vercel." Uh oh.  
So I backed out and went to my AgilityCMS dashboard.  It looked like I had my site working but there was a dashboard and a lot of links to decipher.  

I clicked 'View Site' expecting a preview URL on Vercel. Nope, I got a pop-up telling me "Production Domain Not Set - Click below to manage your channels and setup a production domain." I hit the "Manage Domain" button in that pop up and got taken to a rather intimidating screen to 'add a domain'.  

![production domain not set alert](https://i.imgur.com/7nFJBbH.png)

Meanwhile, I got the normal alert emails from new account spin up. The last one I got contained a list of my new preview URLs.  My mind says 'of course, DNS is hard and this is going to take a few minutes.' I made some more coffee and waited. After caffeination achieved, I hit all 3 of the links in the emails....
and saw 404, 404 and a 404.

## I was ~10 minutes in at this point. 

I think I had been through 12 screens altogether, not counting Reddit.  

I went back to the 'add a domain' button and attempted to configured my preview and live URLs.  It gave me the option of Custom or Vercel URLs, so I picked Vercel.  

I was thrown back to the screen that asks which repo I am trying to connect.  Like, what happened with the other deploy? But ok, no other option, so I tried to do it again. But I couldn't since that instance already exists.  

I looked at my Vercel account and there were the logs I was looking for. Highlighted were some warnings about `tailwind` and `url-loader` unmet dependencies (neither of which I know too well) but those weren't failures just warnings. Then is see it, Agility fails to load because of a missing GUID.  

![Vercel Log showing warnings](https://i.imgur.com/0TkfAgg.png)

## I was not too worried yet. 

After all, deploys can fail for a lot of reasons and with all new accounts connected to a new github repo, failures happen.  That's life.  

I tried a redeploy. Only to get the exact same log with different time stamp.  

I am around 15 minutes in and about to try and research GUID and AgilityCMS. I stop myself and think "ok, something went horribly wrong maybe because perhaps, Agility needed to pre-populate something to generate that GUID from an existing Vercel connection. By the way, 'stabbing in the dark' guessing is not the best place to be when debugging. 

I decided then to just start over with Vercel.  So I delete the Vercel instance of the site.  Now I should be able to reattach my AgilityCMS and have it build anew.  I also deleted the repo on Github entirely for this to work.  

## Then I tried to delete my instance from AgiltyCMS.  

I could not.  

I tried for a few minutes to do this and just could not. 4 google and duckduckgo searches later and found nothing. There has to be a simple way I am overlooking, which makes me feel kinda dumb. That is the opposite of what the Reddit post promised me. I sat there about to open a support request when I stopped myself. 

I was a little more than 30 minutes in at this point and I still didn't have a site. This was supposed to be a simple, quick demo site. So I decided to bail on the whole thing and start over 100% from the original link. 

## Exhale

I closed all the tabs I had been working in.  I tried again. This time I had all accounts set up and permission-ed. I immediately ran into my account limit of 1 free site with AgilityCMS. No option on deleting and now I can not test a new one.

So I am gave up on this approach.  Not the likely outcome the OP wanted me to have. I was frustrated and feeling a not the smartest to be honest.  

## Breath and think about what I was really trying to accomplish.

I still wanted a site with Next.js to poke around at. So I built and deployed one.  
Setting up my site locally, reading all the needed docs, making minor content edits and deploying it to Vercel took me **15 minutes** total. I had never, ever done any of that before this attempt either.  
[You can see that site here](https://next-js-demo-site.vercel.app/)

I felt really smart and accomplished after this step! Perhaps, in a way, that Reddit poster was right all along, just not about the AgiltyCMS part.  

## Conclusion: 

I took the day for myself so I could reflect on the valuable lessons of Veterans Day, of which there are many. If you want a great resource for history, I can not recommend a better source right now that [The History Guy on Youtube](https://www.youtube.com/channel/UC4sEmXUuWIFlxRIFBRV6VXQ).  

I also wanted a day to tinker and learn.  I learned a few things for sure:

* So far I love Next.js. 

* Tech will fail sometimes and that is OK. Patience is a virtue after all and 

* I do not know how to delete an instance from AgiltyCMS. 

* You can not deploy a second instance to AgiltyCMS for free.  

* Do not believe anything you read on Reddit that says something "made me feel smart and efficient so fast."


