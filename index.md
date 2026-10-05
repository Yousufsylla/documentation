<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<meta name="theme-color" content="#111827">
<title>YS LERNE DEUTSCH — Deutsch sprechen. Jeden Tag.</title>

<style>
:root{
  --bg:#f5f7fb;
  --card:#ffffff;
  --text:#172033;
  --muted:#697386;
  --primary:#d71920;
  --primary-dark:#a90f15;
  --accent:#ffcc00;
  --border:#e3e7ef;
  --success:#159447;
  --shadow:0 12px 35px rgba(0,0,0,.08);
}

*{box-sizing:border-box}

body{
  margin:0;
  font-family:Inter,Arial,Helvetica,sans-serif;
  background:var(--bg);
  color:var(--text);
  transition:.25s;
}

body.dark{
  --bg:#0d1117;
  --card:#161b22;
  --text:#f1f5f9;
  --muted:#aab4c3;
  --border:#293241;
  --shadow:0 12px 35px rgba(0,0,0,.3);
}

button,select,input{
  font:inherit;
}

button{
  cursor:pointer;
}

.hidden{
  display:none!important;
}

/* HOME */

#home{
  min-height:100vh;
  display:flex;
  align-items:center;
  justify-content:center;
  padding:25px;
}

.home-box{
  text-align:center;
  max-width:600px;
}

.logo{
  width:150px;
  height:150px;
  border-radius:50%;
  margin:0 auto 25px;
  display:flex;
  align-items:center;
  justify-content:center;
  background:
    linear-gradient(135deg,#111 0 33%,#d71920 33% 66%,#ffcc00 66%);
  color:white;
  font-size:42px;
  font-weight:900;
  border:6px solid white;
  box-shadow:var(--shadow);
}

.home-title{
  font-size:clamp(28px,6vw,48px);
  font-weight:900;
  margin:0 0 28px;
}

.start-btn{
  border:0;
  background:var(--primary);
  color:white;
  padding:15px 30px;
  border-radius:14px;
  font-size:18px;
  font-weight:800;
  box-shadow:0 8px 22px rgba(215,25,32,.25);
}

.start-btn:hover{
  background:var(--primary-dark);
  transform:translateY(-1px);
}

/* APP */

#app{
  min-height:100vh;
}

header{
  position:sticky;
  top:0;
  z-index:20;
  background:var(--card);
  border-bottom:1px solid var(--border);
  padding:13px 18px;
}

.header-inner{
  max-width:1200px;
  margin:auto;
  display:flex;
  align-items:center;
  gap:15px;
  justify-content:space-between;
}

.brand{
  font-weight:900;
  white-space:nowrap;
}

.header-actions{
  display:flex;
  align-items:center;
  gap:8px;
}

.icon-btn{
  border:1px solid var(--border);
  background:var(--card);
  color:var(--text);
  border-radius:10px;
  padding:8px 11px;
}

/* CONTROLS */

.controls{
  max-width:1200px;
  margin:20px auto;
  padding:0 18px;
}

.control-grid{
  display:grid;
  grid-template-columns:1fr 1fr 1fr;
  gap:12px;
}

.control{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:14px;
  padding:11px 13px;
}

.control label{
  display:block;
  font-size:12px;
  color:var(--muted);
  margin-bottom:5px;
  font-weight:700;
}

.control select,
.control input{
  width:100%;
  border:0;
  outline:0;
  background:transparent;
  color:var(--text);
}

.search-box{
  grid-column:1/-1;
}

/* LEVELS */

.levels{
  max-width:1200px;
  margin:0 auto 20px;
  padding:0 18px;
}

.level-grid{
  display:grid;
  grid-template-columns:repeat(5,1fr);
  gap:10px;
}

.level-btn{
  padding:14px 8px;
  border:1px solid var(--border);
  border-radius:12px;
  background:var(--card);
  color:var(--text);
  font-weight:900;
}

.level-btn.active{
  background:var(--primary);
  color:white;
  border-color:var(--primary);
}

/* LESSON LIST */

.lessons{
  max-width:1200px;
  margin:auto;
  padding:0 18px 50px;
}

.section-title{
  margin:25px 0 12px;
  font-size:22px;
}

.lesson-grid{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:12px;
}

.lesson-card{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:15px;
  padding:16px;
  box-shadow:var(--shadow);
  cursor:pointer;
  transition:.2s;
}

.lesson-card:hover{
  transform:translateY(-2px);
}

.lesson-card.done{
  border-left:5px solid var(--success);
}

.lesson-number{
  color:var(--primary);
  font-weight:900;
  font-size:13px;
}

.lesson-title{
  margin-top:6px;
  font-weight:800;
}

.lesson-topic{
  color:var(--muted);
  font-size:13px;
  margin-top:5px;
}

/* LESSON */

#lessonView{
  max-width:1050px;
  margin:25px auto;
  padding:0 18px 60px;
}

.back-btn{
  border:1px solid var(--border);
  background:var(--card);
  color:var(--text);
  padding:10px 14px;
  border-radius:10px;
  margin-bottom:15px;
}

.lesson-head{
  background:var(--card);
  border:1px solid var(--border);
  border-radius:18px;
  padding:22px;
  box-shadow:var(--shadow);
}

.lesson-head h1{
  margin:5px 0;
}

.lesson-head p{
  color:var(--muted);
}

.block{
  margin-top:15px;
  background:var(--card);
  border:1px solid var(--border);
  border-radius:18px;
  padding:22px;
}

.block h2{
  margin-top:0;
}

.grammar-box{
  background:rgba(215,25,32,.07);
  border-left:5px solid var(--primary);
  padding:14px;
  border-radius:8px;
}

.vocab-grid{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:10px;
}

.vocab{
  border:1px solid var(--border);
  border-radius:10px;
  padding:12px;
}

