---
layout: post
comments: true
title: A Podcast for You! And You! And You!
date: 2023-07-29 08:00:00
description: One small step for how LLMs are going to change your world
---
# A Podcast for You! And You! And You!

Imagine starting your day with a tailored podcast, containing summarized stories from various newspapers and websites that you care about. With advances in LLMs and Text-to-Speech, it is now possible to automate this process. Let's explore how to leverage AI to curate, summarize, and transform online stories into personalized podcasts.

To start, here's a sample podcast created on July 29, 2023.
{% include audio.html path="assets/mp3/hacker_news_podcast_jul_27_23.mp3.mp3" controls=true %}
{% include figure.html path="assets/img/hacker_news_page_270723.png" class="img-fluid rounded z-depth-1" zoomable=true %}

## Curating Online Stories

Our journey begins with curating the stories. We navigate to the URL of the website we're interested in and fetch the text content for processing.

```python
url = args.url
html = navigate(url)
formatted_text = textapi.scrape_text(html)
```

## Extracting and Selecting Topics
Once we have the formatted text, we can extract main topics and stories using LLMs - the [OpenAI Function Calling update](https://openai.com/blog/function-calling-and-other-api-updates) was particularly useful. This is done iteratively until we have a satisfactory selection of topics.

## Summarizing Stories and Discussions
Next we can summarize the main stories and discussions using ... LLMs. :-)

## Compiling the Podcast Script
With the summaries of the stories and discussions, we can now compile our podcast script using LLMs. The entire podcast is then put together with all the information gathered so far with a "producer" LLM step.

## Converting the Script into a Podcast
Finally, we convert the podcast script into an actual podcast. We first generate the audio for each text segment using [ElevenLabs' speech synthesis](https://elevenlabs.io/speech-synthesis).

And voila! You now have your personalized podcast, ready to play, with stories and discussions from your favorite online sources.

By leveraging AI technologies like OpenAI's GPT-4 for content curation and summarization, and ElevenLabs' text-to-speech for converting the script into a podcast, we can automate the process of creating personalized podcasts. It's an exciting time to explore the possibilities of AI in customizing and enhancing our consumption of online content.
