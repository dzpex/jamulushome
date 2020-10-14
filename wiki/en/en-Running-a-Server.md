---
layout: wiki
title: "Running a Server"
lang: "en"
permalink: "/wiki/Running-a-Server"
---

# Running a Server

## Do I need to run a server to use Jamulus?

**Not if you don't want to.** You can just choose somebody else's server from your list and get going. 

**Don't want strangers interrupting?**  Once you and your friends are connected to a public server, press the "solo" buttons on the musicians each of you want to play with. Anyone you don't solo will see a "muted" icon on your channel. And you won't hear them. 

## That sounds too easy. I REALLY want to run one - what do I need to know?

### Server types

It's **very important** that you read and understand what type of server you want to run. **Please read the overview on [Server Types](Choosing-a-Server-Type)** then come back here.

### Speed and latency

**_The capability of the server itself (and the network it's on) is NOT the main determinant of the quality of a Jamulus session!_**

Many people attribute problems to the server that are in fact problems with the _client_. Much depends on the clients' [hardware](https://github.com/corrados/jamulus/wiki/Hardware-Setup), the networks that _they_ are on, and whether they are sticking to [Rule Number One](Getting-Started#having-trouble-cant-keep-in-time). There is therefore no guarantee that you will achieve lower latency or better overall performance by having your own server. 

If you plan to be playing regularly with the same people, **you are strongly advised** to first make sure that each member of the group is set up to use Jamulus properly. Do this by finding a public server with a reasonable ping time for all of you (20ms or less perhaps), all connect to that and work to fix any individual issues (verifying that they can [follow Rule Number One](Getting-Started#having-trouble-cant-keep-in-time) in particular). Use the solo technique above to prevent being interrupted if needed. 

Once any issues with musicians have been solved in this way, you can then investigate hosting your own server either at home or on a cloud host such as Amazon, which may result in better latency than servers run at home. For example, [see this guide](https://www.facebook.com/notes/jamulus-online-musicianssingers-jamming/howto-idiots-guide-to-installing-jamulus-server-on-amazon-aws-lightsail-ubuntu-i/507719749802976/) to using AWS Lightsail by Jamulus user [Simon Tomlinson](https://www.facebook.com/simon.james.tomlinson?eid=ARBQoY3KcZAtS3pGdLJuqvQTeRSOo4gHdQZT7nNzOt1oPMGgZ4_3GERe-rOyH5PxsSHVYYXjWwcqd71a) (_Facebook_) 

### Bandwidth - do you have enough?

A typical jam might have 4 people, for which you would need 200Kbps * 4 = 800Kbs (0.8Mbps) up and down. So if you have a 10Mbits down and 1Mbps up broadband connection, **you may start running out of bandwidth if a fifth player joins**, particularly if other musicians choose settings that increase their usage. You may want to [check that you have enough speed](https://fast.com) for that. [Read more about bandwidth use](Quality,-delay-and-network-bandwidth) at different quality settings. 

### In general

- Consider using a cloud host to get better ping times if you having problems

- Any server should have at least 1.6GHz CPU frequency and 1GB RAM

- Running a server may require you to adjust any firewalls running on or outside of your machine or cloud host. 

- Running a **private server at home** (but not a public one) will require you to [port forward](Running-a-Private-Server) on your router. 

- Jamulus doesn't currently support IPv6


# All OK? Get set up!

### [For Windows or Macintosh users](Server--Windows-&-Mac)
### [For Linux users](Server---Linux)
### [For Raspberry Pi](Server---Raspberry-Pi)

Server operators may also be interested in downloading [this set of useful tools](https://github.com/corrados/jamulus/tree/master/tools) from the Jamulus repository (clone the Git repo and also call `git submodule update --init`). 

# Having problems? Got issues?

See the [Server Troubleshooting FAQ](Server-Troubleshooting)