.vocab strong{
  display:block;
}

.vocab small{
  color:var(--muted);
}

.dialogue{
  display:flex;
  flex-direction:column;
  gap:10px;
}

.line{
  border-radius:12px;
  padding:12px;
  max-width:90%;
}

.line.sofia{
  background:#fff0f0;
  align-self:flex-start;
}

.line.youssuf{
  background:#fff8d9;
  align-self:flex-end;
}

body.dark .line.sofia{
  background:#3a2022;
}

body.dark .line.youssuf{
  background:#3c351b;
}

.line strong{
  display:block;
  margin-bottom:4px;
}

.listen{
  border:0;
  background:var(--primary);
  color:white;
  padding:7px 10px;
  border-radius:8px;
  margin-top:7px;
  font-size:12px;
}

.exercise{
  padding:16px;
  border:1px solid var(--border);
  border-radius:12px;
  margin-bottom:12px;
}

.exercise input{
  width:100%;
  padding:10px;
  margin-top:8px;
  border:1px solid var(--border);
  border-radius:8px;
  background:var(--bg);
  color:var(--text);
}

.check{
  margin-top:10px;
  border:0;
  background:var(--primary);
  color:white;
  padding:9px 14px;
  border-radius:9px;
}

.correction{
  margin-top:10px;
  font-weight:700;
}

.good{
  color:var(--success);
}

.bad{
  color:var(--primary);
}

.play-all{
  border:0;
  background:#111827;
  color:white;
  padding:12px 17px;
  border-radius:10px;
  font-weight:800;
}

body.dark .play-all{
  background:#f1f5f9;
  color:#111827;
}

.progress-wrap{
  margin-top:15px;
  background:var(--border);
  height:9px;
  border-radius:99px;
  overflow:hidden;
}

.progress-bar{
  height:100%;
  background:var(--primary);
  width:0;
}

/* RESPONSIVE */

@media(max-width:850px){
  .control-grid{
    grid-template-columns:1fr 1fr;
  }

  .lesson-grid{
    grid-template-columns:repeat(2,1fr);
  }

  .level-grid{
    grid-template-columns:repeat(5,1fr);
  }
}

@media(max-width:600px){
  .header-inner{
    flex-wrap:wrap;
  }

  .control-grid{
    grid-template-columns:1fr;
  }

  .search-box{
    grid-column:auto;
  }

  .level-grid{
    grid-template-columns:repeat(2,1fr);
  }

  .lesson-grid{
    grid-template-columns:1fr;
  }

  .vocab-grid{
    grid-template-columns:1fr;
  }

  .line{
    max-width:100%;
  }
}
</style>
</head>

<body>

<!-- ACCUEIL -->
<section id="home">
  <div class="home-box">
    <div class="logo">YS</div>

    <h1 class="home-title">
      Deutsch sprechen. Jeden Tag.
    </h1>

    <button class="start-btn" onclick="startApp()">
      🚀 Commencer
    </button>
  </div>
</section>


<!-- APPLICATION -->
<section id="app" class="hidden">

<header>
  <div class="header-inner">

    <div class="brand">
      YS LERNE DEUTSCH
    </div>

    <div class="header-actions">
      <button class="icon-btn" onclick="goHome()">⌂</button>
      <button class="icon-btn" onclick="toggleDark()" id="darkBtn">🌙</button>
    </div>

  </div>
</header>


<!-- COMMANDES -->

<div class="controls">

  <div class="control-grid">

    <div class="control">
      <label>Langue d’apprentissage</label>
      <select disabled>
        <option>🇩🇪 Deutsch</option>
      </select>
    </div>

    <div class="control">
      <label>Langue d’explication</label>

      <select id="supportLanguage" onchange="changeSupportLanguage()">

        <option value="fr">🇫🇷 Français</option>
        <option value="en">🇬🇧 English</option>
        <option value="es">🇪🇸 Español</option>
        <option value="it">🇮🇹 Italiano</option>
        <option value="pt">🇵🇹 Português</option>
        <option value="nl">🇳🇱 Nederlands</option>
        <option value="pl">🇵🇱 Polski</option>
        <option value="tr">🇹🇷 Türkçe</option>
        <option value="ar">🇸🇦 العربية</option>
        <option value="ru">🇷🇺 Русский</option>
        <option value="uk">🇺🇦 Українська</option>
        <option value="ro">🇷🇴 Română</option>
        <option value="el">🇬🇷 Ελληνικά</option>
        <option value="ja">🇯🇵 日本語</option>
        <option value="ko">🇰🇷 한국어</option>
        <option value="zh">🇨🇳 中文</option>
        <option value="hi">🇮🇳 हिन्दी</option>
        <option value="bn">🇧🇩 বাংলা</option>
        <option value="vi">🇻🇳 Tiếng Việt</option>
        <option value="sw">🇹🇿 Kiswahili</option>
        <option value="zu">🇿🇦 isiZulu</option>
        <option value="xh">🇿🇦 isiXhosa</option>
        <option value="af">🇿🇦 Afrikaans</option>
        <option value="yo">🇳🇬 Yorùbá</option>
        <option value="ha">🇳🇬 Hausa</option>
        <option value="ig">🇳🇬 Igbo</option>
        <option value="am">🇪🇹 Amharic</option>
        <option value="wo">🇸🇳 Wolof</option>
        <option value="bm">🇲🇱 Bambara</option>

      </select>
    </div>

    <div class="control">
      <label>Recherche</label>
      <input
        id="search"
        type="search"
        placeholder="Rechercher une leçon..."
        oninput="renderLessons()"
      >
    </div>

  </div>

</div>


<!-- NIVEAUX -->

