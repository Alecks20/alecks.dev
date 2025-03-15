
+++
author = "Alex"
title = "Oracle cloud is a horrible platform."
date = "2024-03-10"
description = ""
tags = [
    "linux","servers","oracle","rant"
]
+++
For quite a while I used to use oracle cloud to host pretty much all of my stuff, from minecraft servers, to self hosted storage solutions and much more.

I signed up for the platform on April 20th 2023, and ended up leaving/being terminated from the platform for literally no reason at all on the 29th of November, I ran 2 oracle cloud accounts and only 1 of them was terminated so I continued using the platform until late 2023 (around December) when I left the platform for good

## Random Termination 
When my account was terminated, I received ZERO communication from oracle about it, the only way I found out about it is my uptime monitor notified me about my server going offline and me trying to figure out the cause. While doing this I found that my dashboard was broken. Every page on it said “Permission denied” or something along those lines. Nothing said my account was terminated until I googled the cause and found a reddit post talking about having the exact same thing happening to them.

The weird thing about this is the fact that I didn’t do anything wrong and even if I did I should have at least been notified about it, thankfully I wasn’t storing anything important on it but if I was then a ton of my stuff would have been completely wiped.

To make the situation even worse, I couldn’t even contact support about the issue because you needed an “Active Tenancy” to use the support service but since my account was terminated/disabled I couldn’t access it, I couldn’t even use the live chat on the dashboard because you needed a premium plan to talk to a real person on it.

There are a few things I thought off that could’ve got my account terminated in the first place, but its impossible to know because they didn’t give me any information about it

- Since I ran a minecraft server off it, there would constantly be people spamming the ports of my server from server scanners. This also connects to the fact that a lot of people who have had this happen to them before also ran minecraft servers off their oracle cloud servers.
- When trying to upgrade my server to a PAYG account (Which is like oracle’s “paid” service, if you don’t upgrade then you can’t go over the free tier limits) oracle randomly said my card was invalid and removed it from my account, even though the card was perfectly fine and it was also the same one I used at signup.

## “Closing” my account
Another issue I have with oracles cloud service is that when you “delete” a tenancy (An account) it doesn’t actually delete ANYTHING, it just disables it putting it under the illusion that its gone. You can even still login to the account and access the dashboard. I disabled my other oracle cloud account expecting to be able to sign up for it again once the old one was deleted and change the home region, however im still waiting to this day 4 months later for it to fully delete and it hasn’t yet and im not expecting it to at all.

So that is why I will not ever be returning to this horrible cloud provider, their offering is tempting but you should outright avoid it unless your hosting non-critial workloads, and even then keep backups on a 3rd party service.
