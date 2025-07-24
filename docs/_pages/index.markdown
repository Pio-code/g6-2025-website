---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "The European Mammal Atlas"
header_img: assets/images/head.png
# header_img: assets/images/folium_map.webp
header_title: "The European Mammal Atlas"
header_type: hero
subtitle: "Climate Change, Land Use and the Future of Terrestrial Wildlife"
vega: true
---

<style>
.chulapa-subtitle {
  background-color: rgba(255, 255, 255, 0.9); /* bianco semitrasparente */
  color: #222;
  padding: 0.4rem 0.8rem;
  border-radius: 6px;
  display: inline-block;
  font-style: italic;
  max-width: 80%;
  text-align: center;
}
</style>

<!-- Homepage – The Future of European Mammals -->
<section style="max-width: 880px; margin: 0 auto; padding: 2rem; font-family: 'Merriweather', serif; font-size: 1.05rem; line-height: 1.8; color: #222;">

  <p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The climate crisis is no longer an <em>abstract concept</em>, intangible to an extremely urbanized society, unable to see its effects on ecosystems — <strong>it is now a lived experience for all of us</strong>.  
  Environmental conditions are rapidly deteriorating: the planet’s average temperature is rising, while <em>extreme events</em> like <strong>heatwaves</strong>, <strong>floods</strong> and <strong>droughts</strong> are becoming the new normal.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The clearest signal of this shift — rising average temperatures — marks 2024 once again as the <strong>hottest year ever recorded</strong>, surpassing for the first time the <strong>+1.5 °C threshold</strong> compared to pre-industrial levels.  
  And while the world is running, Europe is flying: our continent is warming at nearly twice the global average, with land temperatures reaching <strong>+2.6 °C</strong> as early as 2023.
</p>

  <!-- Vega chart -->
  <div style="width: 100%; margin: 2rem 0;">
    <vegachart schema-url="{{site.baseurl}}/Land_cover/temperature_anomaly_chart.json" style="width: 100%;"></vegachart>
  </div>

 <p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  Faced with this evidence, <strong>interest in the climate is growing</strong>. 
  Yet, as environmental journalist and photographer <strong>Jacopo Pasotti</strong> points out, this attention is still mostly driven by <em>economic concerns</em> rather than a deeper care for the environment itself. Our awareness seems to increase as the damage becomes personal.  
  But we are not the planet’s only inhabitants. 
  One question emerges:  
  <strong>What do these changes mean for other species?</strong>  
  In particular, <strong>what will be the impact onEurope’s terrestrial mammals</strong>?  
  If things are getting worse for us, <em>are they getting worse for them too</em>?
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The answer depends on the futures ahead.  
  These depend not only on how the climate evolves, but also on how society shapes the land we share.  
  To explore these paths, scientists use the <strong>Shared Socioeconomic Pathways (SSPs)</strong> — global scenarios describing different developments up to 2100, taking into account <em>demographics, economy, energy policies</em>, and <em>land use</em>.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  Recent projections agree: the most optimistic goals — limiting warming to <strong>1.5 °C</strong> or even <strong>2 °C</strong> — are now out of reach.  
  The focus has shifted to more realistic pathways.  
  Among the most studied:
</p>

<ul style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif; margin-bottom: 1.5rem;">
  <li>
    <strong>SSP2-4.5 (“Middle of the Road”):</strong> A moderate scenario where current trends continue.  
    Emissions grow at a moderate pace, leading to <strong>~2.7 °C</strong> warming by 2100.
  </li>
  <li>
    <strong>SSP3-7.0 (“Regional Rivalry”):</strong> A pessimistic scenario marked by <em>nationalism</em>, <em>poor international cooperation</em>, and <em>limited investment</em> in sustainability.  
    This path leads to approximately <strong>3.6 °C</strong> of global warming by century’s end.
  </li>
