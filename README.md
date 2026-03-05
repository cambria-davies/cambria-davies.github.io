# cambria-davies.github.io

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>⛵ South Ionian Sailing Week — May 2–9, 2026</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
:root {
  --navy: #1B3A5C;
  --accent: #2E75B6;
  --gold: #D4A853;
  --muted: #6B7280;
  --light-blue: #D5E8F0;
  --sand: #F5F0E8;
  --teal: #0F766E;
}
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
body { font-family: 'DM Sans', system-ui, sans-serif; background: #FAFAFA; color: #333; -webkit-font-smoothing: antialiased; }
a { text-decoration: none; }
.hero { background: linear-gradient(160deg, rgba(27,58,92,0.94), rgba(46,117,182,0.88)); padding: 3.5rem 2rem; text-align: center; color: white; }
.hero h1 { font-size: 2.2rem; font-weight: 700; margin-bottom: 0.5rem; }
.hero p { font-size: 1.1rem; opacity: 0.9; }
.hero-badge { display: inline-block; background: rgba(212,168,83,0.9); padding: 0.4rem 1.2rem; border-radius: 20px; font-weight: 600; font-size: 0.85rem; margin-top: 0.75rem; }
.container { max-width: 800px; margin: 0 auto; padding: 2rem 1.5rem; }
h2 { font-size: 1.5rem; font-weight: 700; color: var(--navy); margin-bottom: 1rem; }
h2.mt { margin-top: 2.5rem; }
.info-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1px; background: #E5E7EB; border-radius: 12px; overflow: hidden; margin-bottom: 2.5rem; }
.info-label { background: var(--light-blue); padding: 0.6rem 1rem; font-weight: 600; color: var(--navy); font-size: 0.9rem; }
.info-value { background: white; padding: 0.6rem 1rem; font-size: 0.9rem; }
.map-card { background: white; border-radius: 16px; overflow: hidden; box-shadow: 0 4px 20px rgba(0,0,0,0.06); margin-bottom: 1rem; }
.map-card svg { width: 100%; display: block; }
.map-legend { display: flex; flex-wrap: wrap; gap: 1rem; padding: 0.75rem 1.5rem; font-size: 0.8rem; color: var(--muted); border-top: 1px solid #F0F0F0; align-items: center; }
.legend-dot { width: 10px; height: 10px; border-radius: 50%; display: inline-block; margin-right: 0.35rem; vertical-align: middle; }
.overview { background: white; border-radius: 12px; padding: 1rem 1.5rem; box-shadow: 0 2px 10px rgba(0,0,0,0.04); margin-bottom: 2.5rem; }
.overview-row { padding: 0.5rem 0; font-size: 0.9rem; }
.overview-row:not(:last-child) { border-bottom: 1px solid #F0F0F0; }
.overview-row strong { color: var(--navy); }
.overview-row .muted { color: var(--muted); }
.day-card { background: white; border-radius: 16px; overflow: hidden; box-shadow: 0 4px 20px rgba(0,0,0,0.06); margin-bottom: 1.5rem; }
.day-header { padding: 1.5rem 2rem; color: white; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; }
.day-header:hover { filter: brightness(1.05); }
.day-label { font-size: 0.75rem; font-weight: 600; text-transform: uppercase; letter-spacing: 1.5px; opacity: 0.85; margin-bottom: 4px; }
.day-title { font-size: 1.35rem; font-weight: 700; }
.day-meta { font-size: 0.85rem; opacity: 0.9; margin-top: 4px; }
.day-chevron { font-size: 1.5rem; transition: transform 0.2s; flex-shrink: 0; margin-left: 1rem; }
.day-chevron.open { transform: rotate(180deg); }
.day-body { padding: 1.5rem 2rem; display: none; }
.day-body.open { display: block; }
.map-links { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 1rem; }
.map-pill { display: inline-flex; align-items: center; gap: 0.35rem; padding: 0.4rem 0.75rem; background: white; border-radius: 20px; font-size: 0.82rem; font-weight: 600; transition: all 0.15s; cursor: pointer; }
.map-pill.gmaps { border: 1.5px solid var(--accent); color: var(--accent); }
.map-pill.gmaps:hover { background: var(--accent); color: white; }
.map-pill.navily { border: 1.5px solid var(--teal); color: var(--teal); }
.map-pill.navily:hover { background: var(--teal); color: white; }
.section-label { color: var(--accent); font-size: 0.8rem; text-transform: uppercase; letter-spacing: 0.5px; margin-bottom: 0.5rem; font-weight: 600; }
.section-label.mt { margin-top: 1rem; }
.route-box { display: grid; grid-template-columns: 1fr 1fr; gap: 0.5rem; margin-bottom: 1rem; background: var(--light-blue); border-radius: 10px; padding: 0.75rem 1rem; font-size: 0.9rem; }
.route-box strong { color: var(--navy); }
.route-list { padding-left: 1.25rem; margin-bottom: 1rem; color: var(--muted); font-size: 0.9rem; }
.route-list li { margin-bottom: 0.25rem; }
.festival-box { background: linear-gradient(135deg, var(--navy), var(--accent)); color: white; border-radius: 12px; padding: 1.25rem 1.5rem; margin-bottom: 1rem; text-align: center; }
.festival-title { color: var(--gold); font-weight: 700; font-size: 1.15rem; margin-bottom: 0.5rem; }
.festival-items { text-align: left; margin-top: 0.75rem; }
.festival-items div { padding: 0.2rem 0; opacity: 0.95; }
.about-text { margin-bottom: 1rem; line-height: 1.7; font-size: 0.93rem; white-space: pre-line; }
.stay-text { margin-bottom: 1rem; font-size: 0.93rem; color: #4A4A4A; }
.restaurant-row { display: flex; gap: 0.6rem; padding: 0.4rem 0; align-items: flex-start; }
.restaurant-row .star { font-size: 1rem; flex-shrink: 0; }
.restaurant-name { font-weight: 600; color: var(--navy); font-size: 0.93rem; }
.restaurant-desc { font-size: 0.85rem; color: var(--muted); }
.activities-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 0.5rem; }
.activity-card { background: var(--light-blue); border-radius: 10px; padding: 0.65rem 0.75rem; display: flex; gap: 0.5rem; align-items: flex-start; }
.activity-icon { font-size: 1.15rem; flex-shrink: 0; line-height: 1; }
.activity-name { font-weight: 600; color: var(--navy); font-size: 0.85rem; margin-bottom: 2px; }
.activity-desc { font-size: 0.78rem; color: var(--muted); line-height: 1.35; }
.captain-box { background: var(--sand); border-left: 4px solid var(--gold); padding: 0.85rem 1rem; margin-top: 1rem; border-radius: 0 8px 8px 0; font-style: italic; font-size: 0.9rem; color: #4A4A4A; }
.captain-label { font-style: normal; font-weight: 600; }
/* Photo strip styles */
.photo-strip { display: grid; grid-template-columns: 1fr 1fr; gap: 0.5rem; margin-bottom: 1rem; }
.photo-strip a { display: block; border-radius: 10px; overflow: hidden; aspect-ratio: 16/9; position: relative; background: #e0e7ee; }
.photo-strip img { width: 100%; height: 100%; object-fit: cover; display: block; transition: transform 0.3s; }
.photo-strip a:hover img { transform: scale(1.05); }
.photo-strip .photo-label { position: absolute; bottom: 0; left: 0; right: 0; padding: 0.4rem 0.6rem; background: linear-gradient(transparent, rgba(0,0,0,0.6)); color: white; font-size: 0.75rem; font-weight: 600; }
.footer { text-align: center; color: var(--muted); font-size: 0.85rem; padding: 1.5rem 0; }
@media (max-width: 600px) {
  .hero h1 { font-size: 1.6rem; }
  .info-grid, .route-box { grid-template-columns: 1fr; }
  .activities-grid { grid-template-columns: 1fr; }
  .day-header { padding: 1.25rem 1.25rem; }
  .day-body { padding: 1.25rem; }
  .container { padding: 1.25rem 1rem; }
}
</style>
</head>
<body>
<div class="hero">
  <h1>⛵ South Ionian Sailing Week</h1>
  <p>Saturday May 2 — Saturday May 9, 2026</p>
  <div class="hero-badge">🏛️ Ithaca · Kefalonia · Meganisi · Kastos · Kalamos</div>
</div>
<div class="container" id="app"></div>
<script>
const infoRows = [
  ["Pick Up","Saturday, May 2, 2026 (afternoon)"],["Drop Off","Saturday, May 9, 2026 (morning)"],
  ["Marina","Lefkas Marina, Lefkada, Greece"],["Boat","Lagoon 40 | Mary Grace (Catamaran)"],
  ["Cabins","6 cabins, 10+2 berths, built 2021"],["Charter Co.","Exploreseas"],
  ["Rental","€1,530 / week"],["Transit Log","€320 (cleaning + linen) · mandatory"],
  ["Security Deposit","€3,500 (refundable)"],["Includes","Free SUP, WiFi, dinghy engine"],
  ["Airport","Aktion/Preveza (PVK) · ~20 min to marina"],["Pets","Not permitted"]
];
const costData = {
  fixed: { rental: 1530, transit: 320, fuel: 175, marinas: 100 },
  perPersonPerDay: 50,
  provisionDays: 7,
  crewOptions: [4, 6, 8]
};
const days = [
  { num:1, day:"Saturday", date:"May 2", title:"Lefkada → Meganisi (Vathi)", nm:"~11 NM", time:"~1.5 hours", note:"Easy first sail to settle in", gradient:"linear-gradient(135deg, #667eea 0%, #764ba2 100%)", emoji:"🏁",
    maps:[{label:"Lefkas Marina",url:"https://maps.google.com/?q=38.8347,20.7069",t:"g"},{label:"Vathi, Meganisi",url:"https://maps.google.com/?q=38.6653,20.7819",t:"g"},{label:"Meganisi (Navily)",url:"https://www.navily.com/mouillage/meganisi/55027",t:"n"},{label:"Vathi Marina (Navily)",url:"https://www.navily.com/port/vathi-marina/11616",t:"n"}],
    route:["Depart mid-afternoon after boarding and provisioning","Pass through the Lefkada canal and head south past Nidri"],
    about:"Meganisi is a lush green jewel just southeast of Lefkada — the perfect first-night stop with short distances and calm, protected waters. Vathi (Little Vathi) is a sleepy fishing village with a tiny harbor surrounded by whitewashed houses, colorful tavernas, and pine-covered hills. The bay is well-sheltered and the atmosphere is quintessentially Greek.",
    stay:"Moor stern-to on the south quay in the old harbor (arrive early for a spot), or book ahead at Odyseas Marina for lazy lines and shore power (~€50–80/night).",
    restaurants:[{name:"Errikos",desc:"Upscale seafood on the fishing mole · Classy twist on Greek classics",url:"https://www.google.com/maps/search/Errikos+restaurant+Vathi+Meganisi"},{name:"Stavros Taverna",desc:"Traditional Greek food with excellent service · Local favorite",url:"https://www.google.com/maps/search/Stavros+Taverna+Vathi+Meganisi"},{name:"The Rose Garden",desc:"Quality Greek cuisine · Beautiful garden setting",url:"https://www.google.com/maps/search/Rose+Garden+restaurant+Vathi+Meganisi"},{name:"Tilevoes Italian",desc:"Good pasta and steak · Nice change from Greek food",url:"https://www.google.com/maps/search/Tilevoes+Italian+Vathi+Meganisi"}],
    captain:"Easy first sail to get settled. Meganisi is forgiving, protected, and a textbook first night. Provision in Lefkada Town before departure — the Palmos supermarket in Vathi is small.",
    diningMode:"out", diningNote:"First night — celebrate with the crew at Errikos on the waterfront",
    activities:[{icon:"🤿",name:"Snorkel by the Church",desc:"Walk east past the little church to find steps into the water with excellent snorkeling off the rocks"},{icon:"🚶",name:"Walk to Katomeri",desc:"30-minute uphill walk to this sleepy inland village with panoramic views of the Ionian",url:"https://www.google.com/maps/search/Katomeri+Meganisi"},{icon:"🚲",name:"E-Bike Meganisi",desc:"Rent e-bikes in Vathi and explore to Spartachori, Abelike Bay, and Port Atheni"},{icon:"🏊",name:"Swim Abelike Bay",desc:"15-minute walk NE to one of the most beautiful spots on the island — two tavernas and a shingle beach",url:"https://www.google.com/maps/search/Abelike+Bay+Meganisi"}],
    images:[
      {url:"https://www.sailionian.com/wp-content/uploads/2020/11/AdobeStock_125982782.jpeg",label:"Vathi Harbor, Meganisi"},
      {url:"https://www.greeka.com/village_beach/photos/668/vathy-top-2-1280.jpg",label:"Vathi from above"}
    ]
  },
  { num:2, day:"Sunday", date:"May 3", title:"Meganisi → Kastos", nm:"~15 NM", time:"~2.5 hours", note:"Swim stops en route", gradient:"linear-gradient(135deg, #43e97b 0%, #38f9d7 100%)", emoji:"🏝️",
    maps:[{label:"Kastos Harbor",url:"https://maps.google.com/?q=38.5700,20.9200",t:"g"},{label:"Sarakiniko Beach, Kastos",url:"https://maps.google.com/?q=38.5580,20.9100",t:"g"}],
    route:["Sail south past the east coast of Kalamos","Optional swim stop at Kalamos Woods Bay en route"],
    about:"Kastos is a tiny, unspoiled island that feels like a hidden corner of the Ionian. With just a handful of year-round residents, a single village, and no cars to speak of, this is where you truly switch off. The small harbor is peaceful, the water impossibly clear, and the evening ashore is about as authentic as Greece gets.",
    stay:"Moor stern-to on the village quay (free, limited space) or anchor in the bay. The quay has basic water but no electric.",
    restaurants:[{name:"Kastos Taverna",desc:"The main taverna on the waterfront · Fresh fish, slow pace",url:"https://www.google.com/maps/search/taverna+Kastos+island+Greece"},{name:"Harbour Cafe",desc:"Morning coffee and simple meals · Perfect for watching fishing boats",url:"https://www.google.com/maps/search/cafe+Kastos+harbour+Greece"}],
    captain:"This is a 'switch off your brain' day. Kastos is deliberately quiet — embrace it. The anchorage is calm and the holding is good.",
    diningMode:"boat", diningNote:"Cook aboard tonight — grab drinks at the harbour cafe, then sunset dinner on deck under the stars. Kastos' taverna is basic; save your dining-out budget for Kioni tomorrow.",
    activities:[{icon:"🏖️",name:"Sarakiniko Beach",desc:"Walk south from the village to this gorgeous bay with turquoise water and white pebbles — one of the Ionian's hidden gems"},{icon:"🤿",name:"Snorkel the East Coast",desc:"Crystal visibility around the rocky shoreline; bring gear from the boat"},{icon:"🌅",name:"Sunset from the Hill",desc:"Walk up the path behind the village for a panoramic sunset view over the Ionian"},{icon:"📚",name:"Read on Deck",desc:"This is the quietest night of the trip — stars, silence, and the sound of water lapping the hull"}],
    images:[
      {url:"https://www.travel.gr/wp-content/uploads/2022/06/shutterstock_1679055322-scaled.jpg",label:"Kastos village harbor"},
      {url:"https://sailingbritican.com/wp-content/uploads/2015/07/Port-Kastos-Greek-Ionian-14-1.jpg",label:"Port Kastos"}
    ]
  },
  { num:3, day:"Monday", date:"May 4", title:"Kastos → Ithaca (Kioni)", nm:"~20 NM", time:"~3.5 hours", note:"The legendary island of Odysseus", gradient:"linear-gradient(135deg, #f5af19 0%, #f12711 100%)", emoji:"🏛️",
    maps:[{label:"Kioni Harbor, Ithaca",url:"https://maps.google.com/?q=38.4637,20.6930",t:"g"},{label:"Filiatro Beach (swim stop)",url:"https://maps.google.com/?q=38.4350,20.7200",t:"g"}],
    route:["Sail west across the channel to Ithaca's east coast","Optional swim stop at Filiatro Bay en route to Kioni"],
    about:"Ithaca — the legendary home of Odysseus. Kioni is one of the most charming harbors in all of Greece: a tiny horseshoe bay overlooked by three ruined windmills on the hillside, with neoclassical houses in pastel colors tumbling down to the waterfront. This is the cultural highlight of the trip.\n\nThe bay is intimate and sheltered, surrounded by dense cypress and olive groves. In the evening, the waterfront tavernas fill up and the village has a magical, timeless atmosphere.",
    stay:"Moor stern-to on the village quay with an anchor. Space is limited and it gets busy — arrive early afternoon. If full, anchor in the bay and dinghy ashore.",
    restaurants:[{name:"Calypso",desc:"Waterfront terrace · Excellent seafood and pasta · Romantic",url:"https://www.google.com/maps/search/Calypso+restaurant+Kioni+Ithaca"},{name:"Kanenas",desc:"Traditional Greek · Great meze plates · Harbor views",url:"https://www.google.com/maps/search/Kanenas+restaurant+Kioni+Ithaca"},{name:"Myrto",desc:"Family-run · Wood-fired oven · Local favorite",url:"https://www.google.com/maps/search/Myrto+restaurant+Kioni+Ithaca"}],
    captain:"Kioni is the harbor you'll talk about for years. Arrive by 2pm for quay space. The three windmills above the bay are iconic — walk up at sunset.",
    diningMode:"out", diningNote:"Don't miss this one — Kioni's waterfront tavernas are the quintessential Ionian evening",
    activities:[{icon:"🏛️",name:"Walk to the Windmills",desc:"Hike up the hillside path to the three ruined windmills above the bay — the most photographed view on Ithaca"},{icon:"🤿",name:"Snorkel Kioni Bay",desc:"Excellent visibility in the horseshoe bay; rocky edges teem with marine life"},{icon:"🚶",name:"Coastal Path South",desc:"Walk the scenic coastal trail toward Frikes — stunning views of the channel between Ithaca and Kefalonia"},{icon:"📖",name:"The Odyssey Connection",desc:"This is Odysseus' island — browse the local shops for Homeric souvenirs and mythology books"}],
    images:[
      {url:"https://www.sailionian.com/wp-content/uploads/2020/12/AdobeStock_375401237.jpeg",label:"Kioni Harbor, Ithaca"},
      {url:"https://s3-eu-west-1.amazonaws.com/zalinga/800x600/05297cee-b493-4e9b-905e-ad45ff175678.jpg",label:"Kioni village & harbor"}
    ]
  },
  { num:4, day:"Tuesday", date:"May 5", title:"Kioni → Ithaca (Vathy) → Kefalonia Coast", nm:"~18 NM", time:"~3 hours", note:"Capital of Ithaca + sailing the strait", gradient:"linear-gradient(135deg, #a18cd1 0%, #fbc2eb 100%)", emoji:"🌊",
    maps:[{label:"Vathy, Ithaca",url:"https://maps.google.com/?q=38.3650,20.7180",t:"g"},{label:"Antisamos Beach, Kefalonia",url:"https://maps.google.com/?q=38.3480,20.5920",t:"g"},{label:"Vathy Port (Navily)",url:"https://www.navily.com/port/vathy-port/7937",t:"n"}],
    route:["Sail south along Ithaca's beautiful east coast to Vathy","Cross the strait to Kefalonia for an afternoon swim at Antisamos"],
    about:"Vathy is the capital of Ithaca, set at the head of one of the largest natural harbors in the Mediterranean — a deep, fjord-like inlet surrounded by green mountains. The town has a lovely waterfront, small archaeological museum, and the laid-back charm of a real working Greek town rather than a tourist resort.\n\nIn the afternoon, sail across the spectacular strait between Ithaca and Kefalonia to Antisamos Beach — a stunning crescent of white pebbles backed by towering green hills (the Captain Corelli's Mandolin beach).",
    stay:"Anchor overnight at Antisamos for a wild anchorage under the stars, or continue to Agia Efimia harbor (4 NM further) for a quay berth and taverna dinner.",
    restaurants:[{name:"Nikos Taverna (Vathy)",desc:"Classic Greek · Harbor terrace · Great value",url:"https://www.google.com/maps/search/Nikos+Taverna+Vathy+Ithaca"},{name:"Sirens (Vathy)",desc:"Seafood-focused · Named for the mythological Sirens · Waterfront",url:"https://www.google.com/maps/search/Sirens+restaurant+Vathy+Ithaca"},{name:"Pergola (Agia Efimia)",desc:"Excellent taverna if you continue to Kefalonia · Fresh fish and garden setting",url:"https://www.google.com/maps/search/Pergola+restaurant+Agia+Efimia+Kefalonia"}],
    captain:"The Ithaca-Kefalonia strait offers the best sailing of the week — expect good wind in the channel. Antisamos at sunset is extraordinary.",
    diningMode:"boat", diningNote:"Anchor at Antisamos and BBQ on deck with the mountains lit up at sunset. If you continue to Agia Efimia, Pergola taverna is worth the stop.",
    activities:[{icon:"🏛️",name:"Ithaca Archaeological Museum",desc:"Small but fascinating collection with artifacts from Odysseus-era excavations in Vathy"},{icon:"🏊",name:"Swim Antisamos Beach",desc:"Captain Corelli's Mandolin filming location — white pebbles, turquoise water, dramatic mountain backdrop"},{icon:"⛵",name:"Channel Sailing",desc:"The strait between Ithaca and Kefalonia offers the best sailing conditions of the trip — good wind, manageable waves"},{icon:"🌊",name:"Snorkel Pera Pigadia",desc:"Stop at this bay on Ithaca's south coast en route — exceptional underwater rock formations"}],
    images:[
      {url:"https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/20140411_ithaki094.JPG/1280px-20140411_ithaki094.JPG",label:"Vathy, Ithaca capital"},
      {url:"https://www.nothingfamiliar.com/wp-content/uploads/2024/05/Antisamos-Beach-Kefalonia.jpg",label:"Antisamos Beach, Kefalonia"}
    ]
  },
  { num:5, day:"Wednesday", date:"May 6", title:"Kefalonia Coast → Fiskardo", nm:"~15 NM", time:"~2.5 hours", note:"The jewel of the Ionian", gradient:"linear-gradient(135deg, #fa709a 0%, #fee140 100%)", emoji:"💎",
    maps:[{label:"Fiskardo Harbor, Kefalonia",url:"https://maps.google.com/?q=38.4570,20.5780",t:"g"},{label:"Fiskardo (Navily)",url:"https://www.navily.com/mouillage/ormos-fiskardo/17351",t:"n"}],
    route:["Sail north along Kefalonia's east coast, passing seven beautiful swim-stop bays","Arrive at Fiskardo on Kefalonia's northern tip"],
    about:"Fiskardo is the crown jewel of the Ionian — a crescent-shaped harbor of brightly painted Venetian houses, elegant restaurants, and luxury yachts. It's the only village on Kefalonia that survived the devastating 1953 earthquake, so its 18th-century architecture is beautifully preserved.\n\nThe harbor is buzzy and cosmopolitan but never loses its charm. Expect the best food, the liveliest evening, and the most photogenic harbor of the entire trip.",
    stay:"Moor in the bay just south of Fiskardo and dinghy in, or try for a stern-to spot on the town quay (arrive early — very competitive in season).",
    restaurants:[{name:"Nefeli",desc:"Elegant dining under blooming trees · Known for late-night dancing on tables under the stars",url:"https://www.google.com/maps/search/Nefeli+restaurant+Fiskardo+Kefalonia"},{name:"Tassia",desc:"Legendary Fiskardo institution · Run by cookbook author Tassia Dendrinou · Exceptional seafood",url:"https://www.google.com/maps/search/Tassia+restaurant+Fiskardo+Kefalonia"},{name:"Vasso's",desc:"Waterfront terrace · Famous for lobster pasta · Busy but worth the wait",url:"https://www.google.com/maps/search/Vassos+restaurant+Fiskardo+Kefalonia"},{name:"Platanos",desc:"Under the plane tree · Traditional meze · Great for a relaxed lunch",url:"https://www.google.com/maps/search/Platanos+taverna+Fiskardo+Kefalonia"}],
    captain:"Fiskardo is the 'big night out' of the trip. It's the Monte Carlo of the Ionian — dress up a little. The anchorage in the bay south of town is beautiful and free.",
    diningMode:"out", diningNote:"The best dining of the week — this is the night to dress up and splurge. Book Tassia or Nefeli if you can.",
    activities:[{icon:"🏘️",name:"Explore the Venetian Village",desc:"Wander the pastel-colored streets, browse boutiques, visit the Roman-era ruins and Venetian lighthouse"},{icon:"🤿",name:"Snorkel Emblisi Beach",desc:"Walk or dinghy north to this hidden pebble beach with outstanding snorkeling in crystal-clear water",url:"https://www.google.com/maps/search/Emblisi+Beach+Fiskardo+Kefalonia"},{icon:"🍷",name:"Wine & Dine",desc:"Kefalonia is famous for its Robola wine — taste the local vintage at any restaurant"},{icon:"🌅",name:"Sunset at the Lighthouse",desc:"Walk to the Venetian lighthouse on the point for a spectacular sunset over Ithaca across the channel",url:"https://www.google.com/maps/search/Venetian+lighthouse+Fiskardo+Kefalonia"}],
    images:[
      {url:"https://upload.wikimedia.org/wikipedia/commons/0/01/Fiskardo1.jpg",label:"Fiskardo Harbor"},
      {url:"https://dynamic-media-cdn.tripadvisor.com/media/photo-o/0f/14/45/94/fiskardo-harbor-cephalonia.jpg",label:"Fiskardo Venetian waterfront"}
    ]
  },
  { num:6, day:"Thursday", date:"May 7", title:"Fiskardo → Kalamos", nm:"~22 NM", time:"~4 hours", note:"Wild island, off the beaten path", gradient:"linear-gradient(135deg, #0c3483 0%, #a2b6df 100%)", emoji:"🌿",
    maps:[{label:"Kalamos Port",url:"https://maps.google.com/?q=38.6250,20.9300",t:"g"},{label:"Episkopi Bay, Kalamos",url:"https://maps.google.com/?q=38.6480,20.9280",t:"g"},{label:"Atokos Island (swim stop)",url:"https://maps.google.com/?q=38.5100,20.7800",t:"g"}],
    route:["Depart Fiskardo north, passing the isle of Arkoudi","Optional swim stop at uninhabited Atokos Island en route","Round into Kalamos from the west"],
    about:"Kalamos is a wild, mountainous island with just one village and no tourism infrastructure to speak of. It's the adventure day — dramatically different from polished Fiskardo. The port sits beneath towering cliffs covered in dense pine forest, and the island has a raw, untouched beauty.\n\nEn route, stop at Atokos — a completely uninhabited island with pristine anchorages and some of the clearest water in Greece.",
    stay:"Moor stern-to on the Kalamos village quay (free) or anchor in Episkopi Bay on the north coast for a wilder experience with a taverna ashore.",
    restaurants:[{name:"Harbour Taverna (Kalamos port)",desc:"Simple, authentic, family-run · Fresh fish caught that morning",url:"https://www.google.com/maps/search/taverna+Kalamos+port+Greece"},{name:"Varka Taverna (Episkopi Bay)",desc:"Legendary remote taverna · Dinghy to the pier · Incredible setting under the pines",url:"https://www.google.com/maps/search/Varka+taverna+Episkopi+Kalamos"}],
    captain:"The longest sailing day — but the route past Arkoudi and Atokos is spectacular. Kalamos port is basic but the atmosphere is unforgettable. Episkopi Bay is one of the best anchorages in the Ionian.",
    diningMode:"either", diningNote:"If you anchor at Episkopi Bay, dinghy to Varka Taverna — it's legendary and worth the trip. At Kalamos port, the harbour taverna is simple but authentic. Or cook aboard and enjoy the silence.",
    activities:[{icon:"🏝️",name:"Swim Stop at Atokos",desc:"Anchor off this uninhabited island for a swim in some of the clearest water in Greece — completely wild"},{icon:"🤿",name:"Snorkel Kalamos Woods Bay",desc:"Turquoise waters, cicadas in the pines, pristine underwater visibility — east coast of Kalamos"},{icon:"🚶",name:"Hike to the Ruined Monastery",desc:"From Episkopi Bay, walk uphill to the abandoned monastery with sweeping views over the strait"},{icon:"🌌",name:"Stargazing",desc:"Zero light pollution on Kalamos — the Milky Way is extraordinary from the cockpit"}],
    images:[
      {url:"https://www.sailionian.com/wp-content/uploads/2024/12/Screenshot-2024-12-07-124510.png",label:"Kalamos island village"},
      {url:"https://www.occyachting.com/wp-content/uploads/2015/10/Kalamos.jpg",label:"Kalamos coastline"}
    ]
  },
  { num:7, day:"Friday", date:"May 8", title:"Kalamos → Sivota (Lefkada)", nm:"~12 NM", time:"~2 hours", note:"Rest day — final anchorage", gradient:"linear-gradient(135deg, #D4A853 0%, #e8d5a3 50%, #D4A853 100%)", emoji:"⚓",
    maps:[{label:"Sivota Bay, Lefkada",url:"https://maps.google.com/?q=38.6350,20.7250",t:"g"},{label:"Scorpios Island (view only)",url:"https://maps.google.com/?q=38.6700,20.7380",t:"g"}],
    route:["Easy morning sail west back toward Lefkada","Pass Scorpios (the former Onassis private island) en route","Arrive Sivota Bay for a lazy final afternoon"],
    about:"Sivota is a stunning natural harbor on Lefkada's southeast coast — a horseshoe bay surrounded by lush green hills, with a tiny waterfront village of excellent tavernas. This is the perfect penultimate night: close to base for an easy return tomorrow, but still feeling wonderfully remote.\n\nEn route, you'll pass Scorpios — the famous private island once owned by Aristotle Onassis. You can't land, but sailing past is a moment.",
    stay:"Pick up a mooring or anchor in the main bay. Space is plentiful and the bay is well-protected. Stern-to on the quay is also possible.",
    restaurants:[{name:"Stavros Taverna",desc:"Right on the waterfront · Excellent grilled fish · Sunset views",url:"https://www.google.com/maps/search/Stavros+Taverna+Sivota+Lefkada"},{name:"Flisvos",desc:"Relaxed harbor setting · Great meze and seafood",url:"https://www.google.com/maps/search/Flisvos+restaurant+Sivota+Lefkada"},{name:"Rachi",desc:"Hillside above Sivota · Incredible sunset views from the terrace · Perfect farewell dinner spot",url:"https://www.google.com/maps/search/Rachi+restaurant+Sivota+Lefkada"}],
    captain:"This is your wind-down day. Short sail, protected bay, great food. Last chance for a proper taverna evening before returning the boat. Rachi restaurant above Sivota has the best sunset view.",
    diningMode:"out", diningNote:"Farewell dinner — Rachi up on the hill is the perfect send-off with sunset views over the islands",
    activities:[{icon:"⛵",name:"Sail Past Scorpios",desc:"The legendary Onassis private island — you can't land, but the views sailing past are iconic"},{icon:"🤿",name:"Snorkel Sivota Bay",desc:"Clear, calm water in the protected bay — great for a final afternoon swim"},{icon:"🍽️",name:"Farewell Dinner at Rachi",desc:"Take a taxi or walk uphill to this legendary restaurant — sunset views over the islands are unforgettable"},{icon:"🏄",name:"Final SUP Session",desc:"Break out the free paddleboard for one last glide around the glassy bay at golden hour"}],
    images:[
      {url:"https://sunnysailing.com/wp-content/uploads/2020/10/bigstock-Traditional-Greek-restaurants-203019943.jpg",label:"Sivota village waterfront"},
      {url:"https://www.sailionian.com/wp-content/uploads/2020/11/AdobeStock_231717475-700x525.jpeg",label:"Sivota Bay, Lefkada"}
    ]
  },
  { num:8, day:"Saturday", date:"May 9", title:"Sivota → Lefkas Marina (Return)", nm:"~8 NM", time:"~1.5 hours", note:"Morning sail back to base", gradient:"linear-gradient(135deg, #2E75B6 0%, #1B3A5C 100%)", emoji:"🏁",
    maps:[{label:"Lefkas Marina",url:"https://maps.google.com/?q=38.8347,20.7069",t:"g"},{label:"Lefkada Town",url:"https://maps.google.com/?q=38.8336,20.7078",t:"g"}],
    route:["Easy morning sail north along Lefkada's coast","Return to Lefkas Marina by midday for check-out"],
    about:"A gentle morning sail back up the coast to Lefkas Marina. The boat needs to be returned by early afternoon, so depart Sivota by 9am. On the way, enjoy one final swim off the stern in a bay near Nidri if time allows.\n\nAfter check-out, Lefkada Town is worth a stroll — colorful houses, Venetian churches, and a pedestrianized main street with cafes and shops.",
    stay:"Return to Lefkas Marina. Complete check-out and disembark. Taxis to Preveza Airport (PVK) ~20 minutes.",
    restaurantHeader:"Farewell Lunch — Lefkada Town",
    restaurants:[{name:"Taverna Eftyhia",desc:"Legendary local souvlaki · Huge portions · Cash only",url:"https://www.google.com/maps/search/Eftyhia+taverna+Lefkada+town"},{name:"Fytopoulos",desc:"Traditional Greek · Excellent value · Town center",url:"https://www.google.com/maps/search/Fytopoulos+restaurant+Lefkada"},{name:"Cafe Plateia",desc:"On the main square · Great coffee and people-watching",url:"https://www.google.com/maps/search/Plateia+cafe+Lefkada+town"}],
    captain:"Easy final sail. Be at the marina by noon for check-out. Lefkada Town is walkable from the marina — grab lunch before heading to the airport.",
    diningMode:"out", diningNote:"Farewell lunch in Lefkada Town — Eftyhia for legendary souvlaki before heading to the airport",
    activities:[{icon:"🏘️",name:"Explore Lefkada Town",desc:"Stroll the colorful streets, visit Venetian churches, browse the pedestrianized shopping street"},{icon:"🍦",name:"Coffee on the Square",desc:"Sit at Cafe Plateia on the main square and reflect on the week"},{icon:"📸",name:"Final Photos at the Marina",desc:"The marina with 600+ boats is photogenic — last group shot before heading home"},{icon:"🎒",name:"Provision for Home",desc:"Pick up olive oil, local honey, and Robola wine from the town shops as souvenirs"}],
    images:[
      {url:"https://www.greeka.com/photos/ionian/lefkada/villages/hero/lefkada-villages-1920.jpg",label:"Lefkada Town"},
      {url:"https://sailingreekwaters.gr/uploads/c36bbd258b7ee694eb987221b2b197b0/2023_03_21/0/0/1679405146.42119a9d66fd9791cf452f85f6b766cf.jpg",label:"Lefkada aerial view"}
    ]
  }
];
// ─── SVG ROUTE MAP ───
function buildRouteMap() {
  const bounds = {latMin:38.30,latMax:38.88,lngMin:20.52,lngMax:20.98};
  const W=800,H=720,pad=40;
  const toXY = (lat,lng) => {
    const x = pad+((lng-bounds.lngMin)/(bounds.lngMax-bounds.lngMin))*(W-pad*2);
    const y = pad+((bounds.latMax-lat)/(bounds.latMax-bounds.latMin))*(H-pad*2);
    return [Math.round(x*10)/10,Math.round(y*10)/10];
  };
  const wp={
    lefkada:toXY(38.8347,20.7069),
    vathi:toXY(38.6653,20.7819),
    kastos:toXY(38.5700,20.9200),
    kioni:toXY(38.4637,20.6930),
    vathyIth:toXY(38.3650,20.7180),
    fiskardo:toXY(38.4570,20.5780),
    kalamos:toXY(38.6250,20.9300),
    sivota:toXY(38.6350,20.7250),
  };
  const lefkada=[[38.83,20.64],[38.82,20.63],[38.80,20.63],[38.78,20.64],[38.76,20.64],[38.74,20.63],[38.72,20.62],[38.70,20.62],[38.68,20.63],[38.66,20.64],[38.64,20.64],[38.63,20.63],[38.62,20.63],[38.63,20.66],[38.64,20.68],[38.63,20.70],[38.64,20.72],[38.65,20.73],[38.66,20.72],[38.68,20.72],[38.69,20.73],[38.70,20.72],[38.72,20.71],[38.74,20.71],[38.76,20.71],[38.78,20.71],[38.80,20.70],[38.82,20.70],[38.83,20.68],[38.84,20.66]].map(([a,b])=>toXY(a,b));
  const meganisi=[[38.68,20.76],[38.67,20.75],[38.66,20.76],[38.65,20.78],[38.66,20.80],[38.67,20.80],[38.68,20.79],[38.68,20.77]].map(([a,b])=>toXY(a,b));
  const ithaca=[[38.47,20.68],[38.46,20.66],[38.44,20.65],[38.42,20.65],[38.40,20.66],[38.38,20.68],[38.36,20.70],[38.35,20.72],[38.36,20.73],[38.38,20.73],[38.40,20.73],[38.42,20.72],[38.44,20.71],[38.45,20.70],[38.46,20.69]].map(([a,b])=>toXY(a,b));
  const kefalonia=[[38.48,20.58],[38.46,20.55],[38.44,20.53],[38.42,20.53],[38.40,20.54],[38.38,20.56],[38.36,20.57],[38.34,20.58],[38.32,20.58],[38.30,20.57],[38.30,20.52],[38.48,20.52],[38.50,20.54],[38.49,20.56]].map(([a,b])=>toXY(a,b));
  const kalamos_i=[[38.64,20.91],[38.63,20.90],[38.61,20.91],[38.60,20.93],[38.61,20.95],[38.63,20.95],[38.64,20.94],[38.65,20.93]].map(([a,b])=>toXY(a,b));
  const kastos_i=[[38.58,20.91],[38.57,20.90],[38.56,20.91],[38.55,20.92],[38.56,20.93],[38.57,20.93],[38.58,20.92]].map(([a,b])=>toXY(a,b));
  const mainland=[[38.88,20.88],[38.85,20.86],[38.82,20.84],[38.80,20.85],[38.78,20.87],[38.75,20.90],[38.72,20.93],[38.70,20.95],[38.68,20.96],[38.65,20.97],[38.62,20.98],[38.58,20.98],[38.55,20.97],[38.52,20.96],[38.50,20.96],[38.48,20.97],[38.45,20.97],[38.42,20.98],[38.38,20.98],[38.35,20.98],[38.30,20.98],[38.30,21.0],[38.88,21.0]].map(([a,b])=>toXY(a,b));
  const N="#1B3A5C",A="#2E75B6",G="#D4A853";
  const path=a=>"M"+a.map(p=>p.join(",")).join("L")+"Z";
  const leg=(a,b)=>`M${a[0]},${a[1]} L${b[0]},${b[1]}`;
  const mid=(a,b)=>[(a[0]+b[0])/2,(a[1]+b[1])/2];
  let svg = `<svg viewBox="0 0 ${W} ${H}" xmlns="http://www.w3.org/2000/svg">
  <defs>
    <linearGradient id="sea" x1="0%" y1="0%" x2="100%" y2="100%"><stop offset="0%" stop-color="#E8F4FD"/><stop offset="100%" stop-color="#D0E6F5"/></linearGradient>
    <linearGradient id="land" x1="0%" y1="0%" x2="0%" y2="100%"><stop offset="0%" stop-color="#C8D9A8"/><stop offset="100%" stop-color="#A8C488"/></linearGradient>
    <linearGradient id="ml" x1="0%" y1="0%" x2="0%" y2="100%"><stop offset="0%" stop-color="#B8C998"/><stop offset="100%" stop-color="#98B478"/></linearGradient>
    <filter id="sh"><feDropShadow dx="1" dy="1" stdDeviation="2" flood-color="#00000020"/></filter>
  </defs>
  <rect width="${W}" height="${H}" fill="url(#sea)"/>`;
  for(let i=1;i<=5;i++) svg+=`<line x1="0" y1="${H*i/6}" x2="${W}" y2="${H*i/6}" stroke="#B8D4E8" stroke-width="0.3" opacity="0.2"/>`;
  for(let i=1;i<=4;i++) svg+=`<line x1="${W*i/5}" y1="0" x2="${W*i/5}" y2="${H}" stroke="#B8D4E8" stroke-width="0.3" opacity="0.2"/>`;
  svg+=`<path d="${path(mainland)}" fill="url(#ml)" stroke="#8BA870" stroke-width="1.5" opacity="0.6"/>`;
  svg+=`<path d="${path(lefkada)}" fill="url(#land)" stroke="#8BA870" stroke-width="1.5"/>`;
  svg+=`<path d="${path(meganisi)}" fill="url(#land)" stroke="#8BA870" stroke-width="1.3"/>`;
  svg+=`<path d="${path(ithaca)}" fill="url(#land)" stroke="#8BA870" stroke-width="1.5"/>`;
  svg+=`<path d="${path(kefalonia)}" fill="url(#land)" stroke="#8BA870" stroke-width="1.5"/>`;
  svg+=`<path d="${path(kalamos_i)}" fill="url(#land)" stroke="#8BA870" stroke-width="1.3"/>`;
  svg+=`<path d="${path(kastos_i)}" fill="url(#land)" stroke="#8BA870" stroke-width="1.2"/>`;
  const lbl=(lat,lng,txt,sz,rot)=>{const p=toXY(lat,lng); return `<text x="${p[0]}" y="${p[1]}" font-family="DM Sans,system-ui" font-size="${sz}" fill="#5A7A40" font-weight="700" text-anchor="middle"${rot?` transform="rotate(${rot} ${p.join(",")})"`:''}>${txt}</text>`;};
  svg+=lbl(38.74,20.66,"LEFKADA",14,-10);
  svg+=lbl(38.665,20.775,"MEGANISI",8,0).replace('700','600');
  svg+=lbl(38.41,20.68,"ITHACA",13,0);
  svg+=lbl(38.40,20.54,"KEFALONIA",13,-5);
  svg+=lbl(38.625,20.92,"KALAMOS",9,0).replace('700','600');
  svg+=lbl(38.565,20.915,"KASTOS",8,0).replace('700','500');
  svg+=lbl(38.60,20.97,"MAINLAND",10,-80).replace('#5A7A40','#6B8050').replace('700','600');
  const legs=[[wp.lefkada,wp.vathi,A,2.5],[wp.vathi,wp.kastos,A,2.5],[wp.kastos,wp.kioni,A,2.5],[wp.kioni,wp.vathyIth,G,2],[wp.vathyIth,wp.fiskardo,A,2.5],[wp.fiskardo,wp.kalamos,A,2.5],[wp.kalamos,wp.sivota,G,2],[wp.sivota,wp.lefkada,N,2.5]];
  legs.forEach(([a,b,c,w],i)=>{
    const op=i===7?"0.45":"0.75";
    svg+=`<path d="${leg(a,b)}" stroke="${c}" stroke-width="${w}" fill="none" stroke-dasharray="${w>2?"8,4":"6,3"}" opacity="${op}"/>`;
  });
  const distLabels=[
    {p:mid(wp.lefkada,wp.vathi),t:"~11 NM",c:A,off:[-30,-8]},
    {p:mid(wp.vathi,wp.kastos),t:"~15 NM",c:A,off:[10,-8]},
    {p:mid(wp.kastos,wp.kioni),t:"~20 NM",c:A,off:[-10,12]},
    {p:mid(wp.kioni,wp.vathyIth),t:"~6 NM",c:G,off:[-45,0]},
    {p:mid(wp.vathyIth,wp.fiskardo),t:"~15 NM",c:A,off:[-10,-8]},
    {p:mid(wp.fiskardo,wp.kalamos),t:"~22 NM",c:A,off:[0,-8]},
    {p:mid(wp.kalamos,wp.sivota),t:"~12 NM",c:G,off:[-10,12]},
    {p:mid(wp.sivota,wp.lefkada),t:"~8 NM",c:N,off:[-35,0]}
  ];
  distLabels.forEach(l=>{
    const x=l.p[0]+(l.off?.[0]||0),y=l.p[1]+(l.off?.[1]||0),tw=l.t.length*6.5+16;
    svg+=`<rect x="${x-tw/2}" y="${y-11}" width="${tw}" height="20" rx="10" fill="white" opacity="0.92" filter="url(#sh)"/>`;
    svg+=`<text x="${x}" y="${y+4}" font-family="DM Sans,system-ui" font-size="10" fill="${l.c}" font-weight="600" text-anchor="middle">${l.t}</text>`;
  });
  const markers=[
    {p:wp.lefkada,label:"LEFKADA ⚓",r:9,c:N,ring:true,lx:12,ly:-2,lw:90},
    {p:wp.vathi,label:"Vathi",r:7,c:A,lx:12,ly:-2,lw:45},
    {p:wp.kastos,label:"Kastos",r:7,c:A,lx:12,ly:-2,lw:52},
    {p:wp.kioni,label:"Kioni",r:7,c:A,lx:-55,ly:-2,lw:45},
    {p:wp.vathyIth,label:"Vathy",r:6,c:G,lx:-55,ly:-2,lw:45},
    {p:wp.fiskardo,label:"Fiskardo ⭐",r:8,c:G,ring:true,lx:-95,ly:-2,lw:85},
    {p:wp.kalamos,label:"Kalamos",r:7,c:A,lx:12,ly:-2,lw:58},
    {p:wp.sivota,label:"Sivota",r:7,c:G,lx:-58,ly:-2,lw:50},
  ];
  markers.forEach(w=>{
    svg+=`<circle cx="${w.p[0]}" cy="${w.p[1]}" r="${w.r}" fill="${w.c}" stroke="white" stroke-width="${w.ring?2.5:2}" filter="url(#sh)"/>`;
    if(w.ring) svg+=`<circle cx="${w.p[0]}" cy="${w.p[1]}" r="${w.r*0.45}" fill="white"/>`;
    if(w.label){
      svg+=`<rect x="${w.p[0]+w.lx}" y="${w.p[1]+w.ly-10}" width="${w.lw}" height="18" rx="9" fill="${w.c}" opacity="0.9" filter="url(#sh)"/>`;
      svg+=`<text x="${w.p[0]+w.lx+w.lw/2}" y="${w.p[1]+w.ly+3}" font-family="DM Sans,system-ui" font-size="${w.ring?10:9.5}" fill="white" font-weight="${w.ring?700:600}" text-anchor="middle">${w.label}</text>`;
    }
  });
  const dayNums=[
    {p:mid(wp.lefkada,wp.vathi),n:"1",off:[20,10]},{p:mid(wp.vathi,wp.kastos),n:"2",off:[20,10]},
    {p:mid(wp.kastos,wp.kioni),n:"3",off:[15,-15]},{p:mid(wp.kioni,wp.vathyIth),n:"4",off:[-25,15]},
    {p:mid(wp.vathyIth,wp.fiskardo),n:"5",off:[15,12]},{p:mid(wp.fiskardo,wp.kalamos),n:"6",off:[15,12]},
    {p:mid(wp.kalamos,wp.sivota),n:"7",off:[15,-10]},{p:mid(wp.sivota,wp.lefkada),n:"8",off:[-15,-15]}
  ];
  dayNums.forEach(d=>{
    const x=d.p[0]+d.off[0],y=d.p[1]+d.off[1];
    svg+=`<circle cx="${x}" cy="${y}" r="10" fill="white" stroke="#D0D5DD" stroke-width="1" opacity="0.9"/>`;
    svg+=`<text x="${x}" y="${y+4}" font-family="DM Sans,system-ui" font-size="10" fill="${N}" font-weight="700" text-anchor="middle">${d.n}</text>`;
  });
  svg+=`<g transform="translate(65,65)"><circle r="22" fill="white" opacity="0.7" stroke="#B8D4E8" stroke-width="1"/><line x1="0" y1="-16" x2="0" y2="16" stroke="#8BA870" stroke-width="1"/><line x1="-16" y1="0" x2="16" y2="0" stroke="#8BA870" stroke-width="1"/><polygon points="0,-14 -3,-6 3,-6" fill="${N}"/><text y="-19" font-family="DM Sans,system-ui" font-size="9" fill="${N}" font-weight="700" text-anchor="middle">N</text></g>`;
  svg+=`<g transform="translate(50,${H-30})"><line x1="0" y1="0" x2="75" y2="0" stroke="${N}" stroke-width="2"/><line x1="0" y1="-3" x2="0" y2="3" stroke="${N}" stroke-width="2"/><line x1="75" y1="-3" x2="75" y2="3" stroke="${N}" stroke-width="2"/><text x="37" y="14" font-family="DM Sans,system-ui" font-size="10" fill="${N}" font-weight="500" text-anchor="middle">~10 NM</text></g>`;
  svg+=`</svg>`;
  return svg;
}
// ─── RENDER ───
function render() {
  const app = document.getElementById('app');
  let html = '';
  html += '<h2>Trip Details</h2><div class="info-grid">';
  infoRows.forEach(([l,v]) => { html += `<div class="info-label">${l}</div><div class="info-value">${v}</div>`; });
  html += '</div>';
  // Cost breakdown
  html += '<h2>Cost Breakdown</h2>';
  html += '<div style="background:white;border-radius:16px;padding:1.5rem 2rem;box-shadow:0 4px 20px rgba(0,0,0,0.06);margin-bottom:2.5rem">';
  html += '<div class="section-label">Fixed Costs (split equally)</div>';
  const fc = costData.fixed;
  const totalFixed = fc.rental + fc.transit + fc.fuel + fc.marinas;
  html += `<div style="display:grid;grid-template-columns:1fr auto;gap:0.3rem 1rem;font-size:0.9rem;margin-bottom:1rem">`;
  html += `<div>Boat rental</div><div style="text-align:right;font-weight:600">€${fc.rental.toLocaleString()}</div>`;
  html += `<div>Transit log (cleaning + linen)</div><div style="text-align:right;font-weight:600">€${fc.transit}</div>`;
  html += `<div>Fuel estimate</div><div style="text-align:right;font-weight:600">~€${fc.fuel}</div>`;
  html += `<div>Marina/mooring fees</div><div style="text-align:right;font-weight:600">~€${fc.marinas}</div>`;
  html += `<div style="border-top:1px solid #E5E7EB;padding-top:0.4rem;font-weight:700;color:var(--navy)">Total fixed (split)</div><div style="border-top:1px solid #E5E7EB;padding-top:0.4rem;text-align:right;font-weight:700;color:var(--navy)">~€${totalFixed.toLocaleString()}</div>`;
  html += '</div>';
  html += '<div class="section-label">Estimated Cost Per Person</div>';
  html += '<div style="display:grid;grid-template-columns:repeat(3,1fr);gap:0.75rem;margin-top:0.5rem">';
  costData.crewOptions.forEach(n => {
    const fixedPP = Math.round(totalFixed / n);
    const provPP = costData.perPersonPerDay * costData.provisionDays;
    const totalPP = fixedPP + provPP;
    html += `<div style="background:var(--light-blue);border-radius:12px;padding:1rem;text-align:center">`;
    html += `<div style="font-size:0.8rem;color:var(--muted);margin-bottom:0.25rem">${n} crew</div>`;
    html += `<div style="font-size:1.5rem;font-weight:700;color:var(--navy)">~€${totalPP}</div>`;
    html += `<div style="font-size:0.75rem;color:var(--muted);margin-top:0.25rem">€${fixedPP} boat + ~€${provPP} food</div>`;
    html += '</div>';
  });
  html += '</div>';
  html += '<p style="font-size:0.78rem;color:var(--muted);margin-top:0.75rem;font-style:italic">Provisioning estimate ~€50/person/day for groceries + eating out. Security deposit (€3,500) is refundable and not included above. Dining ashore varies — budget €20–40/person/meal at tavernas.</p>';
  html += '<div class="section-label mt">Meal Plan at a Glance</div>';
  html += '<div style="display:grid;grid-template-columns:auto 1fr auto;gap:0.25rem 0.75rem;font-size:0.85rem;margin-top:0.5rem">';
  const mealPlan = [
    {day:"Day 1",loc:"Vathi, Meganisi",mode:"🍽️ Eat Out",note:"Errikos"},
    {day:"Day 2",loc:"Kastos",mode:"⛵ Cook Aboard",note:"Sunset dinner on deck"},
    {day:"Day 3",loc:"Kioni, Ithaca",mode:"🍽️ Eat Out",note:"Calypso or Kanenas"},
    {day:"Day 4",loc:"Antisamos anchorage",mode:"⛵ Cook Aboard",note:"BBQ under the stars"},
    {day:"Day 5",loc:"Fiskardo, Kefalonia",mode:"🍽️ Eat Out",note:"Tassia or Nefeli ★"},
    {day:"Day 6",loc:"Kalamos",mode:"🤷 Your Call",note:"Varka Taverna or cook aboard"},
    {day:"Day 7",loc:"Sivota, Lefkada",mode:"🍽️ Eat Out",note:"Farewell at Rachi"},
    {day:"Day 8",loc:"Lefkada Town",mode:"🍽️ Lunch Out",note:"Eftyhia souvlaki"},
  ];
  mealPlan.forEach(m => {
    html += `<div style="font-weight:600;color:var(--navy)">${m.day}</div><div>${m.mode} <span style="color:var(--muted)">· ${m.loc}</span></div><div style="color:var(--muted);font-style:italic">${m.note}</div>`;
  });
  html += '</div>';
  html += '<p style="font-size:0.78rem;color:var(--muted);margin-top:0.5rem">4 eat-out nights + 2 cook-aboard + 1 your-call + 1 lunch = smart budget balance</p>';
  html += '</div>';
  html += '<h2>Getting to Lefkas Marina</h2>';
  html += '<div style="background:white;border-radius:16px;padding:1.5rem 2rem;box-shadow:0 4px 20px rgba(0,0,0,0.06);margin-bottom:2.5rem">';
  html += '<div class="section-label">✈️ Fly to Preveza / Aktion Airport (PVK)</div>';
  html += '<p style="font-size:0.9rem;margin-bottom:0.75rem;line-height:1.6">Preveza (PVK) is the closest airport — just <strong>20–30 minutes</strong> from Lefkas Marina. Seasonal direct flights run May–October from across the UK and Europe.</p>';
  html += '<div style="display:grid;grid-template-columns:1fr 1fr;gap:0.5rem;margin-bottom:1rem">';
  const flights = [
    {from:"London Gatwick",airlines:"easyJet, Jet2",time:"~3h 20min"},{from:"London Stansted",airlines:"Jet2, Ryanair",time:"~3h 20min"},
    {from:"London Heathrow",airlines:"British Airways",time:"~3h 15min"},{from:"Manchester",airlines:"Jet2",time:"~3h 30min"},
    {from:"Birmingham",airlines:"Jet2",time:"~3h 25min"},{from:"Bristol",airlines:"easyJet, Jet2",time:"~3h 15min"},
    {from:"Edinburgh",airlines:"Jet2",time:"~3h 45min"},{from:"Berlin / Düsseldorf",airlines:"easyJet, Eurowings",time:"~2h 30min"},
  ];
  flights.forEach(f => {
    html += `<div style="background:var(--light-blue);border-radius:8px;padding:0.5rem 0.75rem;font-size:0.82rem"><strong style="color:var(--navy)">${f.from}</strong><br><span style="color:var(--muted)">${f.airlines} · ${f.time}</span></div>`;
  });
  html += '</div>';
  html += '<p style="font-size:0.82rem;color:var(--muted);margin-bottom:1rem">💡 Flights from ~£43 return on easyJet. Book early for best prices. <a href="https://www.google.com/travel/flights/flights-from-london-to-preveza.html" target="_blank" style="color:var(--accent)">Search flights on Google Flights →</a></p>';
  html += '<div class="section-label mt">🚕 Airport → Lefkas Marina (22 km)</div>';
  html += '<div style="display:grid;grid-template-columns:1fr 1fr 1fr;gap:0.5rem;margin-bottom:0.75rem">';
  const transfers = [
    {mode:"🚕 Taxi",time:"~20 min",cost:"~€35",note:"Available outside arrivals. Metered — confirm price first."},
    {mode:"🚌 KTEL Bus",time:"~25 min",cost:"~€4",note:"Bus stop 200m from terminal. Weekdays 07:00–20:10. Limited Sat/Sun."},
    {mode:"🚐 Private Transfer",time:"~20 min",cost:"~€40–60",note:"Pre-book for group of 4–8. Air-con minivan, door-to-door."},
  ];
  transfers.forEach(t => {
    html += `<div style="background:var(--sand);border-radius:10px;padding:0.75rem;font-size:0.82rem">`;
    html += `<div style="font-weight:700;color:var(--navy);margin-bottom:0.25rem">${t.mode}</div>`;
    html += `<div><strong>${t.time}</strong> · ${t.cost}</div>`;
    html += `<div style="color:var(--muted);font-size:0.78rem;margin-top:0.25rem">${t.note}</div></div>`;
  });
  html += '</div>';
  html += '<p style="font-size:0.82rem;color:var(--muted);margin-bottom:1rem">The KTEL bus drops you in Lefkada Town — the marina is a <strong>3-minute walk</strong> from the bus stop. Best option if arriving during the day!</p>';
  html += '<div class="section-label mt">💡 Pro Tips</div>';
  html += '<div style="background:var(--light-blue);border-radius:10px;padding:0.75rem 1rem;font-size:0.85rem;line-height:1.6">';
  html += '• <strong>Aim for a lunchtime arrival</strong> — you can provision and be sailing by mid-afternoon<br>';
  html += '• <strong>Provision in Lefkada Town</strong> before boarding — there\'s a supermarket within walking distance of the marina<br>';
  html += '• <strong>Share a taxi/minivan</strong> with crew arriving on the same flight — coordinate in the group chat<br>';
  html += '• <strong>Alternative airports:</strong> Corfu (CFU) has more flights but requires a ferry + bus (~3–4 hours total). Athens (ATH) is 4.5 hours by bus (€37, <a href="https://www.ktelbus.com" target="_blank" style="color:var(--accent)">KTEL bus</a>)<br>';
  html += '• <strong>Greece is GMT+2</strong> (GMT+3 in summer) — 2 hours ahead of the UK';
  html += '</div>';
  html += '</div>';
  html += '<h2>Sailing Route Map</h2>';
  html += '<p style="color:var(--muted);font-size:0.9rem;margin-bottom:1rem">Lefkada → Meganisi → Kastos → Ithaca → Kefalonia → Kalamos → Sivota → Return · Total ~120 NM</p>';
  html += '<div class="map-card">' + buildRouteMap();
  html += '<div class="map-legend"><span><span class="legend-dot" style="background:var(--navy)"></span> Start / End</span>';
  html += '<span><span class="legend-dot" style="background:var(--accent)"></span> Overnight</span>';
  html += '<span><span class="legend-dot" style="background:var(--gold)"></span> Day stop / Highlight</span>';
  html += '<span>Total: ~120 NM</span></div></div>';
  html += '<h2 class="mt">Itinerary Overview</h2><div class="overview">';
  days.forEach(d => {
    html += `<div class="overview-row"><strong>Day ${d.num} (${d.day} ${d.date}):</strong> ${d.title} — ${d.nm}${d.time!=='No sailing'?` <span class="muted">· ${d.time}</span>`:''}</div>`;
  });
  html += '</div>';
  html += '<h2>Cruising Guide</h2>';
  html += '<p style="color:var(--muted);font-size:0.85rem;margin-bottom:1.5rem;font-style:italic">Click each day to expand details, map links, restaurants, and captain\'s notes.</p>';
  days.forEach(d => {
    const isOpen = d.num === 1;
    html += `<div class="day-card"><div class="day-header" style="background:${d.gradient}" onclick="toggleDay(${d.num})"><div>`;
    html += `<div class="day-label">${d.emoji} Day ${d.num} — ${d.day} ${d.date}</div>`;
    html += `<div class="day-title">${d.title}</div>`;
    html += `<div class="day-meta">${d.nm} · ${d.time} · ${d.note}</div>`;
    html += `</div><div class="day-chevron${isOpen?' open':''}" id="chev-${d.num}">▾</div></div>`;
    html += `<div class="day-body${isOpen?' open':''}" id="body-${d.num}">`;
    // ── PHOTO STRIP WITH REAL IMAGES ──
    if (d.images && d.images.length > 0) {
      html += '<div class="photo-strip">';
      d.images.forEach(img => {
        html += `<a href="${img.url}" target="_blank" rel="noopener">`;
        html += `<img src="${img.url}" alt="${img.label}" loading="lazy" onerror="this.parentElement.style.background='linear-gradient(135deg,#667eea,#764ba2)';this.style.display='none';this.parentElement.innerHTML+='<div style=\\'position:absolute;inset:0;display:flex;align-items:center;justify-content:center;color:white;font-size:0.85rem;font-weight:600;text-align:center;padding:0.5rem\\'>${img.label}</div>'">`;
        html += `<div class="photo-label">${img.label}</div>`;
        html += `</a>`;
      });
      html += '</div>';
    }
    html += '<div class="map-links">';
    d.maps.forEach(m => {
      const cls = m.t==='n' ? 'navily' : 'gmaps';
      const icon = m.t==='n' ? '⚓' : '📍';
      html += `<a href="${m.url}" target="_blank" class="map-pill ${cls}">${icon} ${m.label}</a>`;
    });
    html += '</div>';
    if (d.route) {
      html += '<div class="section-label">About the Route</div>';
      html += `<div class="route-box"><div><strong>Distance:</strong> ${d.nm}</div><div><strong>Sailing time:</strong> ${d.time}</div></div>`;
      html += '<ul class="route-list">';
      d.route.forEach(r => html += `<li>${r}</li>`);
      html += '</ul>';
    }
    if (d.isFestival) {
      html += '<div class="festival-box"><div class="festival-title">🎉 The Cultural Highlight of Your Trip 🎉</div><div class="festival-items">';
      d.festivalItems.forEach(f => html += `<div>• ${f}</div>`);
      html += '</div></div>';
    }
    html += `<p class="about-text">${d.about}</p>`;
    html += '<div class="section-label">Where to Stay</div>';
    html += `<p class="stay-text">${d.stay}</p>`;
    if (d.diningMode) {
      const modeColors = { out: {bg:'#EBF5EB',border:'#4CAF50',icon:'🍽️',label:'Eat Out'}, boat: {bg:'#E3F2FD',border:'#2196F3',icon:'⛵',label:'Dine on Board'}, either: {bg:'#FFF8E1',border:'#FFB300',icon:'🤷',label:'Your Call'} };
      const m = modeColors[d.diningMode];
      html += `<div style="background:${m.bg};border:1.5px solid ${m.border};border-radius:12px;padding:0.75rem 1rem;margin-bottom:1rem;display:flex;gap:0.75rem;align-items:flex-start">`;
      html += `<span style="font-size:1.3rem;flex-shrink:0">${m.icon}</span>`;
      html += `<div><div style="font-weight:700;color:var(--navy);font-size:0.9rem;margin-bottom:2px">${m.label} Tonight</div>`;
      html += `<div style="font-size:0.85rem;color:#4A4A4A">${d.diningNote}</div></div></div>`;
    }
    if (d.restaurants && d.diningMode !== 'boat') {
      html += `<div class="section-label">${d.restaurantHeader || 'Best Restaurants'}</div>`;
      d.restaurants.forEach(r => {
        const nameHtml = r.url ? `<a href="${r.url}" target="_blank" style="color:var(--navy);text-decoration:none;border-bottom:1px dashed var(--accent)">${r.name}</a>` : r.name;
        html += `<div class="restaurant-row"><span class="star">⭐</span><div><div class="restaurant-name">${nameHtml}</div><div class="restaurant-desc">${r.desc}</div></div></div>`;
      });
    } else if (d.restaurants && d.diningMode === 'boat') {
      html += `<div class="section-label" style="opacity:0.6">Nearby Options (if you change your mind)</div>`;
      d.restaurants.forEach(r => {
        const nameHtml = r.url ? `<a href="${r.url}" target="_blank" style="color:var(--muted);text-decoration:none;border-bottom:1px dashed #ccc">${r.name}</a>` : r.name;
        html += `<div class="restaurant-row" style="opacity:0.65"><span class="star">📍</span><div><div class="restaurant-name" style="color:var(--muted)">${nameHtml}</div><div class="restaurant-desc">${r.desc}</div></div></div>`;
      });
    }
    if (d.activities) {
      html += '<div class="section-label mt">Things to Do</div><div class="activities-grid">';
      d.activities.forEach(a => {
        const nameHtml = a.url ? `<a href="${a.url}" target="_blank" style="color:var(--navy);text-decoration:none;border-bottom:1px dashed var(--accent)">${a.name}</a>` : a.name;
        html += `<div class="activity-card"><span class="activity-icon">${a.icon}</span><div><div class="activity-name">${nameHtml}</div><div class="activity-desc">${a.desc}</div></div></div>`;
      });
      html += '</div>';
    }
    html += `<div class="captain-box"><span class="captain-label">🧑‍✈️ Captain Notes — </span>${d.captain}</div>`;
    html += '</div></div>';
  });
  html += '<h2 style="margin-top:2rem">Useful Information</h2><div class="info-grid" style="margin-bottom:2rem">';
  [["Marina","Lefkas Marina · 620 berths"],["Airport","Aktion/Preveza (PVK) · ~20 min"],["Facilities","Water, electric, fuel, showers, supermarket"],["Town","Lefkada Town walkable from marina"],["Sailing Area","South Ionian · Sheltered, short distances"],["Emergency","Port Police: +30 26450 31200"]].forEach(([l,v])=>{
    html+=`<div class="info-label">${l}</div><div class="info-value">${v}</div>`;
  });
  html += '</div>';
  html += '<div class="footer">South Ionian Sailing Week · May 2–9, 2026 · Fair winds and following seas ⛵</div>';
  app.innerHTML = html;
}
function toggleDay(n) {
  const body = document.getElementById('body-'+n);
  const chev = document.getElementById('chev-'+n);
  body.classList.toggle('open');
  chev.classList.toggle('open');
}
render();
</script>
</body>
</html>
