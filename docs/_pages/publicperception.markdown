---
layout: default
title: "Public perception"
vega: true
---

<!-- Intestazione -->
<div style="text-align: center; margin-bottom: 2rem;">
  <h1 style="margin-bottom: 0.3rem; font-size: 2.2rem; font-weight: 600; font-style: italic; letter-spacing: -0.5px;">
    Textual Analysis and Sentiment Insights on European Mammals
  </h1>
</div>

<!-- Introduzione -->
<div style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif; max-width: 800px; margin: 0 auto;">

  <p>This section of the project focuses on public perception, analyzing how different mammal species are discussed and perceived in the <strong>Reddit</strong> community. This work leverages <strong>Natural Language Processing (NLP)</strong> and <strong>deep learning models</strong> to understand the <strong>tone, frequency, and thematic context</strong> of discussions involving these species.</p>

  <p>The objective is twofold:</p>
  <ol>
    <li><strong>Quantify the visibility and prominence</strong> of each species across discussions (which species drive the majority of interactions).</li>
    <li><strong>Classify the emotional tone</strong> of conversations.</li>
  </ol>

  <p>By combining these insights, we can identify which species <strong>dominate the public narrative</strong> and which are <strong>symbolically tied to climate change concerns</strong>.</p>

  
<div style="display: flex; flex-direction: column; gap: 0.2rem; margin-top: 2.5rem; margin-bottom: 1.2rem; border-bottom: 1px solid #ddd; padding-bottom: 0.6rem;">
  <div style="font-size: 0.85rem; color: #777; text-transform: uppercase; letter-spacing: 0.8px;">
    Section
  </div>
  <div style="display: flex; align-items: center; gap: 0.6rem;">
    <h2 style="margin: 0; font-size: 1.55rem; font-weight: 700; font-family: Georgia, serif; color: #222;">
      <span style="font-size: 1.2rem;">🛠️</span> Data Collection and Preprocessing Pipeline
    </h2>
  </div>
