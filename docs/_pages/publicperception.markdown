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

  <p>This section of the project focuses on public perception, analyzing how different mammal species are discussed and perceived in the <strong>Reddit</strong> community. This work leverages <strong>Natural Language Processing (NLP)</strong> and <strong>deep learning models</strong> to understand the tone, frequency, and thematic context of discussions involving these species.</p>

  <p>The objective is twofold:</p>
  <ol>
    <li><strong>Quantify the visibility and prominence</strong> of each species across discussions (which species drive the majority of interactions).</li>
    <li><strong>Classify the emotional tone</strong> of conversations.</li>
  </ol>

  <p>By combining these insights, we can identify which species dominate the public narrative and which are symbolically tied to climate change concerns.</p>

  
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
  <p>To ensure a systematic and reproducible analysis, the workflow was structured into three stages:</p>
  <ol>
    <li><strong>Reddit Data Extraction:</strong>
      <ul>
        <li>Retrieved up to <strong>5,000 posts and 5,000 comments</strong> using <strong>PRAW (Python Reddit API Wrapper)</strong>, covering the period <strong>2019-2024</strong>.</li>
        <li>Focused on relevant subreddits – <em>climatechange, environment, sustainability, wildlife</em> – to exclude unrelated topics.</li>
      </ul>
    </li>
    <li><strong>Keyword Optimization:</strong>
      <ul>
        <li>Built an extended keyword set per species (scientific and common names, plural forms, synonyms, and multilingual variants) to maximize recall and minimize missed mentions.</li>
      </ul>
    </li>
    <li><strong>Linguistic Cleaning and NLP Preprocessing:</strong>
      <ul>
        <li>Removed duplicates, spam, promotional content, and links.</li>
        <li>Applied tokenization and lemmatization.</li>
        <li>Removed punctuation and non-informative grammatical elements (articles, pronouns, conjunctions).</li>
        <li>Consolidated all cleaned data into a <strong>structured CSV dataset</strong> for analysis.</li>
      </ul>
    </li>
  </ol>

  <div style="display: flex; flex-direction: column; gap: 0.2rem; margin-top: 2.5rem; margin-bottom: 1.2rem; border-bottom: 1px solid #ddd; padding-bottom: 0.6rem;">
  <div style="font-size: 0.85rem; color: #777; text-transform: uppercase; letter-spacing: 0.8px;">
    Section
  </div>
  <div style="display: flex; align-items: center; gap: 0.6rem;">
    <h2 style="margin: 0; font-size: 1.55rem; font-weight: 700; font-family: Georgia, serif; color: #222;">
      <span style="font-size: 1.2rem;">📊</span> Quantitative Insights: Mentions per Species
    </h2>
  </div>
</div>
  <p><strong>Grey wolf</strong> and <strong> polar bear</strong> dominate the discourse, jointly accounting for over 70% of all mentions. In contrast, <strong>red deer</strong> and <strong>red fox</strong> receive moderate attention, while other species (lynx, hedgehog, mole, wildcat) are virtually absent with just a few mentions each.</p>

  <p>This reflects a typical trend in environmental communication, where iconic or controversial species attract disproportionate focus, while less conspicuous species remain underrepresented.</p>

  <img src="{{site.baseurl}}/assets/images/grafico_2.png" alt="Mentions per species">
  <img src="{{site.baseurl}}/assets/images/grafico_1.png" alt="Species visibility over time">
  <img src="{{site.baseurl}}/assets/images/grafico_3.png" alt="Species mentions comparison">

  <p>Within <strong>Reddit comments</strong> – the most interactive dimension of discourse – the concentration is even higher:</p>
  <ul>
    <li><strong>🐺 Grey wolf (43.4%)</strong> and <strong>🐻 polar bear (40.5%)</strong> account for over 80% of species-related mentions.</li>
    <li>The remaining species collectively represent less than 15% of mentions.</li>
  </ul>

  <div style="display: flex; flex-direction: column; gap: 0.2rem; margin-top: 2.5rem; margin-bottom: 1.2rem; border-bottom: 1px solid #ddd; padding-bottom: 0.6rem;">
  <div style="font-size: 0.85rem; color: #777; text-transform: uppercase; letter-spacing: 0.8px;">
    Section
  </div>
  <div style="display: flex; align-items: center; gap: 0.6rem;">
    <h2 style="margin: 0; font-size: 1.55rem; font-weight: 700; font-family: Georgia, serif; color: #222;">
      <span style="font-size: 1.2rem;">💬</span> Emotional Analysis: Sentiment and Emotion Classification
    </h2>
  </div>