<div class="levels">

  <div class="level-grid">

    <button class="level-btn active" onclick="selectLevel('A1',this)">A1</button>
    <button class="level-btn" onclick="selectLevel('A2',this)">A2</button>
    <button class="level-btn" onclick="selectLevel('B1',this)">B1</button>
    <button class="level-btn" onclick="selectLevel('B2',this)">B2</button>
    <button class="level-btn" onclick="selectLevel('C1',this)">C1</button>

  </div>

</div>


<!-- LISTE DES LEÇONS -->

<section id="lessonList" class="lessons">

  <h2 class="section-title" id="levelTitle">
    A1 — 40 leçons
  </h2>

  <div id="lessonGrid" class="lesson-grid"></div>

</section>


<!-- VUE LEÇON -->

<section id="lessonView" class="hidden"></section>

</section>


<script>

/* =========================================================
   CONFIGURATION
========================================================= */

const LEVELS = ["A1","A2","B1","B2","C1"];

const LEVEL_INFO = {

  A1:{
    title:"A1 — Grundlagen",
    description:"Premiers échanges, phrases simples, vocabulaire quotidien.",
    grammar:[
      "sein / haben",
      "présent",
      "articles der / die / das",
      "accusatif",
      "nominatif",
      "verbes réguliers",
      "verbes irréguliers fréquents",
      "questions",
      "négation",
      "possessifs"
    ]
  },

  A2:{
    title:"A2 — Alltag",
    description:"Situations quotidiennes et communication plus développée.",
    grammar:[
      "datif",
      "prépositions avec accusatif",
      "prépositions avec datif",
      "Perfekt",
      "Präteritum de sein et haben",
      "verbes séparables",
      "comparatif",
      "superlatif",
      "pronoms personnels",
      "subordonnées simples"
    ]
  },

  B1:{
    title:"B1 — Selbstständig",
    description:"Communication autonome et construction de textes.",
    grammar:[
      "Nebensätze",
      "weil / dass / obwohl",
      "Konjunktiv II",
      "Futur I",
      "Passiv",
      "Relativsätze",
      "Plusquamperfekt",
      "verbes avec prépositions",
      "connecteurs",
      "discours indirect simple"
    ]
  },

  B2:{
    title:"B2 — Sicher sprechen",
    description:"Argumentation, précision et allemand professionnel.",
    grammar:[
      "Passiv avancé",
      "Konjunktiv II avancé",
      "Partizipialkonstruktionen",
      "nominalisation",
      "Relativsätze avancés",
      "discours indirect",
      "connecteurs complexes",
      "infinitif avec zu",
      "style formel",
      "structures complexes"
    ]
  },

  C1:{
    title:"C1 — Fortgeschritten",
    description:"Expression précise, académique et professionnelle.",
    grammar:[
      "Genitiv",
      "Konjunktiv I",
      "discours indirect avancé",
      "structures participiales",
      "nominalisation avancée",
      "inversion stylistique",
      "connecteurs académiques",
      "nuances modales",
      "style administratif",
      "syntaxe complexe"
    ]
  }

};


/* =========================================================
   200 SUJETS
========================================================= */

const TOPICS = {

A1:[
"Se présenter",
"Saluer quelqu’un",
"Parler de sa famille",
"Dire où l’on habite",
"Parler de son âge",
"Les nombres",
"Les jours de la semaine",
"L’heure",
"Le calendrier",
"Les couleurs",
"Les objets de la maison",
"La chambre",
"La cuisine",
"Faire les courses",
"Au supermarché",
"Commander une boisson",
"Au restaurant",
"Parler de nourriture",
"Les vêtements",
"Faire des achats",
"Les transports",
"À la gare",
"Demander son chemin",
"La ville",
"Le travail",
"Les professions",
"Une journée normale",
"Le matin",
"Le soir",
"Les loisirs",
"Le sport",
"La météo",
"Le week-end",
"Prendre rendez-vous",
"Chez le médecin",
"À la pharmacie",
"À l’hôtel",
"Voyager",
"Les vacances",
"Révision A1"
],

A2:[
"Raconter sa journée",
"Parler de ses habitudes",
"Décrire son logement",
"Changer de logement",
"Faire une invitation",
"Accepter une invitation",
"Refuser poliment",
"Organiser une sortie",
"Parler du passé",
"Raconter un voyage",
"Une expérience importante",
"Les transports publics",
"Un retard de train",
"À l’aéroport",
"Réserver un hôtel",
"Un problème à l’hôtel",
"Au restaurant",
"Une réclamation",
"Au travail",
"Un nouveau collègue",
"Une réunion simple",
"Prendre un rendez-vous",
"Annuler un rendez-vous",
"Chez le médecin",
"Parler de sa santé",
"Les études",
"Apprendre une langue",
"Internet",
"Les réseaux sociaux",
"Le téléphone",
"Faire des projets",
"Le futur",
"Comparer deux choses",
"Donner son opinion",
"Conseiller quelqu’un",
"Demander de l’aide",
"Résoudre un problème",
"Raconter une histoire",
"Une journée spéciale",
"Révision A2"
],

B1:[
"Parler de ses objectifs",
"Changer de travail",
"Un entretien d’embauche",
"Écrire un CV",
"Le monde professionnel",
"Travailler en équipe",
"Résoudre un conflit",
"Donner une opinion",
"Défendre une idée",
"Exprimer un désaccord",
"Les études supérieures",
"Choisir une formation",
"Apprendre efficacement",
"Les médias",
"Les informations",
"Les réseaux sociaux",
"La technologie",
"L’intelligence artificielle",
"Le télétravail",
"L’environnement",
"Le climat",
"Les transports modernes",
"La ville de demain",
"Voyager seul",
"Voyager en groupe",
"Les différences culturelles",
"Vivre à l’étranger",
"Les relations sociales",
"L’amitié",
"La communication",
"La santé",
"Le stress",
"L’équilibre de vie",
"Les habitudes alimentaires",
"Le sport",
"Les achats en ligne",
"Les services publics",
"Les problèmes administratifs",
"Débat du quotidien",
"Révision B1"
],

B2:[
"Présenter un projet",
"Convaincre une équipe",
"Négocier",
"Une réunion professionnelle",
"Une présentation",
"Prendre la parole",
"Argumenter",
"Contredire poliment",
"Analyser un problème",
"Proposer une solution",
"Le marché du travail",
"Le leadership",
"La responsabilité",
"Le management",
"La communication professionnelle",
"Le monde numérique",
"La cybersécurité",
"L’intelligence artificielle",
"L’automatisation",
"L’économie",
"La consommation",
"Le développement durable",
"Les changements climatiques",
"La politique locale",
"La société",
"L’éducation",
"Les médias modernes",
"La publicité",
"La culture",
"L’art",
"La littérature",
"Les différences culturelles",
"La mondialisation",
"L’immigration",
"L’intégration",
"Les générations",
"Les relations professionnelles",
"Débat avancé",
"Révision B2"
],

C1:[
"Présenter une analyse",
"Construire une argumentation",
"Défendre une thèse",
"Nuancer une opinion",
"Analyser un discours",
"Le langage académique",
"Une présentation universitaire",
"Écrire un rapport",
"Écrire une synthèse",
"Faire une critique",
"Le monde professionnel",
"La stratégie d’entreprise",
"La prise de décision",
"La gestion des risques",
"L’économie mondiale",
"La transformation numérique",
"L’intelligence artificielle",
"L’éthique technologique",
"Les médias et la société",
"La désinformation",
"La démocratie",
"Les institutions",
"La politique internationale",
"L’environnement",
"La transition énergétique",
"Les migrations",
"L’intégration sociale",
"Les inégalités",
"L’éducation moderne",
"La recherche",
"La science",
"La culture contemporaine",
"La littérature allemande",
"Les enjeux sociaux",
"Les changements démographiques",
"La mondialisation",
"Le travail du futur",
"Débat académique",
"Révision C1"
]

};


