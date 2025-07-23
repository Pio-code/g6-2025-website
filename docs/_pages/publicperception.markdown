---
layout: default
title: "Public perception"
permalink: /publicperception.html
---

<section>
  <h1>Textual Analysis and Sentiment Insights on European Mammals</h1>

  <p>This section of the project <em>“Impacts of Climate Change on European Mammals”</em> focuses on the <strong>textual dimension of public perception</strong>, analyzing how key mammal species are discussed and perceived across online communities. Rather than studying ecological dynamics directly, this work leverages <strong>Natural Language Processing (NLP)</strong> and <strong>deep learning models</strong> to understand the <strong>tone, frequency, and thematic context</strong> of discussions involving these species, particularly on <strong>Reddit</strong>, one of the most active platforms for public discourse on environmental issues.</p>

  <p>The objective is twofold:</p>
  <ol>
    <li><strong>Quantify the visibility and prominence</strong> of each species across discussions (which species drive the majority of interactions).</li>
    <li><strong>Classify the emotional tone</strong> of conversations—detecting signals of fear, anger, or positive curiosity—using a Transformer-based deep learning model.</li>
  </ol>

  <p>By combining these insights, we can identify which species <strong>dominate the public narrative</strong>, which are <strong>symbolically tied to climate change concerns</strong>, and which generate <strong>positive engagement</strong> that can support awareness and conservation campaigns.</p>

  <h2>Species Analyzed</h2>
  <ol>
    <li>Polar bear (<em>Ursus maritimus</em>)</li>
    <li>Grey wolf (<em>Canis lupus</em>)</li>
    <li>Brown bear (<em>Ursus arctos</em>)</li>
    <li>Red fox (<em>Vulpes vulpes</em>)</li>
    <li>Red deer (<em>Cervus elaphus</em>)</li>
    <li>Roe deer (<em>Capreolus capreolus</em>)</li>
    <li>European hedgehog (<em>Erinaceus europaeus</em>)</li>
    <li>European mole (<em>Talpa europaea</em>)</li>
    <li>European otter (<em>Lutra lutra</em>)</li>
    <li>European wildcat (<em>Felis silvestris silvestris</em>)</li>
  </ol>

  <h2>Data Collection and Preprocessing Pipeline</h2>
  <p>To ensure a <strong>systematic and reproducible analysis</strong>, the workflow was structured into three key stages:</p>
  <ol>
    <li><strong>Reddit Data Extraction (Data Mining):</strong>
      <ul>
        <li>Retrieved up to <strong>5,000 posts and 5,000 comments</strong> using <strong>PRAW (Python Reddit API Wrapper)</strong>, covering the period <strong>2019–2024</strong>.</li>
        <li>Focused on relevant subreddits (<em>environment, sustainability, wildlife, conservation</em>) to reduce noise and exclude unrelated topics.</li>
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
        <li>Applied <strong>spaCy-based tokenization and lemmatization</strong>, keeping only <strong>nouns and adjectives</strong> to capture descriptive content.</li>
        <li>Removed punctuation and non-informative grammatical elements (articles, pronouns, conjunctions).</li>
        <li>Consolidated all cleaned data into a <strong>structured CSV dataset</strong> for analysis.</li>
      </ul>
    </li>
  </ol>

  <h2>Quantitative Insights: Mentions per Species</h2>
  <p><strong>Grey wolf (998 mentions)</strong> and <strong>polar bear (850 mentions)</strong> dominate the discourse, jointly accounting for <strong>over 70% of all mentions</strong>. In contrast, <strong>red deer (189 mentions)</strong> and <strong>red fox (178 mentions)</strong> receive moderate attention, while other species (lynx, hedgehog, mole, wildcat) are <strong>virtually absent</strong> with fewer than 50 mentions each.</p>
  <p>This reflects a typical trend in environmental communication, where <strong>iconic or controversial species attract disproportionate focus</strong>, while <strong>less conspicuous species remain underrepresented</strong>.</p>

   <img src="{{site.baseurl}}/assets/images/grafico_1.png" alt="Total mentions (posts + comments) per species">

  



   <img src="{{site.baseurl}}/assets/images/grafico_2.png" alt="Most mentioned species in posts"> 

   

  <img src="{{site.baseurl}}/assets/images/grafico_3.png" alt="Most mentioned species in comments">
    


  <h2>Focus on Comments</h2>
  <p>Within <strong>Reddit comments</strong>—the most interactive dimension of discourse—the concentration is even sharper:</p>
  <ul>
    <li><strong>Grey wolf (43.4%)</strong> and <strong>polar bear (40.5%)</strong> account for <strong>over 80% of species-related mentions</strong>.</li>
    <li>The remaining species collectively represent <strong>less than 15%</strong> of mentions.</li>
  </ul>
  <p>This suggests that <strong>outreach efforts</strong> can capitalize on <strong>flagship species</strong> to drive engagement, while also using them as entry points to promote <strong>lesser-known biodiversity</strong>.</p>

  <h2>Emotional Analysis: Sentiment and Emotion Classification</h2>
  
  <img src="{{site.baseurl}}/assets/images/Emotions.png" alt="Percentage distribution of anger, fear, joy, and neutral by species">
    

  <section>
  <h2>Emotional Analysis: Sentiment and Emotion Classification (Updated)</h2>
  <p>To better capture the <strong>emotional framing</strong> of Reddit discussions, we applied a 
  <strong>Transformer-based deep learning model</strong>, DistilRoBERTa 
  (<em>j-hartmann/emotion-english-distilroberta-base</em>), optimized for 
  <strong>multi-class emotion detection</strong>. Each text (post or comment) was analyzed 
  within a <strong>512-token context window</strong> to preserve semantic continuity and 
  prevent truncation.</p>

  <p>In this updated version, we focused on <strong>four emotions only</strong> — 
  <em>Anger, Fear, Joy, and Sadness</em> — <strong>excluding Neutral</strong> to emphasize 
  emotional content. The distribution (<strong>Figure X</strong>) reveals distinct 
  emotional patterns by species:</p>

  <ul>
    <li><strong>Grey wolf:</strong> Shows the <strong>highest overall negative sentiment</strong>, 
    with <strong>43.2% anger</strong>, <strong>29.6% fear</strong>, and <strong>22.1% sadness</strong>. 
    Most discussions center on <strong>livestock predation, safety concerns, and 
    human-wildlife conflicts</strong>, reflecting wolves’ controversial role in 
    conservation debates.</li>

    
  <li><strong>Roe deer:</strong> Exhibits <strong>49.1% fear</strong> and <strong>16.4% sadness</strong>, 
    mostly connected to <strong>road accidents and incidental encounters</strong>, rather than predator-related fear. 
    Joy is minimal (<strong>7.3%</strong>), indicating a largely negative framing.</li>

  <li><strong>Polar bear:</strong> Dominated by <strong>fear (36.4%)</strong> and 
    <strong>sadness (25.3%)</strong>, often tied to <strong>climate crisis narratives</strong> and 
    <strong>endangered status</strong> (keywords like “melting”, “climate”, “endangered”). 
    Joy remains low (<strong>11.5%</strong>).</li>

  <li><strong>Red fox:</strong> Displays a <strong>mixed profile</strong> — 
    <strong>38% anger</strong>, <strong>34% fear</strong>, but also <strong>12% joy</strong>, the 
    highest among species. Joy is mainly linked to <strong>urban sightings and 
    photography</strong>, while negative emotions stem from <strong>conflicts with humans and pets</strong>.</li>

  <li><strong>European mole and hedgehog:</strong> Hedgehog is strikingly 
    <strong>dominated by sadness (60%)</strong>, with very low anger and fear, possibly 
    reflecting a <strong>perceived vulnerability or threats</strong> (e.g., habitat loss). 
    Mole shows a more balanced mix, with <strong>33% fear</strong>, <strong>33% anger</strong>, 
    and <strong>16.7% joy</strong>, though based on fewer discussions.</li>

  <li><strong>Eurasian lynx and wildcat:</strong> While less discussed overall, 
    these species display <strong>substantial sadness (33%)</strong> and 
    <strong>fear (53.8% for lynx)</strong>, likely tied to <strong>rarity and human interactions</strong> 
    (lynx collisions or sightings).</li>
  </ul>

  <figure>
    <img src="{{ site.baseurl }}/assets/images/Emotions.png" alt="Emotional distribution by species" width="800">

