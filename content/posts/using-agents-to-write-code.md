+++
date = '2025-07-03T21:41:22+02:00'
draft = false
title = 'Using Agents to Write Code for repeatable tasks'
+++

Today, Armin Ronacher published [yet another post](https://lucumr.pocoo.org/2025/7/3/tools/) about agentic coding. This one primarily talks about the shortcomings of MCP with regards to tool selection and robustness. The introductory example is that using the Github CLI will be more token efficient, faster and stable used as a simple tool than the Github MCP server. The extension of this is that letting the LLM use a deterministic program will reliably beat LLM inference, which is not deterministic. This idea is not new, but in context of MCP and agentic systems it gains a new perspective for me.

An example that really brings this point home for me is using LLMs to convert a document from one format to another. At work I oftentimes convert from markdown to various Confluence and Jira dialects. Now LLMs are pretty good at that - however, you cannot be sure that there isn't also a change in wording besides the formatting adjustments. You definitely cannot rule it out, so you need to check or just hope for the best. The alternative approach is to let the LLM write code to accomplish the task instead. This can be done in an agentic loop with e.g. an LLM as a judge approach to validating that the output the written script or application produces is good enough. You gain reproducibility, speed and cost efficiency as well. So when you convert a document a second time, you do not need to involve an LLM at all for this - you may just mention to Claude to use your markdown-convert tool to produce the reformatted version and that's it. Bonus is that you can also call it yourself.

This definitely does not extend to all tasks - I sometimes use LLMs to transform e.g. print statements to logging statements. I guess that a program will have to handle an enormous amount of edge cases to properly work for this, but maybe I am wrong. I will try it.