/* =========================================================
   GÉNÉRATION DES 200 LEÇONS
========================================================= */

const lessons=[];

let globalId=1;

for(const level of LEVELS){

  TOPICS[level].forEach((topic,index)=>{

    lessons.push({
      id:globalId++,
      level,
      number:index+1,
      topic,
      grammar:LEVEL_INFO[level].grammar[index % LEVEL_INFO[level].grammar.length]
    });

  });

}


/* =========================================================
   VOCABULAIRE
========================================================= */

const VOCAB={

A1:[
["Hallo","Bonjour"],
["Guten Morgen","Bonjour / bon matin"],
["Danke","Merci"],
["Bitte","S’il vous plaît / de rien"],
["Freund","Ami"],
["Familie","Famille"],
["Haus","Maison"],
["Wohnung","Appartement"],
["Arbeit","Travail"],
["Schule","École"],
["Bahnhof","Gare"],
["Stadt","Ville"],
["Essen","Nourriture"],
["Wasser","Eau"],
["Zeit","Temps"]
],

A2:[
["Erfahrung","Expérience"],
["Einladung","Invitation"],
["Termin","Rendez-vous"],
["Gesundheit","Santé"],
["Reise","Voyage"],
["Gewohnheit","Habitude"],
["Problem","Problème"],
["Lösung","Solution"],
["Zukunft","Futur"],
["Vergangenheit","Passé"],
["Meinung","Opinion"],
["Vorschlag","Proposition"],
["Entscheidung","Décision"],
["Verkehr","Circulation"],
["Umwelt","Environnement"]
],

B1:[
["Ziel","Objectif"],
["Bewerbung","Candidature"],
["Erfahrung","Expérience"],
["Ausbildung","Formation"],
["Verantwortung","Responsabilité"],
["Zusammenarbeit","Collaboration"],
["Beziehung","Relation"],
["Gesellschaft","Société"],
["Nachricht","Information / message"],
["Technologie","Technologie"],
["Umwelt","Environnement"],
["Gesundheit","Santé"],
["Gewohnheit","Habitude"],
["Möglichkeit","Possibilité"],
["Entwicklung","Développement"]
],

B2:[
["Verhandlung","Négociation"],
["Argument","Argument"],
["Vorteil","Avantage"],
["Nachteil","Inconvénient"],
["Entscheidung","Décision"],
["Führung","Direction / leadership"],
["Verantwortung","Responsabilité"],
["Wirtschaft","Économie"],
["Verbrauch","Consommation"],
["Nachhaltigkeit","Durabilité"],
["Gesellschaft","Société"],
["Globalisierung","Mondialisation"],
["Integration","Intégration"],
["Kommunikation","Communication"],
["Strategie","Stratégie"]
],

C1:[
["Auseinandersetzung","Analyse / confrontation"],
["Behauptung","Affirmation"],
["Begründung","Justification"],
["Zusammenhang","Lien / contexte"],
["Voraussetzung","Condition préalable"],
["Auswirkung","Conséquence"],
["Herausforderung","Défi"],
["Entwicklung","Évolution"],
["Forschung","Recherche"],
["Wissenschaft","Science"],
["Gleichberechtigung","Égalité"],
["Nachhaltigkeit","Durabilité"],
["Verantwortung","Responsabilité"],
["Wahrnehmung","Perception"],
["Bewertung","Évaluation"]
]

};


/* =========================================================
   LANGUES D'EXPLICATION
========================================================= */

