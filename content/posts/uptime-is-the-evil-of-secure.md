---
title: "Uptime Is the Evil of Secure"
date: 2017-11-24T10:36:50-07:00
draft: false
---

Who hates uptime? If we’re talking system uptime, then yeah, this guy hates uptime. Service uptime? Love it. 

Metrics? Love those also. My favorite metrics are aggregates. I love single values that can tell a story. Uptime is one of the best aggregates. Uptime tells us the obvious: How long has it been up? It also tells us the not so obvious: How good are we at patching systems and how good are we at designing resilient services? Give me a list of system uptime and I can quickly identify the pets and the cattle. 

The cattle will have less than 60 days of uptime. The pets, they’ll have much higher uptime, maybe even years. Nobody is manually patching and rebooting cattle, we herd cattle with automation. The pets on the other hand, somebody has to negotiate the exact time and process to patch and reboot a pet. 

Pets are also snowflakes and maybe even landmines. Snowflakes are systems that were built with no documentation by somebody who has long departed. Landmines are snowflakes with configurations that can’t survive a reboot, but, the system has been running for years and nobody knows it. Landmines earn their title when something like Shellshock pops up and the system owner is forced to patch and reboot; That’s when we find out a critical configuration wasn’t saved to disk and we also had an undocumented dependency on this system that just took down production. 

If there’s one metric you should focus on for situation awareness, it’s uptime. Establish an uptime SLA: No system should be up for more than 30 days. This one SLA yields profound ROI. 30 day uptime enforcement rewards resilient design patterns: Configs are documented and/or automated and critical services can survive the failure of a single node. 

I often hear the argument “It doesn’t matter, the system isn’t connected to the internet” in my quest to lower uptime. OK, sure, maybe it doesn’t feel paramount today, but it’s going to feel painful if we have an incident. An incident will force the need to patch, reboot, or rebuild every system. Guess who’s going to be working around the clock to rebuild their pets when an incident occurs. The choice for lower uptime SLAs will pay dividends in an incident. 

Some of you may argue this issue is solved with containers. Containers solve many problems due to their immutable nature. Let’s not forget, containers are hosted on systems that require patches. Pets are rare in container environments but don’t fool yourself into thinking they’re not there. 

Disagree? I’d love to know why. Reach out or add a comment. 



