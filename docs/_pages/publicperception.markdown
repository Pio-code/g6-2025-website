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

  <figcaption>
  
  Figure 1: Grey wolf and polar bear dominate total mentions across posts and comments.</figcaption>



   <img src="{{site.baseurl}}/assets/images/grafico_2.png" alt="Most mentioned species in posts"> 

   <figcaption>  
       
  Figure 2: Percentage distribution of species mentions in posts.</figcaption>

  <img src="{{site.baseurl}}/assets/images/grafico_3.png" alt="Most mentioned species in comments">
    <figcaption>
   
  Figure 3: Percentage distribution of species mentions in comments and posts.</figcaption>


  <h2>Focus on Comments</h2>
  <p>Within <strong>Reddit comments</strong>—the most interactive dimension of discourse—the concentration is even sharper:</p>
  <ul>
    <li><strong>Grey wolf (43.4%)</strong> and <strong>polar bear (40.5%)</strong> account for <strong>over 80% of species-related mentions</strong>.</li>
    <li>The remaining species collectively represent <strong>less than 15%</strong> of mentions.</li>
  </ul>
  <p>This suggests that <strong>outreach efforts</strong> can capitalize on <strong>flagship species</strong> to drive engagement, while also using them as entry points to promote <strong>lesser-known biodiversity</strong>.</p>

  <h2>Emotional Analysis: Sentiment and Emotion Classification</h2>
  <p>To assess the <strong>emotional framing</strong> of discussions, we applied a <strong>Transformer-based deep learning model</strong>:</p>
  <ul>
    <li><strong>DistilRoBERTa</strong> (<em>j-hartmann/emotion-english-distilroberta-base</em>), optimized for <strong>multi-class emotion detection</strong>.</li>
    <li>Each text was analyzed within a <strong>512-token context window</strong> to preserve semantic continuity.</li>
    <li>Emotions were categorized as: <strong>Anger, Fear, Joy, Neutral</strong>.</li>
  </ul>
  <p><strong>Key findings:</strong></p>
  <ul>
    <li><strong>Grey wolf:</strong> 18% anger, 12% fear—mainly tied to <strong>livestock predation</strong> and <strong>human-wildlife conflict debates</strong>.</li>
    <li><strong>Polar bear:</strong> Dominated by <strong>fear and sadness</strong>, often connected to <strong>climate crisis</strong> and <strong>endangered narratives</strong>.</li>
    <li><strong>Red fox:</strong> Mixed emotional profile (17.3% anger, 9.6% fear, 1.9% joy), largely from <strong>urban wildlife and photography discussions</strong>.</li>
    <li><strong>Red deer & Eurasian lynx:</strong> Mostly <strong>neutral (>70%)</strong>, with <strong>fear (19–20%)</strong> tied to <strong>road collisions</strong>.</li>
  </ul>
  <p>Overall, the discourse leans <strong>neutral to negative</strong>, with <strong>joy appearing rarely</strong>, primarily in <strong>observational or aesthetic contexts</strong>.</p>

  <img src="{{site.baseurl}}/assets/images/grafico_4.png" alt="Percentage distribution of anger, fear, joy, and neutral by species">
    <figcaption>
      
  Figure 4: Emotional tone distribution per species based on Reddit discussions.</figcaption>


  <h2>Word Cloud Analysis</h2>
  <p>The <strong>word cloud</strong> highlights the most frequent words from <strong>comments classified with fear or anger</strong>, providing a clear view of <strong>themes driving negative emotions</strong>. After stopword removal and lemmatization, three dominant clusters emerge:</p>
  <ol>
    <li><strong>Climate change and species survival:</strong> <em>climate, melting, endangered</em> (reflecting concern for polar bears).</li>
    <li><strong>Human-wildlife conflict:</strong> <em>wolf, bear, attack</em> (debates about safety and coexistence).</li>
    <li><strong>Underlying ecological interest:</strong> <em>wildlife, habitat</em> (continued engagement with conservation, even in negative-toned conversations).</li>
  </ol>

  <img src="{{site.baseurl}}/assets/images/wordcloud_1.svg" alt="Wordcloud Comments with Negative Emotions">
    <figcaption>
      
  Figure 4: World Cloud - Comments with Negative Emotions </figcaption>

  <h2>Implications and Applications</h2>
  <p>By combining <strong>text mining, NLP, Transformer-based modeling, statistical visualization, and thematic word cloud analysis</strong>, this study offers a <strong>data-driven perspective on public perception</strong> of European mammals. Findings can guide:</p>
  <ul>
    <li><strong>Awareness campaigns</strong>, leveraging <strong>emotional triggers</strong> around flagship species.</li>
    <li><strong>Conservation policy</strong>, aligning management priorities with <strong>societal concerns</strong>.</li>
    <li><strong>Educational outreach</strong>, using <strong>iconic animals</strong> (polar bear, grey wolf) as entry points to highlight <strong>broader biodiversity issues</strong>.</li>
  </ul>
</section>
