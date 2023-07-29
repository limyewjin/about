---
layout: post
comments: true
title: A Podcast for You! And You! And You!
date: 2023-07-29 08:00:00
description: One small step for how LLMs are going to change your world
---
Imagine starting your day with a tailored podcast, containing summarized stories from various newspapers and websites that you care about. With advances in LLMs and Text-to-Speech, it is now possible to automate this process. Let's explore how to leverage AI to curate, summarize, and transform online stories into personalized podcasts.

To start, here are sample podcasts created for a "tech user in the Bay Area" on July 29, 2023.

**Hacker News**
{% include audio.html path="assets/mp3/hacker_news_podcast_jul_27_23.mp3" controls=true %}
[Download the transcript for the sample podcast](assets/txt/hacker_news_podcast_jul_27_23.txt)

{% include figure.html path="assets/img/hacker_news_page_270723.png" class="img-fluid rounded z-depth-1" zoomable=true %}

**New York Times**
{% include audio.html path="assets/mp3/nytimes-podcast-290723.mp3" controls=true %}
[Download the transcript for the sample podcast](assets/txt/nytimes-podcast-transcript-290723.txt)

{% include figure.html path="assets/img/nytimes-podcast-290723.png" class="img-fluid rounded z-depth-1" zoomable=true %}

1. **Curating Online Stories:** We navigate to the website URL of interest and use AI tools to fetch and format the text content for processing.

2. **Extracting and Selecting Topics:** Once we have the formatted text, we use LLMs to extract main topics and stories. Thanks to OpenAI's function calling API update, this process can be executed iteratively until we have a satisfactory selection of topics.

3. **Summarizing Stories and Discussions:** The next step is summarizing the main stories and discussions, and LLMs come to the rescue again.

4. **Compiling the Podcast Script:** With the summaries, we compile our podcast script. The entire podcast is put together using a "producer" LLM step, which curates all the information gathered so far into a smooth-flowing narrative.

5. **Converting the Script into a Podcast:** Finally, we convert the podcast script into an actual podcast. We generate the audio for each text segment using [ElevenLabs' speech synthesis](https://elevenlabs.io/speech-synthesis). 

And voila! You now have your personalized podcast, ready to play, with stories and discussions from your favorite online sources.

By leveraging AI technologies like OpenAI's GPT-4 for content curation and summarization, and ElevenLabs' text-to-speech for converting the script into a podcast, we can automate the process of creating personalized podcasts. It's an exciting time to explore the possibilities of AI in customizing and enhancing our consumption of online content.