const SUPPORT_TRANSLATIONS={

fr:{
 explain:"Explication",
 vocab:"Vocabulaire",
 grammar:"Grammaire",
 dialogue:"Dialogue",
 exercise:"Exercice",
 correction:"Correction",
 instruction:"Complète la phrase en allemand."
},

en:{
 explain:"Explanation",
 vocab:"Vocabulary",
 grammar:"Grammar",
 dialogue:"Dialogue",
 exercise:"Exercise",
 correction:"Correction",
 instruction:"Complete the sentence in German."
},

es:{
 explain:"Explicación",
 vocab:"Vocabulario",
 grammar:"Gramática",
 dialogue:"Diálogo",
 exercise:"Ejercicio",
 correction:"Corrección",
 instruction:"Completa la frase en alemán."
},

it:{
 explain:"Spiegazione",
 vocab:"Vocabolario",
 grammar:"Grammatica",
 dialogue:"Dialogo",
 exercise:"Esercizio",
 correction:"Correzione",
 instruction:"Completa la frase in tedesco."
},

pt:{
 explain:"Explicação",
 vocab:"Vocabulário",
 grammar:"Gramática",
 dialogue:"Diálogo",
 exercise:"Exercício",
 correction:"Correção",
 instruction:"Completa a frase em alemão."
},

nl:{
 explain:"Uitleg",
 vocab:"Woordenschat",
 grammar:"Grammatica",
 dialogue:"Dialoog",
 exercise:"Oefening",
 correction:"Correctie",
 instruction:"Vul de zin in het Duits aan."
},

pl:{
 explain:"Wyjaśnienie",
 vocab:"Słownictwo",
 grammar:"Gramatyka",
 dialogue:"Dialog",
 exercise:"Ćwiczenie",
 correction:"Korekta",
 instruction:"Uzupełnij zdanie po niemiecku."
},

tr:{
 explain:"Açıklama",
 vocab:"Kelime bilgisi",
 grammar:"Dilbilgisi",
 dialogue:"Diyalog",
 exercise:"Alıştırma",
 correction:"Düzeltme",
 instruction:"Cümleyi Almanca tamamlayın."
},

ar:{
 explain:"الشرح",
 vocab:"المفردات",
 grammar:"القواعد",
 dialogue:"الحوار",
 exercise:"التمرين",
 correction:"التصحيح",
 instruction:"أكمل الجملة باللغة الألمانية."
},

ru:{
 explain:"Объяснение",
 vocab:"Словарь",
 grammar:"Грамматика",
 dialogue:"Диалог",
 exercise:"Упражнение",
 correction:"Исправление",
 instruction:"Дополните предложение на немецком."
},

uk:{
 explain:"Пояснення",
 vocab:"Словник",
 grammar:"Граматика",
 dialogue:"Діалог",
 exercise:"Вправа",
 correction:"Виправлення",
 instruction:"Доповніть речення німецькою."
},

ro:{
 explain:"Explicație",
 vocab:"Vocabular",
 grammar:"Gramatică",
 dialogue:"Dialog",
 exercise:"Exercițiu",
 correction:"Corectare",
 instruction:"Completează propoziția în germană."
},

el:{
 explain:"Επεξήγηση",
 vocab:"Λεξιλόγιο",
 grammar:"Γραμματική",
 dialogue:"Διάλογος",
 exercise:"Άσκηση",
 correction:"Διόρθωση",
 instruction:"Συμπλήρωσε την πρόταση στα γερμανικά."
},

ja:{
 explain:"説明",
 vocab:"語彙",
 grammar:"文法",
 dialogue:"会話",
 exercise:"練習",
 correction:"訂正",
 instruction:"ドイツ語で文を完成させてください。"
},

ko:{
 explain:"설명",
 vocab:"어휘",
 grammar:"문법",
 dialogue:"대화",
 exercise:"연습",
 correction:"교정",
 instruction:"독일어 문장을 완성하세요."
},

zh:{
 explain:"解释",
 vocab:"词汇",
 grammar:"语法",
 dialogue:"对话",
 exercise:"练习",
 correction:"纠正",
 instruction:"用德语完成句子。"
},

hi:{
 explain:"व्याख्या",
 vocab:"शब्दावली",
 grammar:"व्याकरण",
 dialogue:"संवाद",
 exercise:"अभ्यास",
 correction:"सुधार",
 instruction:"जर्मन में वाक्य पूरा करें।"
},

bn:{
 explain:"ব্যাখ্যা",
 vocab:"শব্দভাণ্ডার",
 grammar:"ব্যাকরণ",
 dialogue:"সংলাপ",
 exercise:"অনুশীলন",
 correction:"সংশোধন",
 instruction:"জার্মান ভাষায় বাক্যটি সম্পূর্ণ করুন।"
},

vi:{
 explain:"Giải thích",
 vocab:"Từ vựng",
 grammar:"Ngữ pháp",
 dialogue:"Hội thoại",
 exercise:"Bài tập",
 correction:"Sửa lỗi",
 instruction:"Hoàn thành câu bằng tiếng Đức."
},

sw:{
 explain:"Maelezo",
 vocab:"Msamiati",
 grammar:"Sarufi",
 dialogue:"Mazungumzo",
 exercise:"Zoezi",
 correction:"Marekebisho",
 instruction:"Kamilisha sentensi kwa Kijerumani."
},

zu:{
 explain:"Incazelo",
 vocab:"Amagama",
 grammar:"Uhlelo lolimi",
 dialogue:"Ingxoxo",
 exercise:"Umsebenzi",
 correction:"Ukulungiswa",
 instruction:"Qedela umusho ngesiJalimane."
},

xh:{
 explain:"Ingcaciso",
 vocab:"Isigama",
 grammar:"Igrama",
 dialogue:"Incoko",
 exercise:"Umsebenzi",
 correction:"Ukulungiswa",
 instruction:"Gqibezela isivakalisi ngesiJamani."
},

af:{
 explain:"Verduideliking",
 vocab:"Woordeskat",
 grammar:"Grammatika",
 dialogue:"Dialoog",
 exercise:"Oefening",
 correction:"Regstelling",
 instruction:"Voltooi die sin in Duits."
},

yo:{
 explain:"Àlàyé",
 vocab:"Àwọn ọ̀rọ̀",
 grammar:"Gírámà",
 dialogue:"Ìjíròrò",
 exercise:"Ìdánwò",
 correction:"Àtúnṣe",
 instruction:"Parí gbolohun náà ní èdè Jámánì."
},

ha:{
 explain:"Bayani",
 vocab:"Kalmomi",
 grammar:"Nahawu",
 dialogue:"Tattaunawa",
 exercise:"Motsa jiki",
 correction:"Gyara",
 instruction:"Kammala jimlar da Jamusanci."
},

ig:{
 explain:"Nkọwa",
 vocab:"Okwu",
 grammar:"Ụtọasụsụ",
 dialogue:"Mkparịta ụka",
 exercise:"Mmega ahụ",
 correction:"Ndozi",
 instruction:"Mezue ahịrịokwu ahụ n'asụsụ German."
},

am:{
 explain:"ማብራሪያ",
 vocab:"ቃላት",
 grammar:"ሰዋሰው",
 dialogue:"ውይይት",
 exercise:"ልምምድ",
 correction:"ማስተካከያ",
 instruction:"ዓረፍተ ነገሩን በጀርመንኛ ያጠናቅቁ።"
},

wo:{
 explain:"Leeral",
 vocab:"Baati",
 grammar:"Njàngum làkk",
 dialogue:"Waxtaan",
 exercise:"Jéem",
 correction:"Jubbanti",
 instruction:"Mottali kàddu gi ci almaaŋ."
},

bm:{
 explain:"Kumakan",
 vocab:"Dɔnkiliw",
 grammar:"Kan ka kuma",
 dialogue:"Kumaɲɔgɔn",
 exercise:"Kɛcogo",
 correction:"Sɛbɛnni",
 instruction:"A bɛɛda kuma in ka German kan."
}

};


