---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "HOME"
header_img: https://placehold.co/600x400
# header_img: assets/images/folium_map.webp
header_title: "Data Collection"
header_type: hero
vega: true

---
<!-- Homepage – The Future of European Mammals -->
<section style="max-width: 880px; margin: 0 auto; padding: 2rem; font-family: 'Merriweather', serif; font-size: 1.05rem; line-height: 1.8; color: #222;">

 <h1 style="font-size: 3rem; font-weight: 700; text-align: center; margin-bottom: 1rem; color: #1a1a1a;">
  The Future of European Mammals
</h1>
<p style="font-size: 1.25rem; text-align: center; color: #555; margin-top: -0.5rem;">
  Climate change, land use and the future of terrestrial wildlife
</p>

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

### aggiornare con i dati più recenti

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

### aggiornare con i dati più recenti
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


# Il Futuro dei Mammiferi Europei
La crisi climatica non è più un concetto astratto, non tangibile da una società estremamente urbanizzata che non può vederne gli effetti sugli ecosistemi, ma un’esperienza vissuta da tutti noi. Le condizioni ambientali peggiorano: la temperatura media del pianeta aumenta, mentre fenomeni estremi come ondate di calore, inondazioni e siccità diventano sempre più vicini alla nuova normalità.
L'indicatore principale di questa trasformazione, l’innalzamento della temperatura media, segnala il 2024 nuovamente come l’anno più caldo mai registrato, superando per la prima volta soglia di +1,5 °C rispetto ai livelli preindustriali. E se il mondo corre, l’Europa vola: il nostro continente si sta riscaldando a una velocità quasi doppia, con un aumento che sulla terraferma ha raggiunto +2,6 °C già nel 2023.

<div style="width: 80%; margin: 1em 0;"> 
  <vegachart schema-url="{{site.baseurl}}/Land_cover/temperature_anomaly_chart.json" style="width: 100%;"></vegachart>
</div>

Di fronte a queste evidenze, l'interesse per il clima sta crescendo. Tuttavia, come osserva il giornalista e fotografo ambientale Jacopo Pasotti, questa attenzione è principalmente legata all'impatto economico che alla salvaguardia dell'ambiente in sé. La nostra preoccupazione, sembra, aumenta con la consapevolezza dei danni per la nostra specie. Ma noi non siamo gli unici abitanti del pianeta. Sorge quindi una domanda: Cosa significano questi cambiamenti per le altre specie? in particolare, quale sarà l’impatto sui mammiferi terrestri europei? Se le condizioni peggiorano per noi, per loro è lo stesso? 

La risposta dipende dai diversi futuri possibili, che dipendono non solo da come evolverà il clima, ma anche da come lo sviluppo della nostra società influirà sulla terra che condividiamo. Per esplorare questi futuri, gli scienziati utilizzano gli Scenari Socioeconomici Condivisi (SSP), i quali descrivono possibili sviluppi globali fino al 2100 tenendo conto di fattori come demografia, economia, politiche energetiche e uso del suolo.  
Le stime più recenti sono concordi: gli obiettivi più ottimistici, come contenere il riscaldamento globale entro 1,5 °C o 2 °C appaiono ormai irraggiungibili. L’attenzione si sposta su scenari più realistici. Tra i più studiati vi sono:

•	SSP2-4.5 (“La via di mezzo”): Uno scenario intermedio in cui le tendenze attuali proseguono. Le emissioni continuano a crescere moderatamente, portando a un riscaldamento globale di circa 2.7°C entro la fine del secolo.

•	SSP3-7.0 (“Rivalità Regionale”): Uno scenario più pessimistico, caratterizzato da nazionalismi, scarsa cooperazione internazionale e limitati investimenti nello sviluppo sostenibile. Questo percorso porterebbe a un aumento delle temperature globali di circa 3.6 °C entro il 2100.

Questi scenari non definiscono solo temperature diverse, ma anche paesaggi diversi. L’uso del suolo per l’agricoltura e per le città è una delle cause principali del degrado ambientale, frammentando gli habitat e minacciando la biodiversità.
Per capire l'impatto sui mammiferi, quindi, non basta guardare al clima, ma bisogna sapere come cambierà la loro casa: le foreste, i prati, le campagne. Per vedere con i nostri occhi questi futuri divergenti, nella mappa interattiva sottostante possiamo esplorare un dettagliatissimo set di mappe sviluppato per l'Europa, che visualizza come potrebbe apparire il nostro continente fino al 2100. Confrontiamo i due scenari. 

