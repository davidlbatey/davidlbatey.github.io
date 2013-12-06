---
layout: main
category: productivity-hack
tags:
  - code
  - 5 hour
  - api
  - easy
---

I've been a bit quiet the last few months because I've been building an awesome new
application (well two actually) one for the brilliant Gleanin guys and one for myself. My new
app is www.Nickelled.com and it's raison d'être is to enable web apps to better
educate their users on how to interact on their site, with the assumption that
if the user knows how to correctly interact with the site then they're more likely to A. become
a customer and B. less likely to raise time consuming/expensive support requests. What
I wanted to discuss though wasn't the application but an architectual design decision
that I've made early on.

Right out of the gate I've pulled out the API and separated out other logical components
into their own small applications/services. I did this not because I expect to hit scale
any time soon but by having the APIs separate I will be able to offer a high level
of availability while rapidly changing and iterating sections of the applications
which are still under development and in flux.

I think that if I was trying to avoid premature optimization then I would have waited
until recieving complaints of dropped requests before separating the code or alternatively
I could have moved to a slower release schedule (e.g. nightly or weekly). Neither
of these alternatives sits well with me, with Nickelled I don't plan to offer a good
service but an exceptional one and I see delayed deployments as not reducing risk
but increasing it (topic for another post?) due to the build up of code and new libararies
that will be released.

Tweet me if you think I've made a heinous error, or if you have a better solution.