/* =========================================================
   ÉTAT
========================================================= */

let currentLevel="A1";
let currentLesson=null;

const completed=
  JSON.parse(localStorage.getItem("ys_completed")||"[]");


/* =========================================================
   NAVIGATION
========================================================= */

function startApp(){

  document.getElementById("home").classList.add("hidden");
  document.getElementById("app").classList.remove("hidden");

  renderLessons();
}

function goHome(){

  document.getElementById("app").classList.add("hidden");
  document.getElementById("home").classList.remove("hidden");

  document.getElementById("lessonView").classList.add("hidden");
  document.getElementById("lessonList").classList.remove("hidden");
}


/* =========================================================
   NIVEAUX
========================================================= */

function selectLevel(level,button){

  currentLevel=level;

  document.querySelectorAll(".level-btn")
    .forEach(b=>b.classList.remove("active"));

  button.classList.add("active");

  renderLessons();
}


/* =========================================================
   LISTE
========================================================= */

function renderLessons(){

  const grid=document.getElementById("lessonGrid");
  const search=document.getElementById("search").value.toLowerCase();

  const list=lessons.filter(l=>
    l.level===currentLevel &&
    (
      l.topic.toLowerCase().includes(search) ||
      l.grammar.toLowerCase().includes(search) ||
      String(l.number).includes(search)
    )
  );

  document.getElementById("levelTitle").textContent=
    `${currentLevel} — 40 leçons`;

  grid.innerHTML="";

  list.forEach(lesson=>{

    const card=document.createElement("div");

    card.className=
      "lesson-card "+
      (completed.includes(lesson.id)?"done":"");

    card.onclick=()=>openLesson(lesson.id);

    card.innerHTML=`

      <div class="lesson-number">
        Leçon ${lesson.number}
      </div>

      <div class="lesson-title">
        ${escapeHTML(lesson.topic)}
      </div>

      <div class="lesson-topic">
        ${escapeHTML(lesson.grammar)}
      </div>

      ${
        completed.includes(lesson.id)
        ? '<div class="good">✓ Terminée</div>'
        : ''
      }

    `;

    grid.appendChild(card);

  });

}


/* =========================================================
   LEÇON
========================================================= */

function openLesson(id){

  const lesson=lessons.find(l=>l.id===id);

  if(!lesson)return;

  currentLesson=lesson;

  document.getElementById("lessonList")
    .classList.add("hidden");

  const view=document.getElementById("lessonView");

  view.classList.remove("hidden");

  renderLesson(lesson);
}


/* =========================================================
   RENDU LEÇON
========================================================= */