<div style="width: 90%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/interactive_chart.json" style="width: 100%;"></vegachart>
</div>

Analizzando le mappe, emergono due futuri per l'uso del suolo in Europa, radicalmente diversi non tanto nei numeri finali, quanto nelle forze che li determinano.
Lo scenario SSP2 descrive un'Europa che prosegue sul sentiero dell'efficienza, accelerando le tendenze già viste negli ultimi decenni. Si immagina questo futuro: l’urbanizzazione prosegue e, contemporaneamente, un'agricoltura sempre più tecnologica produce più cibo su meno terra. Il risultato sono vaste aree agricole, soprattutto quelle meno produttive, che diventano superflue e vengono abbandonate. Su questi terreni, la natura si riprende i suoi spazi: i campi si trasformano in prati, poi in arbusteti e infine in foreste. 
Lo scenario SSP3 dipinge un tutt’altro quadro. A prima vista potrebbe sembrare stabile, quasi un'immagine dell'Europa attuale. In realtà, le dinamiche sottostanti non sono guidate dall’efficienza, bensì dall’insicurezza. In un mondo frammentato, dove la cooperazione internazionale crolla e ogni nazione pensa solo alla propria sicurezza energetica e alimentare, la ricerca e l'innovazione in agricoltura rallentano. A questo si aggiunge un colpo ancora più duro: un clima ancora più ostile. L'aumento delle temperature e la siccità cronica abbattono le rese agricole. l'Europa è costretta a cercare di mantenere in produzione ogni ettaro possibile in una lotta disperata per compensare i raccolti persi a causa del clima. In questa lotta per le risorse, le foreste diventano la prima vittima. Per far spazio a nuovi campi coltivabili, si inizia a disboscare. Anche una lieve diminuzione netta delle foreste diventa il segnale che il trend di espansione si è invertito.
Ma come si traducono un cambiamento del clima, oppure un campo che diventa bosco, o una foresta che viene abbattuta, nella vita di un cervo, di un lupo o di un toporagno? Per rispondere, entra in gioco l’idoneità ambientale.
Non si tratta di dove una specie vive oggi, ma di mappare tutte le aree che, dati i suoi requisiti vitali (temperatura, vegetazione, ecc.), potrebbero sostenerne la presenza. L'obiettivo diventa quindi confrontare le mappe dell'idoneità attuale con quelle dei futuri possibili, per vedere dove una specie potrà ancora vivere (Se effettivamente presente), dove dovrà spostarsi e quali territori diventeranno inospitali.


<div style="width: 90%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/mappa_ricchezza_interattiva.json" style="width: 100%;"></vegachart>
</div>

La mappa dell'idoneità ambientale, aggregata per tutte le specie che potrebbero vivere in una determinata area, racconta una famosa regola dell’ecologia: la vita si manifesta con una maggiore diversità a latitudini più basse, per poi diradarsi gradualmente man mano che si sale verso il clima freddo del nord. Questo schema di base rimane anche nel futuro, ma il cambiamento climatico sta innescando un grande spostamento verso nord, che possiamo osservare anche in queste mappe di idoneità territoriale. Le aree settentrionali, riscaldandosi, diventano ospitali per specie che prima le trovavano inabitabili, offrendo un clima e una vegetazione sempre più simili a quelli del centro Europa.  Allo stesso tempo, le regioni meridionali si riscaldano, alcune specie resistono a questo cambiamento, altre non riusciranno a sopportare condizioni a cui non sono abituate e l’unica cosa che possono fare e spostarsi al nord, o in alcuni casi ad altitudin maggiori. 
Questa migrazione di massa, però, ha una condizione fondamentale: la connettività del territorio. Uno spostamento che sulla carta sembra possibile può essere bloccato da un'autostrada, una città o da campagne intensive prive di corridoi naturali. Se la diminuzione di specie a sud non si traduce in un'estinzione, ma in un semplice spostamento, è solo perché noi, con le nostre scelte, ne avremo dato la possibilità.