<figcaption>
      
Percentage distribution of Anger, Fear, Joy, and Sadness by species (Neutral excluded). Species are sorted by overall negative emotions (Anger + Fear + Sadness).</figcaption>
  </figure>

  <h3>Overall Trends</h3>
  <p>The <strong>discourse is heavily negative</strong>, driven by 
  <strong>anger, fear, and sadness</strong>. 
  <ul>
    <li><strong>Anger</strong> is strongest for <strong>grey wolves (43%)</strong>, tied to 
    <strong>conflict</strong>.</li>
    <li><strong>Sadness</strong> peaks with <strong>hedgehogs (60%)</strong> and 
    <strong>polar bears (25%)</strong>, linked to <strong>vulnerability and climate threats</strong>.</li>
    <li><strong>Fear</strong> dominates for <strong>roe deer (49%)</strong> and 
    <strong>lynx (53.8%)</strong>, primarily due to <strong>human encounters</strong>.</li>
  </ul>
  <p><strong>Joy remains marginal</strong>, never exceeding <strong>12%</strong>, and appears mostly 
  in <strong>contextual appreciation (wildlife photography, casual observations)</strong> rather 
  than deep engagement.</p>

  <p>This analysis shows that <strong>online discourse around European mammals is primarily 
  conflict- and threat-driven</strong>, with emotional polarization strongest for 
  <strong>wolves (conflict)</strong> and <strong>polar bears (climate icon)</strong>, while 
  <strong>hedgehogs and moles evoke sympathy rather than controversy</strong>.</p>