function renderLesson(lesson){

  const lang=
    document.getElementById("supportLanguage").value;

  const t=
    SUPPORT_TRANSLATIONS[lang] ||
    SUPPORT_TRANSLATIONS.fr;

  const vocab=
    VOCAB[lesson.level] || VOCAB.A1;

  const dialogue=
    buildDialogue(lesson);

  const exercises=
    buildExercises(lesson);

  const percentage=
    completed.includes(lesson.id)?100:0;

  const view=document.getElementById("lessonView");

  view.innerHTML=`

    <button class="back-btn" onclick="backToLessons()">
      ← Retour aux leçons
    </button>

    <div class="lesson-head">

      <div class="lesson-number">
        ${lesson.level} · LEÇON ${lesson.number}
      </div>

      <h1>
        ${escapeHTML(lesson.topic)}
      </h1>

      <p>
        ${escapeHTML(LEVEL_INFO[lesson.level].description)}
      </p>

      <div class="progress-wrap">
        <div
          class="progress-bar"
          style="width:${percentage}%"
        ></div>
      </div>

    </div>


    <!-- GRAMMAIRE -->

    <div class="block">

      <h2>
        📘 ${t.grammar}
      </h2>

      <div class="grammar-box">

        <strong>Deutsch:</strong>

        <p>
          Heute lernen wir:
          <b>${escapeHTML(lesson.grammar)}</b>.
        </p>

        <hr>

        <strong>${t.explain} :</strong>

        <p>
          Cette leçon travaille la structure
          <b>${escapeHTML(lesson.grammar)}</b>
          à travers des situations naturelles en allemand.
        </p>

      </div>

    </div>


    <!-- VOCABULAIRE -->

    <div class="block">

      <h2>
        🧠 ${t.vocab}
      </h2>

      <div class="vocab-grid">

        ${
          vocab.map(v=>`

            <div class="vocab">

              <strong>
                ${escapeHTML(v[0])}
              </strong>

              <small>
                ${escapeHTML(v[1])}
              </small>

              <br>

              <button
                class="listen"
                onclick="speakGerman('${escapeJS(v[0])}')"
              >
                🔊 Écouter
              </button>

            </div>

          `).join("")
        }

      </div>

    </div>


    <!-- DIALOGUE -->

    <div class="block">

      <h2>
        💬 ${t.dialogue}
      </h2>

      <button
        class="play-all"
        onclick="playDialogue()"
      >
        🔊 Écouter tout le dialogue
      </button>

      <div class="dialogue" id="dialogue">

        ${
          dialogue.map((line,i)=>`

            <div class="line ${line.person==='Sofia'?'sofia':'youssuf'}">

              <strong>
                ${line.person}
              </strong>

              <div>
                ${escapeHTML(line.de)}
              </div>

              <small>
                ${escapeHTML(line.translation)}
              </small>

              <br>

              <button
                class="listen"
                onclick="speakGerman('${escapeJS(line.de)}')"
              >
                🔊 Écouter
              </button>

            </div>

          `).join("")
        }

      </div>

    </div>


    <!-- EXERCICES -->

    <div class="block">

      <h2>
        ✏️ ${t.exercise}
      </h2>

      <p>
        ${escapeHTML(t.instruction)}
      </p>

      ${
        exercises.map((ex,i)=>`

          <div class="exercise">

            <strong>
              ${i+1}. ${escapeHTML(ex.question)}
            </strong>

            <input
              id="answer-${i}"
              placeholder="Réponse en allemand..."
            >

            <button
              class="check"
              onclick="checkAnswer(${i})"
            >
              Vérifier
            </button>

            <div
              id="correction-${i}"
              class="correction"
            ></div>

          </div>

        `).join("")
      }

      <button
        class="check"
        onclick="completeLesson()"
      >
        ✓ Marquer la leçon comme terminée
      </button>

    </div>

  `;

  window.currentExercises=exercises;

}


/* =========================================================
   DIALOGUES
========================================================= */

function buildDialogue(lesson){

  const topic=lesson.topic;

  const base=[

    ["Sofia",`Hallo Youssuf. Heute sprechen wir über ${topic}.`],
    ["Youssuf",`Ja, gerne. Das ist ein interessantes Thema.`],
    ["Sofia",`Was denkst du darüber?`],
    ["Youssuf",`Ich habe schon einige Erfahrungen damit.`],
    ["Sofia",`Kannst du mir davon erzählen?`],
    ["Youssuf",`Natürlich. Zuerst möchte ich die Situation erklären.`],
    ["Sofia",`Was ist dabei besonders wichtig?`],
    ["Youssuf",`Meiner Meinung nach ist eine gute Vorbereitung sehr wichtig.`],
    ["Sofia",`Warum denkst du das?`],
    ["Youssuf",`Weil man dadurch sicherer sprechen und handeln kann.`],
    ["Sofia",`Das klingt logisch.`],
    ["Youssuf",`Außerdem hilft es, wenn man die richtigen Wörter kennt.`],
    ["Sofia",`Welche Wörter benutzt du normalerweise?`],
    ["Youssuf",`Ich versuche, einfache und klare Ausdrücke zu benutzen.`],
    ["Sofia",`Machst du manchmal Fehler?`],
    ["Youssuf",`Natürlich. Fehler gehören zum Lernen dazu.`],
    ["Sofia",`Wie verbesserst du dich?`],
    ["Youssuf",`Ich wiederhole neue Wörter und spreche regelmäßig Deutsch.`],
    ["Sofia",`Das ist eine gute Methode.`],
    ["Youssuf",`Ja, regelmäßiges Üben macht einen großen Unterschied.`],
    ["Sofia",`Was würdest du einem Deutschlernenden empfehlen?`],
    ["Youssuf",`Ich würde jeden Tag ein bisschen Deutsch lernen.`],
    ["Sofia",`Auch wenn man wenig Zeit hat?`],
    ["Youssuf",`Ja. Schon zehn oder fünfzehn Minuten können helfen.`],
    ["Sofia",`Und was sollte man mit neuen Wörtern machen?`],
    ["Youssuf",`Man sollte sie in eigenen Sätzen benutzen.`],
    ["Sofia",`Das hilft wahrscheinlich beim Sprechen.`],
    ["Youssuf",`Genau. Man muss die Sprache aktiv benutzen.`],
    ["Sofia",`Dann lass uns heute weiterüben.`],
    ["Youssuf",`Sehr gerne. Ich bin bereit.`],
    ["Sofia",`Super. Dann beginnen wir mit unserer Aufgabe.`],
    ["Youssuf",`Einverstanden. Ich versuche, so viel Deutsch wie möglich zu sprechen.`],
    ["Sofia",`Perfekt. Genau darum geht es bei dieser Lektion.`],
    ["Youssuf",`Dann machen wir weiter.`],
    ["Sofia",`Viel Erfolg!`],
    ["Youssuf",`Danke, Sofia. Dir auch!`]

  ];

  return base.map(([person,de])=>({

    person,
    de,
    translation:
      person==="Sofia"
      ? frenchTranslation(de)
      : frenchTranslation(de)

  }));

}


/* =========================================================
   TRADUCTION DE SECOURS
========================================================= */

