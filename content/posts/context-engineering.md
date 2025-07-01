+++
date = '2025-07-01T21:48:57+02:00'
draft = false
title = 'Context Engineering'
+++

In the last days, the term *context engineering* as a replacement or maybe redefinition of *prompt engineering* has emerged. Philipp Schmid gives an overview about the topic in a recent [blog post](https://www.philschmid.de/context-engineering).
In summary, the idea is that proper LLM usage, especially in context of agentic workflows or systems, is less about this one magic prompt but more about deliberately choosing, what to put into the context of the LLM. This is particularly important when there is a lot of back and forth, e.g. due to chat interactions or a coding agent that works on a more complex tasks, needing to read multiple files with a broad context.

The [Hacker News comment section](https://news.ycombinator.com/item?id=44427757) on this blog post is quite extensive and discusses primarily:
* whether context engineering is indeed a better scoped definition than prompt engineering (everyone seems to agree that prompt engineering does not deserve the term *engineering*)
* how sensitive LLMs are to context, especially when newer models provide huge context lengths

It seems to be pretty clear that the right context makes a huge difference. Just focusing on the prompt is probably too narrow as a lot of usage patterns now include ways to expand the context dramatically so being deliberate about what and how to put e.g. source files or documentation into an LLM is even more important.
