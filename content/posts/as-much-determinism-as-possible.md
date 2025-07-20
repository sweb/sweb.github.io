+++
date = '2025-07-20T19:56:54+02:00'
draft = false
title = 'As Much Determinism as Possible'
+++

One of the main learnings of the last months has been that you should try to get as much determinism as possible into your agentic system. This is also true for agentic coding setups. The reason is that each inference step of the LLM has a chance to produce a wrong result. While this also happens with human developers, with current setup, this quickly compounds with each following interaction, as I have the impression that state of the art models still tend to dig deeper and deeper into their wrong solution, while developers will stop much earlier and reevaluate. The blog post [Why I'm Betting Against AI Agents in 2025](https://utkarshkanwat.com/writing/betting-against-agents/) has a section describing how this is not an edge case but a quite common problem once your agent requires more than a couple of steps to solve the problem.

The notion of handling as much as possible through deterministic code has been mentioned a couple of times in the last weeks, e.g. in the previously linked blog but also by [Armin Ronacher](https://lucumr.pocoo.org/2025/7/3/tools/). The idea is to:

* Enforce specific workflows, e.g. run tests after each file write via hooks in Claude Code
* Create specialized tools, e.g. convert markdown to Jira's special markdown via a script instead of letting the LLM do the transformation
* Create dedicated agents for clearly defined tasks, e.g. writing a function from associated context and specification

Another advantage is that the context of the main session can be kept smaller, as some parts are offloaded to dedicated tools.