</div>
  <p>To ensure a <strong>systematic and reproducible analysis</strong>, the workflow was structured into three stages:</p>
  <ol>
    <li><strong>Reddit Data Extraction:</strong>
      <ul>
        <li>Retrieved up to <strong>5,000 posts and 5,000 comments</strong> using <strong>PRAW (Python Reddit API Wrapper)</strong>, covering the period <strong>2019-2024</strong>.</li>
        <li>Focused on relevant subreddits – <em>climatechange, environment, sustainability, wildlife</em> – to exclude unrelated topics.</li>
      </ul>
    </li>
    <li><strong>Keyword Optimization:</strong>
      <ul>
        <li>Built an <strong>extended keyword set</strong> per species (scientific and common names, plural forms, synonyms, and multilingual variants) to maximize recall and minimize missed mentions.</li>
      </ul>
    </li>
    <li><strong>Linguistic Cleaning and NLP Preprocessing:</strong>
      <ul>
        <li>Removed duplicates, spam, promotional content, and links.</li>
        <li>Applied <strong>tokenization and lemmatization</strong>.</li>
        <li>Removed punctuation and non-informative grammatical elements (articles, pronouns, conjunctions).</li>
        <li>Consolidated all cleaned data into a <strong>structured CSV dataset</strong> for analysis.</li>
      </ul>
    </li>
  </ol>

  <h2>Quantitative Insights: Mentions per Species</h2>
  <p><strong>Grey wolf</strong> and <strong> polar bear</strong> dominate the discourse, jointly accounting for <strong>over 70% of all mentions</strong>. In contrast, <strong>red deer</strong> and <strong>red fox</strong> receive moderate attention, while other species (<strong> lynx, hedgehog, mole, wildcat</strong>) are <strong>virtually absent</strong> with just a few mentions each.</p>

  <p>This reflects a typical trend in environmental communication, where <strong>iconic or controversial species attract disproportionate focus</strong>, while <strong>less conspicuous species remain underrepresented</strong>.</p>

  <img src="{{site.baseurl}}/assets/images/grafico_2.png" alt="Mentions per species">
  <img src="{{site.baseurl}}/assets/images/grafico_1.png" alt="Species visibility over time">
  <img src="{{site.baseurl}}/assets/images/grafico_3.png" alt="Species mentions comparison">

  <p>Within <strong>Reddit comments</strong> – the most interactive dimension of discourse – the concentration is even higher:</p>
  <ul>
    <li><strong>🐺 Grey wolf (43.4%)</strong> and <strong>🐻 polar bear (40.5%)</strong> account for <strong>over 80% of species-related mentions</strong>.</li>
    <li>The remaining species collectively represent <strong>less than 15%</strong> of mentions.</li>
  </ul>

  <h2>Emotional Analysis: Sentiment and Emotion Classification</h2>
  <p>To better capture the <strong>emotional framing</strong> of Reddit discussions, we applied a 
  <strong>Transformer-based deep learning model</strong>, DistilRoBERTa 
  (<em>j-hartmann/emotion-english-distilroberta-base</em>), optimized for 
  <strong>multi-class emotion detection</strong>.</p>

  <p>We focused on <strong>four emotions only</strong>: 
  <em>Anger, Fear, Joy, and Sadness</em>. The distribution reveals distinct 
  emotional patterns by species:</p>

  <ul>
    <li><strong>🐺 Grey wolf:</strong> Shows the <strong>highest overall negative sentiment</strong>, 
      with <strong>43.2% anger</strong>, <strong>29.6% fear</strong>, and <strong>22.1% sadness</strong>. 
      Most discussions center on <strong>livestock predation, safety concerns, and 
      human-wildlife conflicts</strong>, reflecting wolves’ controversial role in 
      conservation debates.</li>

    <li><strong>🦌 Roe deer:</strong> Exhibits <strong>49.1% fear</strong> and <strong>16.4% sadness</strong>, 
      mostly connected to <strong>road accidents and incidental encounters</strong>. 
      Joy is minimal (<strong>7.3%</strong>).</li>

    <li><strong>🐻 Polar bear:</strong> Dominated by <strong>fear (36.4%)</strong> and 
      <strong>sadness (25.3%)</strong>, often tied to <strong>climate crisis narratives</strong> and 
      <strong>endangered status</strong> (keywords like “melting”, “climate”, “endangered”). 
      Joy remains low (<strong>11.5%</strong>).</li>

    <li><strong>🦊 Red fox:</strong> Displays a <strong>mixed profile</strong> — 
      <strong>38% anger</strong>, <strong>34% fear</strong>, but also <strong>12% joy</strong>, the 
      highest among species. Joy is mainly linked to <strong>urban sightings and 
      photography</strong>, while negative emotions may stem from <strong>conflicts with humans and pets</strong>.</li>

    <li><strong>🕳️ European mole and 🦔 hedgehog:</strong> Hedgehog is strikingly 
      <strong>dominated by sadness (60%)</strong>, with very low anger and fear, possibly 
      reflecting a <strong>perceived vulnerability or threats</strong> (e.g., habitat loss). 
      Mole shows a more balanced mix, with <strong>33% fear</strong>, <strong>33% anger</strong>, 
      and <strong>16.7% joy</strong>, though based on fewer discussions.</li>

    <li><strong>🧭 Eurasian lynx and 😺 wildcat:</strong> While less discussed overall, 
      these species display <strong>substantial sadness (33% for wildcat)</strong> and 
      <strong>fear (53.8% for lynx)</strong>, likely tied to <strong>rarity and human interactions</strong>.</li>
  </ul>

  <figure>
    <img src="{{ site.baseurl }}/assets/images/Emotions.png" alt="Emotional distribution by species" width="800">
  </figure>

  <h2>Word Cloud Analysis</h2>
  <p>The <strong>word cloud</strong> highlights the most frequent words from <strong>comments classified with fear, anger or sadness</strong>, indicating the <strong>themes driving negative emotions</strong>. The analysis suggests a recurring focus on climate-related concerns – often tied to species like the polar bear – alongside discussions around human-wildlife conflict, particularly involving wolves and bears. There also appears to be a persistent interest in broader ecological themes such as wildlife and habitat conservation.</p>

  <img src="{{site.baseurl}}/assets/images/wordcloud_1.svg" alt="Wordcloud Comments with Negative Emotions">

</div>
    