</ul>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  These scenarios do not just predict <em>different temperatures</em> — they predict different landscapes.  
  Agriculture and urban expansion are key drivers of environmental degradation, <em>fragmenting habitats</em> and <em>threatening biodiversity</em>.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  To understand the impact on mammals, we must look beyond temperature data.  
  We need to understand how their homes — <em>forests, grasslands, farmlands</em> — will change.  
  In the interactive map below, you can explore a detailed dataset developed for Europe, visualizing how our continent may look by 2100.  
  <strong>Let’s compare the two scenarios.</strong>
</p>

<div style="width: 90%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/interactive_chart.json" style="width: 100%;"></vegachart>
</div>


<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  When analyzing the maps, two radically different futures emerge for land use in Europe—less in their final numbers, and more in the forces that shape them.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The SSP2 scenario envisions a Europe that continues along a path of <strong>efficiency</strong>, accelerating trends already seen in recent decades.  
  In this future, urbanization proceeds steadily, while increasingly <em>technological agriculture</em> produces more food on less land.  
  As a result, vast areas of marginal farmland become redundant and are eventually abandoned.  
  On this land, nature begins to reclaim space: fields turn into grasslands, then into shrublands, and finally into forests.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The SSP3 scenario paints a very different picture. At first glance, it may appear stable—almost like today’s Europe.  
  But underneath, the dynamics are not driven by efficiency, but by <strong>insecurity</strong>.  
  In a fragmented world where international cooperation collapses and each country focuses solely on its own energy and food security, innovation in agriculture slows down.  
  And that’s not all: a harsher climate delivers another blow. Rising temperatures and chronic droughts <em>reduce crop yields</em>.  
  Europe is forced to keep <strong>every hectare in production</strong> in a desperate effort to compensate for harvest losses.  
  In this scramble for resources, forests become the first victims.  
  To make room for new farmland, deforestation begins.  
  Even a slight net decline in forest cover becomes a sign that the expansion trend has reversed.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  But what do climate change, or a field turning into forest—or a forest being cut down—actually mean in the life of a <em>deer</em>, a <em>wolf</em>, or a <em>shrew</em>?  
  To answer this, we turn to the concept of habitat suitability.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  This is not just about where a species currently lives, but about mapping all the areas that—given its biological requirements (such as temperature, vegetation, and elevation)—could support its presence.  
  The goal becomes to compare today’s habitat suitability maps with those of potential futures, in order to understand <em>where a species could still survive</em> (whether it’s currently present or not), <em>where it may need to move</em>, and <em>which areas will become uninhabitable</em>.
</p>
</section>

<div style="width: 90%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/mappa_ricchezza_interattiva.json" style="width: 100%;"></vegachart>
</div>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The habitat suitability map—aggregated for all species that could potentially live in a given area—reflects a well-known rule in ecology:  
  <strong>biodiversity increases at lower latitudes</strong> and gradually thins out toward the colder climates of the north.  
  This foundational pattern remains true even in future projections. However, climate change is triggering a dramatic northward shift, clearly visible in these territorial suitability maps.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  As northern regions warm, they become more hospitable to species that once found them uninhabitable—offering climates and vegetation increasingly similar to those of Central Europe.  
  At the same time, southern areas heat up. Some species may adapt, but others won’t tolerate the unfamiliar conditions.  
  For them, <em>the only option is to move north</em>—or in some cases, to higher elevations.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  This mass migration, however, comes with a critical condition: <strong>landscape connectivity</strong>.  
  A movement that looks feasible on a map can be blocked in reality—by a highway, a city, or vast farmlands without natural corridors.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  If the decline of species in the south does not result in extinction but in relocation, <em>it will only be because we made that shift possible</em>—through the way we manage land and design our landscapes.
</p>


<img
  src="{{ site.baseurl }}/assets/charts/species/confronto_scenari_ottimizzato.png"
  alt="Confronto scenari per specie"
  style="width:90%; margin:1em 0;"