</section>



  <h2>Word Cloud Analysis</h2>
  <p>The <strong>word cloud</strong> highlights the most frequent words from <strong>comments classified with fear or anger</strong>, providing a clear view of <strong>themes driving negative emotions</strong>. After stopword removal and lemmatization, three dominant clusters emerge:</p>
  <ol>
    <li><strong>Climate change and species survival:</strong> <em>climate, melting, endangered</em> (reflecting concern for polar bears).</li>
    <li><strong>Human-wildlife conflict:</strong> <em>wolf, bear, attack</em> (debates about safety and coexistence).</li>
    <li><strong>Underlying ecological interest:</strong> <em>wildlife, habitat</em> (continued engagement with conservation, even in negative-toned conversations).</li>
  </ol>

  <img src="{{site.baseurl}}/assets/images/wordcloud_1.svg" alt="Wordcloud Comments with Negative Emotions">
    <figcaption>
      
  World Cloud - Comments with Negative Emotions </figcaption>

  <h2>Implications and Applications</h2>
  <p>By combining <strong>text mining, NLP, Transformer-based modeling, statistical visualization, and thematic word cloud analysis</strong>, this study offers a <strong>data-driven perspective on public perception</strong> of European mammals. Findings can guide:</p>
  <ul>
    <li><strong>Awareness campaigns</strong>, leveraging <strong>emotional triggers</strong> around flagship species.</li>
    <li><strong>Conservation policy</strong>, aligning management priorities with <strong>societal concerns</strong>.</li>
    <li><strong>Educational outreach</strong>, using <strong>iconic animals</strong> (polar bear, grey wolf) as entry points to highlight <strong>broader biodiversity issues</strong>.</li>
  </ul>
</section>
