---
title:  "Announcing C# AI Buddy: Your Assistant for Building AI Solutions with .NET"
date:   2025-10-21 17:00:00 +0000
classes: wide
category: Programming
tags:
- .NET AI
---
Today, I'm happy to share an early preview of C# AI Buddy - an AI assistant you can "hire" to help you build AI projects using C# and .NET.

**Want to try it out?** You can get started right away at [csharpaibuddy.com](https://csharpaibuddy.com) using the preview key: `PREVIEW2025`

{: .align-center style="width: 50%"}
{% include figure popup=true image_path="/assets/images/2025-10-21-announcing-csharp-ai-buddy-intro.png" alt="C# AI Buddy Screenshot, showing a chat box followed by links to samples, news, and chat." %}


This is a proof of concept right now, and I could really use your help – please try it out share feedback, and rate the AI responses (with comments)!

## Why I Built This

I decided to build C# AI Buddy, not just as a tool for myself, but as a way to help the entire .NET community navigate this rapidly evolving space. And along the way, I'd level up my own skills in building production AI systems.

I'm a big fan of coding assistants (I used several in building this very site), but they don't offer great advice when building AI solutions with C# and .NET. I want up to date and prescriptive guidance so that I don't have to spend so much time fact checking the assistant.

My goal for C# AI Buddy: **cut C# AI development time in half**.

## What C# AI Buddy Does

Let me walk you through the core functionality:

### AI Chat Assistant

The heart of C# AI Buddy is the conversational AI chat interface. You can ask questions about any aspect of building AI solutions with C# and .NET. The system uses OpenAI models combined with a curated knowledge base of .NET AI documentation, blog posts, and official resources.

What makes it unique is the filter system. Before you ask a question, you can tell the AI what you're working with:
- **.NET Version**: .NET 7, 8, or 9
- **AI Library**: Microsoft Agent Framework, Semantic Kernel, ML.NET, AutoGen, Microsoft.Extensions.AI, or others
- **AI Provider**: OpenAI, Azure OpenAI, Anthropic, Google, or local models

This context helps the AI provide more relevant answers and code examples that actually match your environment.

{: .align-center style="width: 50%"}
{% include figure popup=true image_path="/assets/images/2025-10-21-announcing-csharp-ai-buddy-assistant.png" alt="Chat window showing the question 'How do I create an MCP Server?' followed by a response." %}

### Code Samples Gallery

I've been aggregating code samples from across the .NET AI community - GitHub repos, blog posts, official Microsoft samples, and more. You can browse by framework, search for specific patterns, and find working examples to learn from.

{: .align-center style="width: 50%"}
{% include figure popup=true image_path="/assets/images/2025-10-21-announcing-csharp-ai-buddy-samples.png" alt="A Search field followed by a List of samples like 'customer support' and 'eShopLite'" %}

Each sample includes author attribution, source links, and tags so you can quickly filter to what matters for your project.

### .NET AI News Feed

Keeping up with the latest developments in the .NET AI space is exhausting. C# AI Buddy automatically monitors RSS feeds from Microsoft DevBlogs, community blogs, and other sources to bring you the latest articles and announcements.

Each article includes an AI-generated summary, so you can quickly decide if it's worth diving deeper.

## Try It Today

I'm opening up the C# AI Buddy proof of concept for early feedback today. You can start using it right now at [csharpaibuddy.com](https://csharpaibuddy.com) with the preview key:

**`PREVIEW2025`**

Just enter that key when prompted, and you'll have full access to all features. I'd love to hear what you think - please [share feedback](https://github.com/jmatthiesen/csharp-ai-buddy-site/issues/new?labels=feedback&template=feedback.md) about what works well, what doesn't, and what features you'd like to see added.

## What's Next?

I've got a long list of improvements I'd like to add to the site, at the top of my list:
- Support MCP as a way to access the knowledgebase
- Expanded code samples from more community sources
- Improving quality through AI evaluations based on user feedback
- Add suggestions for prompt & follow-up questions
- Experiment with integrating web search results

But I need your help to prioritize. What would make C# AI Buddy more valuable for you? What questions does it answer poorly today? What features would you use every day?

---

*Want to dive into the code? Check out the [GitHub repository](https://github.com/jmatthiesen/csharp-ai-buddy-site) to see how it's built and contribute your own improvements. Look for a follow-up post coming soon, with some architectural details.*