</div>
  <p>To better capture the <strong>emotional framing</strong> of Reddit discussions, we applied a 
  <strong>Transformer-based deep learning model</strong>, DistilRoBERTa 
  (<em>j-hartmann/emotion-english-distilroberta-base</em>), optimized for 
  multi-class emotion detection.</p>

  <p>We focused on <strong>four emotions only</strong>: 
  <em>Anger, Fear, Joy, and Sadness</em>. The distribution reveals distinct 
  emotional patterns by species:</p>

  <ul>
    <li><strong>🐺 Grey wolf:</strong> Shows the highest overall negative sentiment, 
      with 43.2% anger, 29.6% fear and 22.1% sadness. 
      Most discussions center on livestock predation, safety concerns, and 
      human-wildlife conflicts, reflecting wolves’ controversial role in 
      conservation debates.</li>

    <li><strong>🦌 Roe deer:</strong> Exhibits 49.1% fear and 16.4% sadness, 
      mostly connected to road accidents and incidental encounters. 
      Joy is minimal (7.3%/).</li>

    <li><strong>🐻 Polar bear:</strong> Dominated by fear (36.4%) and 
      sadness (25.3%), often tied to climate crisis narratives and 
      endangered status(keywords like “melting”, “climate”, “endangered”). 
      Joy remains low (11.5%).</li>

    <li><strong>🦊 Red fox:</strong> Displays a mixed profile — 
      38% anger,34% fear, but also 12% joy, the 
      highest among species. Joy is mainly linked to urban sightings and 
      photography, while negative emotions may stem from conflicts with humans and pets.</li>

    <li><strong>🕳️ European mole and 🦔 hedgehog:</strong> Hedgehog is strikingly 
      dominated by sadness (60%), with very low anger and fear, possibly 
      reflecting aperceived vulnerability or threats (e.g., habitat loss). 
      Mole shows a more balanced mix, with 33% fear, 33% anger, 
      and 16.7% joy, though based on fewer discussions.</li>

    <li><strong>🧭 Eurasian lynx and 😺 wildcat:</strong> While less discussed overall, 
      these species display substantial sadness (33% for wildcat) and 
      fear (53.8% for lynx), likely tied to rarity and human interactions.</li>
  </ul>

  <figure>
    <img src="{{ site.baseurl }}/assets/images/Emotions.png" alt="Emotional distribution by species" width="800">
  </figure>

<p>At a general level - beyond comments explicitly mentioning specific species - there is a noticeable prevalence of negative sentiment.
This trend appears to reflect a general perception of environmental degradation and human impact on the planet.</p>

<figure>
    <img src="{{site.baseurl}}/assets/images/dist.svg" alt="Emotional distribution by species" width="800">
  </figure>

 <div style="display: flex; flex-direction: column; gap: 0.2rem; margin-top: 2.5rem; margin-bottom: 1.2rem; border-bottom: 1px solid #ddd; padding-bottom: 0.6rem;">
  <div style="font-size: 0.85rem; color: #777; text-transform: uppercase; letter-spacing: 0.8px;">
    Section
  </div>
  <div style="display: flex; align-items: center; gap: 0.6rem;">
    <h2 style="margin: 0; font-size: 1.55rem; font-weight: 700; font-family: Georgia, serif; color: #222;">
      <span style="font-size: 1.2rem;">☁️</span> Word Cloud Analysis
    </h2>
  </div>
</div>
  <p>The <strong>word cloud</strong> highlights the most frequent words from comments classified with fear, anger or sadness, indicating the <strong>themes driving negative emotions</strong>. The analysis suggests a recurring focus on climate-related concerns – often tied to species like the polar bear – alongside discussions around human-wildlife conflict, particularly involving wolves and bears. There also appears to be a persistent interest in broader ecological themes such as wildlife and habitat conservation.</p>

  <img src="{{site.baseurl}}/assets/images/wordcloud_1.svg" alt="Wordcloud Comments with Negative Emotions">

</div>
    