/>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  If the first map shows us the <strong>direction</strong> of change, the second reveals its <strong>magnitude</strong>—and the result might seem unexpected:  
  for the vast majority of mammal species, the future appears to hold <em>opportunities for expansion</em>.  
  Interestingly, even though the number of species projected to expand or contract is nearly the same in both scenarios,  
  in SSP3—where temperatures rise more dramatically—we observe a <strong>higher number of species</strong> experiencing over <strong>50% expansion</strong> in suitable habitat.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  A kind of ecological paradox begins to emerge:  
  while our own species—limited by borders and infrastructure—faces worsening conditions,  
  <em>many other mammals might enter a new era of territorial opportunity</em>.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The overall numbers support this trend:  
  when considering all analyzed mammal species, the average growth in suitable territory across Europe reaches nearly <strong>+18.62%</strong>.  
  And this is not just driven by a few lucky species: the <strong>median growth per species</strong> is even higher, at <strong>+22.88%</strong>.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  But not everyone will have somewhere to go. <strong>Some species are climate prisoners</strong>: those adapted to alpine peaks or arctic tundra.  
  As temperatures rise, they retreat—step by step—higher and further north. But their retreat has a limit. There comes a point where <em>there is simply nowhere left to go</em>.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  The mountain ends.  
  The continent ends.
</p>


<img
  src="{{ site.baseurl }}/assets/charts/species/impact_by_specialization(SSP2).png"
  alt="Confronto scenari per specie"
  style="width:100%; margin:1em 0;"
/>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  Looking at the graph above, which illustrates <strong>habitat specialization</strong>, a clear divide emerges.  
  The biggest winners are the <strong>generalist species</strong>. Thanks to their remarkable adaptability,  
  they not only better withstand the pressures in southern regions but are also the quickest to colonize the new and vast territories opening up in the north. Their reign doesn’t just shift — <em>it expands</em>.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  In contrast, <strong>specialist species</strong> adapted to cold environments — such as mountain or tundra mammals — face a future of pure decline. Their narrow ecological niche leaves little room to adapt or relocate as the climate warms and their habitats shrink.
</p>

<img
  src="{{ site.baseurl }}/assets/charts/species/impact_by_specialization(SSP3).png"
  alt="Confronto scenari per specie"
  style="width:100%; margin:1em 0;"
/>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  In the <strong>SSP3 scenario</strong>, the dynamic is similar but amplified: the expansion of generalist species becomes even more pronounced, highlighting how a more intense level of warming further favors the most <em>versatile and adaptable</em> species.
</p>

<div style="width: 80%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/boxplot_ordine_ssp2.json" style="width: 80%;"></vegachart>
</div>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  Shifting the analysis from ecological specialization to <strong>taxonomic classification</strong> reveals another level of insight. A strong positive trend emerges for <strong>rodents</strong>, which appear to be the main beneficiaries of the changing climate.  
  On the other hand, <strong>artiodactyls</strong> — an order that includes many species specialized in mountain and tundra environments — seem to face greater challenges.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  Unsurprisingly, when exploring individual points in the chart, the species losing the most habitat are often those confined to <em>high elevations</em> and <em>northern latitudes</em>.
</p>

<div style="width: 80%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/boxplot_ordine_ssp3.json" style="width: 80%;"></vegachart>
</div>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
  In the <strong>SSP3 scenario</strong>—considered the most critical for humans—these trends become even more pronounced: <strong>Rodents</strong> show an even clearer improvement, while <strong>artiodactyls</strong> face more severe decline.  
  Meanwhile, conditions for other taxonomic orders remain relatively stable compared to the SSP2 projection.
</p>

<p style="font-size: 1.05rem; line-height: 1.8; color: #222; font-family: 'Merriweather', serif;">
For those interested in going deeper into the <strong>individual species</strong>, we invite you to go to the <strong>species explorer</strong>, where you will find the suitability maps of all those analyzed, divided by scenario and year.
</p>
