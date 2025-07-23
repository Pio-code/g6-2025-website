---
layout: default
title: "Public perception"
permalink: /publicperception.html
---

<section class="analysis-section">
  <h1>Textual Analysis and Sentiment Insights on European Mammals</h1>

  <p>This study is part of the broader project <em>“Impacts of Climate Change on European Mammals”</em>, which aims to estimate how suitable habitats for key mammal species will shift in the coming decades.
  In addition to ecological modeling (SDMs – <strong>Species Distribution Models</strong> – using <strong>MaxEnt</strong> to project present and future habitat suitability based on bioclimatic and environmental variables), the project integrates a <strong>social and communicative dimension</strong>: understanding how these target species are perceived and discussed in online communities, specifically on <strong>Reddit</strong>.
  The goal of this component is not only to quantify how frequently these species are mentioned but also to assess the emotional tone associated with these conversations (fear, anger, curiosity, admiration). This allows us to identify which species attract the most attention, which are primarily linked to climate-related concerns, and which spark positive interest that can be leveraged for awareness campaigns and conservation efforts.</p>

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
  <ol>
    <li><strong>Reddit Data Extraction (Data Mining):</strong>
      <ul>
        <li>Utilized the <strong>PRAW</strong> (Python Reddit API Wrapper) to access public Reddit data.</li>
        <li>Collected up to 5,000 posts and 5,000 comments across all species keywords, focusing on the period 2019–2024 to capture a relevant and sizable dataset.</li>
        <li>Targeted topical subreddits: <em>environment</em>, <em>sustainability</em>, <em>wildlife</em>, and <em>conservation</em>, excluding unrelated communities to reduce noise.</li>
      </ul>
    </li>
    <li><strong>Keyword Optimization:</strong>
      <ul>
        <li>Developed a comprehensive multilingual and morphologically expanded keyword set for each species, including:
          <ul>
            <li>scientific and common names,</li>
            <li>singular and plural forms,</li>
            <li>commonly used synonyms and abbreviations.</li>
          </ul>
        </li>
        <li>This approach minimized data loss due to linguistic variations and improved retrieval accuracy.</li>
      </ul>
    </li>
    <li><strong>Linguistic Cleaning and Normalization (NLP Preprocessing):</strong>
      <ul>
        <li>Removed duplicates, spam, promotional content, and external links.</li>
        <li>Applied tokenization and lemmatization using <strong>spaCy</strong>, retaining only nouns and adjectives (to focus on descriptive content) while discarding less informative grammatical elements (articles, pronouns, conjunctions).</li>
        <li>Stripped punctuation and symbols for standardization.</li>
        <li>Consolidated all posts and comments into a unified CSV dataset for analysis.</li>
      </ul>
    </li>
  </ol>

  <h2>Quantitative Insights: Mentions per Species</h2>
  <p>The first stage focused on measuring how frequently each species is discussed across Reddit conversations.</p>
  <figure>
    <img src="/assets/images/grafico1.png" alt="Total mentions (posts + comments) per species">
    <figcaption>Figure 1: Grey wolf and polar bear dominate total mentions across posts and comments.</figcaption>
  </figure>
  <figure>
    <img src="/assets/images/grafico2.png" alt="Most mentioned species in posts">
    <figcaption>Figure 2: Percentage distribution of species mentions in posts.</figcaption>
  </figure>
  <figure>
    <img src="/assets/images/grafico3.png" alt="Most mentioned species in comments">
    <figcaption>Figure 3: Percentage distribution of species mentions in comments.</figcaption>
  </figure>

  <h2>Emotional Analysis: Sentiment and Emotion Classification</h2>
  <p>We used a context-aware deep learning model to assess the emotional tone of these discussions:</p>
  <ul>
    <li><strong>DistilRoBERTa</strong> (<em>j-hartmann/emotion-english-distilroberta-base</em>), a Transformer-based model optimized for multi-class emotion classification.</li>
    <li>Each text (post and comment) was analyzed within a 512-token window to preserve context and avoid truncation.</li>
    <li>Emotions were categorized into four primary classes plus neutrality: <em>Anger</em>, <em>Fear</em>, <em>Joy</em>, and <em>Neutral</em>.</li>
  </ul>
  <figure>
    <img src="/assets/images/grafico4.png" alt="Percentage distribution of anger, fear, joy, and neutral by species">
    <figcaption>Figure 4: Emotional tone distribution per species based on Reddit discussions.</figcaption>
  </figure>

  <h2>Implications and Applications</h2>
  <p>This integrated approach—combining <strong>data mining</strong>, <strong>NLP</strong>, <strong>Transformer-based deep learning</strong>, and <strong>statistical visualization</strong>—provides a unique perspective on public perception of European mammals. Insights can guide:</p>
  <ul>
    <li>Awareness and outreach campaigns, prioritizing species that evoke strong emotions (concern or empathy).</li>
    <li>Conservation policy and management by aligning ecological priorities with public sentiment.</li>
    <li>Educational materials leveraging iconic species (polar bear, grey wolf) to engage audiences while raising awareness of lesser-discussed biodiversity.</li>
  </ul>
</section>
