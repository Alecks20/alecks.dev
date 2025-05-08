
+++
author = "Alecks"
title = "Pyro: my new beast of a home server build."
date = "2025-05-08"
description = ""
tags = [
    "linux","servers","homelab"
]
+++

I've always hated the cloud, expensive subscriptions, random terminations, no physical control over your data, the trust factor and more. Which is why I've built an abolute beast of a home server to run game servers and other services in docker containers.

## How this benefits you.

If your someone living in Australia (Where the servers hosted) **starting in 2026** I'm offering you a free small minecraft server (4-5gb ram, 2-3 threads), valheim server, terraria server or any game that isn't super resource intensive (Full access/control will be given by Pterodactyl Panel), just reach out to me via Discord or Email.

## Phyiscal hardware and specs.
 Below lists my hardware configuration with an explaination why I chose each part.

CPU: AMD Ryzen 5 5500

> Good value and reasonable price (AU$200), lots of threads for lots of game servers, power efficient and high performance.

Memory: 32GB (Upgrading to 64GB later on) DDR4 RAM

> Enough to run a large amount of game servers and docker containers without any worry of running out, the cost increase for DDR5 (And needing an AM5 cpu) wasn't worth it to me so I stuck with DDR4.

Storage: 1TB NVMe SSD (Backed up to Backblaze)

> Incredibly fast and cheap (AU$100), not really a reason to get anything else. Offsite backups are essential for storing important information with the risk of a fire or hardware failure.



## Networking, security and monitoring.
Ideally you'd aim against port forwarding but bandwidth in Australia is quite expensive and I have amazing fibre internet with built in dos protection and unlimited data so I port forward only game server ports (No remote access services)

To secure my home network locally I block the server from connecting to any devices locally and only allow other local devices to connect to *it* (such as my computer for portainer or ssh), this stops anyone who hacks it through the internet from gaining access to my home network.

For resource and uptime monitoring I use [HetrixTools](https://hetrixtools.com), an amazing free monitoring service with a server monitor that story history of cpu, ram, storage and bandwidth usage and monitors from 4 different locations at once.