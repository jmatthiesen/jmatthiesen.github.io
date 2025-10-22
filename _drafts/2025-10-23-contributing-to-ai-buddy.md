---
title:  "Build a YouTube chat app with .NET"
date:   2024-12-16 17:00:00 +0000
classes: wide
category: Programming
tags:
- .NET AI
---
## A Note on Technology Choices

You might notice something interesting about this project: it's built primarily with Python, not .NET. The backend uses FastAPI, the data ingestion pipeline is Python-based, and I'm leveraging the rich Python AI ecosystem.

Why? Honestly, it came down to pragmatism. When I started this project, I wanted to use the OpenAI Agents SDK for multi-agent orchestration, and at the time, the Python version was significantly more mature than the .NET offerings. The Python ecosystem also has incredible tooling for vector search, embeddings, and document processing.

That said, this is a tool *for* .NET developers, built by a .NET developer. The knowledge base is entirely focused on C# and .NET AI development. And who knows - maybe a future version will be a full .NET rewrite once the ecosystem matures a bit more. For now, I'm focused on delivering value to the community, regardless of what tech stack powers it behind the scenes.

## Join Me in the Code

One of my core goals with this project is to learn in public and invite others to learn alongside me. The entire codebase is open source and available on GitHub at [github.com/jordanmatthiesen/csharp-ai-buddy-site](https://github.com/jordanmatthiesen/csharp-ai-buddy-site).

Whether you're curious about how to build production AI systems, want to understand vector search with MongoDB, or just want to see how FastAPI's streaming responses work, the code is there for you to explore.

And if you want to contribute? Even better! I'd love help adding more content sources to the data ingestion pipeline, improving the AI prompts, adding new features, or expanding the code samples gallery. This is a community project at heart.

Here's what you'll find in the repo:
- **FastAPI backend** with streaming AI responses using OpenAI Agents SDK
- **MongoDB vector search** for semantic document retrieval
- **Data ingestion pipeline** that automatically processes web content, blog posts, and RSS feeds
- **OpenTelemetry instrumentation** for observability
- **Arize integration** for feedback tracking and continuous improvement
- **Comprehensive documentation** including architecture guides and deployment instructions

If you're interested in learning how these pieces fit together, clone the repo and dig in. I've tried to document everything thoroughly, and I'm happy to answer questions.