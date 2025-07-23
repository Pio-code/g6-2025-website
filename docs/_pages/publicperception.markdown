---
layout: default
title: "Public perception"
permalink: /publicperception.html
---
---
layout: default
title: "Public perception"
permalink: /publicperception.html
---

<section class="analysis-section">
  <h1>Textual Analysis and Sentiment Insights on European Mammals</h1>

  <p>This study is part of the broader project <em>“Impacts of Climate Change on European Mammals”</em>, which combines ecological modeling (SDMs with <strong>MaxEnt</strong>) and a <strong>social perception analysis</strong> from online conversations, specifically Reddit. The goal is to understand not only <strong>how often these species are mentioned</strong> but also the <strong>emotional tone</strong> of those discussions.</p>

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

  <h2>Mentions Analysis</h2>
  <p>The first analysis measures how frequently these species are discussed across posts and comments:</p>
  <img src="/assets/images/occ_specie_post_commenti.png" alt="Total posts and comments per species">

  <p>Distribution of mentions specifically in posts:</p>
  <img src="/assets/images/specie_piu_menzionate_post.png" alt="Most mentioned species in posts (percentage)">

  <p>Most discussed species based on comment interactions:</p>
  <img src="/assets/images/specie_piu_menzionate_commenti.png" alt="Most mentioned species in comments (percentage)">

  <h2>Emotional Tone by Species</h2>
  <p>To classify emotional content (anger, fear, joy, neutral), we applied a <strong>DistilRoBERTa Transformer model</strong> to each text within a 512-token window:</p>
  <img src="/assets/images/emozioni_per_specie.png" alt="Percentage distribution of anger, fear, joy, and neutral by species">

  <p>The analysis highlights that <strong>grey wolves</strong> trigger high anger (18%) and fear (12%), while <strong>polar bears</strong> are heavily associated with fear and sadness (linked to climate crisis mentions). Other species remain mostly neutral, with joy appearing rarely (primarily in wildlife photography and urban context discussions).</p>

  <h2>Implications</h2>
  <p>This integration of <strong>NLP, deep learning, and data visualization</strong> supports targeted awareness campaigns, aligns conservation policies with public sentiment, and aids in educational outreach using both iconic (polar bear, grey wolf) and lesser-discussed species.</p>
</section>
