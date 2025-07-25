---
title: LLM Context Farming
---
The most profound shift in my workflow isn't a new productivity app or a fancy monitor. It's the realization that my primary productivity tool is now just a collection of ongoing conversations with LLMs. This is a form of context farming: cultivating multiple, independent project contexts that I can dip in and out of with zero ramp-up time. The cognitive tax on switching between wildly different tasks was a cost we all just accepted. Now, that tax has been effectively eliminated. True multitasking, the kind the experts told us for years was a myth, is now not only possible but shockingly effective. The baseline for productivity has been redrawn, and the tools we used just a couple of years ago feel like they're built for a different cognitive era.

<!-- more -->

One example is maintaining this website. It uses Zola internally with a template I created myself, as it didn't look that complex to create one from scratch. Nowadays, I've gotten into the mindset that if I see something I don't like on the layout, I open a Gemini CLI terminal and just dive into it.

The old way was a familiar ritual. First, the blank stare at the screen. Then, the obligatory pilgrimage to Google, spelunking through the top five search results, then battling the cognitive friction of cookie popups, SEO-optimized drivel and autoplaying videos. Just to realize it's still not clear how to achieve what I want and heading down to the official Zola documentation to find the correct concept and term they use for the simple thing I want to build. Now, the process is brutally efficient. I open the Gemini CLI, provide Zola's documentation as context, and just ask for what I want in my own terms. Gemini is happy to chug through my problem in seconds, and I'm happy I didn't have to build context just for this single task.

My knowledgebase directory is nothing fancy. It's just a folder of Markdown files. It serves as a hand-curated cheat sheet for when the LLM inevitably gets confused about an API, which still happens from time to time.

A quick prompt is usually all it takes to get things back on track.

```
The API you're using is incorrect and causing a compile error.
Please refer to @knowledgebase/zola.md to understand the
right way to do this and try again.
```

This points to a weird new consequence: the most time-consuming part of a project is now just finding good documentation in a clean, Markdown format. There's a movement to provide a `/llms.txt` for this very purpose, but I've barely seen it adopted. So for now, I rely on tools like repomix to convert a whole GitHub subtree into markdown or websites that can scrape a set of pages into a single file. The bottleneck has shifted from understanding the code to just feeding the machine's context properly. It points to an inevitable conclusion: websites built for documentation and specifications will have to offer more than just HTML. Their new primary audience isn't human eyes, but LLM contexts, and the most valuable documentation will be the easiest to feed to a machine.

This superpower isn't just for code. Take a recent project: reverse-engineering the reMarkable e-reader Cloud API. The device is wonderfully hackable, but the community desperately needs better documentation. My goal was to create a proper, RFC-style specification for this API as a way to help myself create a client for it for a personal project. I started by feeding Gemini a massive prompt: the document's purpose, a trove of request/response pairs captured from their official client, and code excerpts from existing client libraries. Crucially, I demanded a specific output: strict RFC format and, most importantly, an "Open Questions" section to flesh out every ambiguity.

What I got back wasn't a finished spec, but it was a hell of a good start. It provided a solid structure and a focused list of exactly what to investigate next. My workflow became a loop: from time to time I'd revisit the same conversation, feeding it more context based on the open questions, like new request/response captures from the official clients, or more code examples, or refined explanations.

But the real impact is this: re-engagement friction is gone. Projects that would have died are now perpetually active. My chat history is the proof. A half-dozen deep conversations running in parallel, which I can dip in and out of at will. We've spent years being told true multitasking is a myth. Maybe we just had the wrong tools. Maybe we're the generation that finally, accidentally, made it work.