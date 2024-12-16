---
title:  "Build a YouTube chat app with .NET"
date:   2024-12-16 17:00:00 +0000
classes: wide
categories: .NET and AI
---
Recently on a trip for a tech conference I created a [YouTube chat app using .NET and AI](https://github.com/jmatthiesen/dotnet-ai-youtube-chat). This is part of my exploration into creating a larger app for chatting about .NET AI development (leveraging docs, presentations, and sample code my team has been working on at Microsoft).

![Terminal window showing the YouTubeChat console running, with a question asking "How do I chat with my own data using AI?"](/assets/images/2024-12-16-build-youtube-chatbot.png)

This approach was inspired by a great LangChain tutorial on freeCodeCamp [^1] that I followed when first learning about generative AI last year. I really liked it as a simple example, yet one that's useful for personal tools. If you're new to AI dev, that tutorial is a little dated now, but still worth checking out.

For an up-to-date overview of .NET + AI, I'd recommend checking out the [Building AI Applications fro Scratch (using .NET)](https://www.youtube.com/watch?v=7Rw_ciSh2Wk) video from my team at Microsoft. Which also happens to be the video I'm using as an example in this YouTube chat repo.

# How is this app built?
This sample is built using the following technology:
* [.NET 9](https://dotnet.microsoft.com/en-us/download/dotnet/9.0)
* [Microsoft.Extensions.AI](https://devblogs.microsoft.com/dotnet/introducing-microsoft-extensions-ai-preview/)
* The [OpenAI library for .NET](https://www.nuget.org/packages/OpenAI)
* Alternatively you can use a local AI model, using [OllamaSharp](https://www.nuget.org/packages/OllamaSharp)
* The [YouTubeTranscriptAPI](https://www.nuget.org/packages/Lofcz.Forks.YoutubeTranscriptApi) package, which is a .NET implementation of the Python [youtube-transcript-api](https://github.com/jdepoix/youtube-transcript-api) module

To "chat with YouTube" the application will:
1. Download the transcript of a YouTube video

2. Create vector embeddings for the content of the transcript
3. Take a question from the user and create embeddings of the question
4. Perform a similarity search by comparing embeddings and returning transcript items that match the question
5. Run a prompt through OpenAI (or a local model using Ollama) that will form a responses to the user's question, using the transcript matches as context

This is a pattern called Retrieval-Augmented-Generation (RAG), which is extremely common for including your own data in calls to LLMs (like OpenAI). You can learn more about the concept from this great [What is RAG article by IBM Research](https://research.ibm.com/blog/retrieval-augmented-generation-RAG), or check out the [Building AI Applications fro Scratch (using .NET)](https://www.youtube.com/watch?v=7Rw_ciSh2Wk) video mentioned above.

# Next steps
There's still work that could be done next with this example, which I'll explore in the future as I build out my bigger .NET + AI chat idea. The main thing is improving the quality of responses, which aren't great with audio transcripts alone:
* Include citations with links to specific moment in the video.
* Augment with additional data from authoritative sources, like the [GitHub repo for Microsoft.Extensions.AI](https://github.com/dotnet/extensions/tree/main/src/Libraries/Microsoft.Extensions.AI).
* [Use a vector database solution to persist embeddings](https://learn.microsoft.com/en-us/dotnet/ai/conceptual/vector-databases), instead of a temporary in-memory store and local files.

Let me know in the comments if you find this sample helpful - or if you have questions.