function frenchTranslation(text){

  const map={

    "Hallo":"Bonjour",
    "Heute":"Aujourd’hui",
    "sprechen":"parler",
    "über":"à propos de",
    "Ja":"Oui",
    "gerne":"avec plaisir",
    "interessantes Thema":"sujet intéressant",
    "Was denkst du darüber?":"Qu’en penses-tu ?",
    "Natürlich":"Bien sûr",
    "Warum":"Pourquoi",
    "Meiner Meinung nach":"À mon avis",
    "sehr wichtig":"très important",
    "Das klingt logisch.":"Cela semble logique.",
    "Fehler gehören zum Lernen dazu.":"Les erreurs font partie de l’apprentissage.",
    "jeden Tag":"chaque jour",
    "Viel Erfolg!":"Bonne réussite !",
    "Danke":"Merci"

  };

  let result=text;

  Object.keys(map)
    .sort((a,b)=>b.length-a.length)
    .forEach(k=>{
      result=result.replace(k,map[k]);
    });

  return result;
}


/* =========================================================
   EXERCICES
========================================================= */

function buildExercises(lesson){

  const n=lesson.number;

  const exercises=[];

  exercises.push({

    question:
      `Ergänze: „Ich ______ heute über ${lesson.topic.toLowerCase()}.“`,

    answers:["spreche","spreche heute","rede"]

  });

  exercises.push({

    question:
      `Ergänze: „Ich finde dieses Thema ______.“`,

    answers:["interessant"]

  });

  exercises.push({

    question:
      `Ergänze: „Ich möchte mein Deutsch ______.“`,

    answers:["verbessern"]

  });

  exercises.push({

    question:
      `Ergänze: „Ich lerne Deutsch, ______ ich besser sprechen möchte.“`,

    answers:["weil"]

  });

  exercises.push({

    question:
      `Ergänze: „Wenn ich Zeit habe, ______ ich Deutsch.“`,

    answers:["lerne"]

  });

  return exercises;

}


/* =========================================================
   CORRECTION
========================================================= */

function checkAnswer(index){

  const ex=window.currentExercises[index];

  const input=
    document.getElementById(`answer-${index}`);

  const output=
    document.getElementById(`correction-${index}`);

  const answer=
    input.value.trim().toLowerCase();

  const good=
    ex.answers.some(a=>
      answer===a.toLowerCase()
    );

  if(good){

    output.className="correction good";

    output.textContent=
      "✓ Correct ! Sehr gut.";

  }else{

    output.className="correction bad";

    output.textContent=
      "✗ Correction : "+ex.answers[0];

  }

}


/* =========================================================
   TERMINER
========================================================= */

function completeLesson(){

  if(!currentLesson)return;

  if(!completed.includes(currentLesson.id)){

    completed.push(currentLesson.id);

    localStorage.setItem(
      "ys_completed",
      JSON.stringify(completed)
    );

  }

  const bar=document.querySelector(".progress-bar");

  if(bar){
    bar.style.width="100%";
  }

  alert("✓ Leçon terminée !");

}


/* =========================================================
   RETOUR
========================================================= */

function backToLessons(){

  document.getElementById("lessonView")
    .classList.add("hidden");

  document.getElementById("lessonList")
    .classList.remove("hidden");

  renderLessons();

}


/* =========================================================
   AUDIO
========================================================= */

function speakGerman(text){

  if(!("speechSynthesis" in window)){

    alert("La lecture audio n'est pas disponible sur cet appareil.");

    return;
  }

  speechSynthesis.cancel();

  const utterance=
    new SpeechSynthesisUtterance(text);

  utterance.lang="de-DE";
  utterance.rate=.9;
  utterance.pitch=1;

  const voices=
    speechSynthesis.getVoices();

  const german=
    voices.find(v=>
      v.lang &&
      v.lang.toLowerCase().startsWith("de")
    );

  if(german){
    utterance.voice=german;
  }

  speechSynthesis.speak(utterance);

}


function playDialogue(){

  if(!currentLesson)return;

  const dialogue=
    buildDialogue(currentLesson);

  speechSynthesis.cancel();

  let i=0;

  function next(){

    if(i>=dialogue.length)return;

    const utterance=
      new SpeechSynthesisUtterance(
        dialogue[i].de
      );

    utterance.lang="de-DE";
    utterance.rate=.88;

    utterance.onend=()=>{

      i++;

      setTimeout(next,250);

    };

    speechSynthesis.speak(utterance);

  }

  next();

}


/* =========================================================
   LANGUE
========================================================= */

function changeSupportLanguage(){

  if(currentLesson){
    renderLesson(currentLesson);
  }

}


/* =========================================================
   DARK MODE
========================================================= */

function toggleDark(){

  document.body.classList.toggle("dark");

  const dark=
    document.body.classList.contains("dark");

  localStorage.setItem(
    "ys_dark",
    dark?"1":"0"
  );

  document.getElementById("darkBtn")
    .textContent=
      dark?"☀️":"🌙";

}


/* =========================================================
   UTILITAIRES
========================================================= */

function escapeHTML(value){

  return String(value)
    .replaceAll("&","&amp;")
    .replaceAll("<","&lt;")
    .replaceAll(">","&gt;")
    .replaceAll('"',"&quot;")
    .replaceAll("'","&#039;");

}

function escapeJS(value){

  return String(value)
    .replaceAll("\\","\\\\")
    .replaceAll("'","\\'")
    .replaceAll("\n"," ");

}


/* =========================================================
   INITIALISATION
========================================================= */

if(localStorage.getItem("ys_dark")==="1"){

  document.body.classList.add("dark");

  document.getElementById("darkBtn").textContent="☀️";

}


/* Charge les voix audio */

if("speechSynthesis" in window){

  speechSynthesis.onvoiceschanged=()=>{

    speechSynthesis.getVoices();

  };

}

</script>

</body>
</html>