### aggiornare con i dati più recenti

<img
  src="{{ site.baseurl }}/assets/charts/species/confronto_scenari_ottimizzato.png"
  alt="Confronto scenari per specie"
  style="width:90%; margin:1em 0;"
/>

Se la prima mappa ci mostra la direzione del cambiamento, la seconda ne mostra la magnitudine, rivelando un quadro che sarebbe potuto risultare inaspettato: Per la grande maggioranza delle specie di mammiferi, il futuro sembra promettere un'espansione. Non a caso, sebbene il numero di specie in contrazione e in espansioni sia praticamente identico tra i due scenari, nel SSP3 dove aumenta maggiormente la temperatura, notiamo un più elevato numero di specie con un’espansione di oltre il 50%. Si delinea così una sorta di paradosso: mentre per la nostra specie, confinata all’interno di confini, ha condizioni di vita peggiori, per molti mammiferi si potrebbe aprire un'era di opportunità territoriale.
I numeri complessivi confermano questa tendenza: se consideriamo l'insieme dei mammiferi analizzati, il territorio idoneo in Europa mostra una crescita media di quasi il 18.62%. E non è un dato falsato da poche specie fortunate: il valore mediano di crescita per singola specie è anche più alto, con il 22.88%. 
Ma non tutti avranno un luogo in cui spostarsi perché, se la maggioranza avanza, c'è chi non ha un luogo dove fuggire. Sono i prigionieri del clima. Pensiamo agli specialisti delle alte montagne o delle tundre artiche. Man mano che il caldo sale, loro si ritirano, passo dopo passo, sempre più in alto, sempre più a nord. Ma la loro ritirata ha una fine. Un punto in cui, semplicemente, non c'è più nessun posto dove andare.
La montagna finisce. Il continente finisce.

### aggiornare con i dati più recenti
<img
  src="{{ site.baseurl }}/assets/charts/species/impact_by_specialization(SSP2).png"
  alt="Confronto scenari per specie"
  style="width:100%; margin:1em 0;"
/>

Guardando il grafico soprastante, relativo alla specializzazione dell'habitat, emerge una chiara spaccatura. A trarre i maggiori vantaggi sono le specie generaliste. Grazie alla loro incredibile adattabilità, non solo riescono a resistere meglio all'impatto nei territori più meridionali, ma sono anche le più rapide a colonizzare i nuovi, vasti territori che si aprono a nord. Il loro regno non si sposta semplicemente: si espande.
Al contrario, le specie specializzate per gli ambienti freddi, come quelle montane e delle tundre, affrontano un futuro di esclusivo deterioramento.

<img
  src="{{ site.baseurl }}/assets/charts/species/impact_by_specialization(SSP3).png"
  alt="Confronto scenari per specie"
  style="width:100%; margin:1em 0;"
/>

Nello scenario SSP3, la dinamica è simile ma amplificata: l'espansione dei generalisti diventa ancora più marcata, evidenziando come un riscaldamento più intenso favorisca ulteriormente le specie più versatili.


<div style="width: 80%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/boxplot_ordine_ssp2.json" style="width: 80%;"></vegachart>
</div>


Se spostiamo l'analisi dalla specializzazione ecologica alla classificazione tassonomica, i dati rivelano un altro livello di dettaglio. Notiamo una spiccata tendenza positiva per i Roditori, che sembrano essere i principali beneficiari del cambiamento climatico a venire. In maggiore difficoltà appaiono invece gli Artiodattili, un ordine che include molte delle specie specialiste degli ambienti montani e della tundra. Non sorprende, quindi, che esplorando i singoli punti del grafico, le specie che perdono più territorio siano proprio quelle confinate alle alte quote e alle latitudini settentrionali.


<div style="width: 80%;">
  <vegachart schema-url="{{site.baseurl}}/Land_cover/boxplot_ordine_ssp3.json" style="width: 80%;"></vegachart>
</div>

Nello scenario SSP3, considerato peggiore per gli esseri umani, le tendenze si accentuano ulteriormente: i Roditori mostrano un miglioramento ancora più netto, gli Artiodattili subiscono un peggioramento più severo, mentre la situazione per gli altri ordini rimane relativamente stabile rispetto allo scenario SSP2
