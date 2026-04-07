---
title: Weekly Engineering Log -  2026-14
date: 2026-04-06
draft: false
tags: []
description: ""
---
## Week of Sunday, March 29th 2026 To Saturday, April 4th 2026

To close out the discussion from [[weekly-review-1 | last week]] on secure by default AI agents, I decided to investigate further on permission controle through sandboxing.  Sal Kimmich's article [The Kernel Is Where Sovereignty Lives, and AI Agents Just Broke the Model](https://hackernoon.com/the-kernel-is-where-sovereignty-lives-and-ai-agents-just-broke-the-model?source=rss) dove into the history of access control in Linux system.  _The core assumption baked into every Unix system is that a process runs with the full authority of the user who launched it._ Meaning that current user group permission control cannot be safely apply on AI agents. The article introduce [nono prohects](https://github.com/always-further/nono) That wraps AI agent in a kernel-isolated sandbox.

Sandboxing have always been top of mind for me; not just for AI but also for all the different tools I use daily. Over the past year, supply chain attacks have been increasingly one of the biggest threat. So many open sources project, embedded in multiple pipelines or environment with high privileged access. While [defense in depth](https://en.wikipedia.org/wiki/Defense_in_depth_(computing)) might be the better approach to add guardrail on your environment, sandboxing can be the closest level of security to the tools/AI agent being used. Over the next few weeks, I am planning to explore this concept further. Stay tune !!