<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Słownictwo: polityka, prawo i wybory</title>
<style>
:root{
  --bg:#f3f4fb;--card:#ffffff;--card2:#f6f7fd;--text:#1d2140;--muted:#666c92;
  --primary:#4f46e5;--primary2:#7c3aed;--ink:#ffffff;
  --ok:#15803d;--okbg:#dcfce7;--bad:#b91c1c;--badbg:#fee2e2;--warn:#b45309;
  --border:#e1e4f3;--shadow:0 8px 30px rgba(45,55,130,.10);
}
:root[data-theme="dark"]{
  --bg:#0e1126;--card:#171b36;--card2:#1e2342;--text:#e9eafc;--muted:#9ba2cf;
  --primary:#818cf8;--primary2:#a78bfa;--ink:#0e1126;
  --ok:#4ade80;--okbg:#10331f;--bad:#fca5a5;--badbg:#3d1621;--warn:#fbbf24;
  --border:#2b3160;--shadow:none;
}
@media (prefers-color-scheme:dark){
  :root:not([data-theme="light"]){
    --bg:#0e1126;--card:#171b36;--card2:#1e2342;--text:#e9eafc;--muted:#9ba2cf;
    --primary:#818cf8;--primary2:#a78bfa;--ink:#0e1126;
    --ok:#4ade80;--okbg:#10331f;--bad:#fca5a5;--badbg:#3d1621;--warn:#fbbf24;
    --border:#2b3160;--shadow:none;
  }
}
*{box-sizing:border-box}
html{-webkit-text-size-adjust:100%}
body{
  margin:0;background:var(--bg);color:var(--text);
  font-family:system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;line-height:1.5;
  background-image:radial-gradient(900px 420px at 100% -10%,rgba(124,58,237,.14),transparent),
                   radial-gradient(700px 420px at -10% 0,rgba(79,70,229,.14),transparent);
  background-attachment:fixed;
}
button,select,input{font:inherit;color:inherit}
.wrap{max-width:880px;margin:0 auto;padding:18px 14px 40px}
header{background:var(--card);border:1px solid var(--border);border-radius:20px;padding:18px 20px;box-shadow:var(--shadow);margin-bottom:14px}
.top{display:flex;justify-content:space-between;align-items:flex-start;gap:12px}
h1{margin:0;font-size:clamp(1.25rem,4vw,1.7rem);letter-spacing:-.01em}
.sub{margin:4px 0 0;color:var(--muted);font-size:.95rem}
.mastery{display:grid;grid-template-columns:1fr auto;gap:4px 12px;align-items:center;margin-top:14px;font-size:.9rem;color:var(--muted)}
.mastery b{color:var(--text)}
.mastery .bar{grid-column:1/-1}
.icon-btn{border:1px solid var(--border);background:var(--card2);border-radius:12px;padding:8px 11px;cursor:pointer;font-size:1.05rem;line-height:1}
.icon-btn:hover{border-color:var(--primary)}
#tabs{display:flex;gap:8px;overflow-x:auto;padding:4px 2px 12px;scrollbar-width:thin}
.tab{flex:0 0 auto;display:flex;align-items:center;gap:7px;padding:9px 14px;border-radius:999px;border:1px solid var(--border);background:var(--card);cursor:pointer;font-weight:600;font-size:.92rem;white-space:nowrap;transition:.15s}
.tab:hover{border-color:var(--primary);transform:translateY(-1px)}
.tab.active{background:linear-gradient(135deg,var(--primary),var(--primary2));color:var(--ink);border-color:transparent}
.badge{font-size:.72rem;padding:1px 7px;border-radius:99px;background:var(--card2);color:var(--muted)}
.badge:empty{display:none}
.badge.gold{background:var(--okbg);color:var(--ok)}
.card{background:var(--card);border:1px solid var(--border);border-radius:20px;padding:22px;box-shadow:var(--shadow);min-height:420px}
@media (max-width:560px){.card{padding:16px}}
.ex-head h2{margin:0 0 2px;font-size:1.25rem}
.muted{color:var(--muted)}
.ex-head p{margin:0 0 4px;font-size:.93rem}
.center{text-align:center;justify-content:center}
.hidden{display:none!important}
.row{display:flex;flex-wrap:wrap;gap:10px;margin-top:16px}
.row.center{justify-content:center}
.btn{padding:.7em 1.15em;border-radius:12px;border:1px solid var(--border);background:var(--card2);font-weight:650;cursor:pointer;transition:.15s}
.btn:hover:not(:disabled){border-color:var(--primary);transform:translateY(-1px)}
.btn:disabled{opacity:.45;cursor:not-allowed}
.btn.primary{background:linear-gradient(135deg,var(--primary),var(--primary2));color:var(--ink);border-color:transparent}
.topline{display:flex;justify-content:space-between;gap:8px;font-size:.88rem;color:var(--muted);margin:14px 0 6px}
.bar{height:8px;background:var(--card2);border:1px solid var(--border);border-radius:99px;overflow:hidden}
.bar>i{display:block;height:100%;width:0;background:linear-gradient(90deg,var(--primary),var(--primary2));transition:width .3s}
.prompt{text-align:center;padding:20px 8px 6px}
.big{font-size:clamp(1.6rem,5.2vw,2.3rem);font-weight:800;letter-spacing:-.01em;overflow-wrap:anywhere}
.prompt .muted{font-size:.9rem;margin-top:4px}
.opts{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:14px}
@media (max-width:560px){.opts{grid-template-columns:1fr}}
.opt,.pbtn{display:flex;gap:12px;align-items:center;text-align:left;padding:13px 15px;border:2px solid var(--border);background:var(--card2);border-radius:14px;cursor:pointer;transition:.15s;font-size:1rem}
.opt:hover:not(:disabled),.pbtn:hover:not(:disabled){border-color:var(--primary);transform:translateY(-1px)}
.opt kbd{flex:0 0 auto;min-width:26px;height:26px;display:inline-grid;place-items:center;border-radius:8px;background:var(--card);border:1px solid var(--border);font-size:.8rem;font-weight:700;color:var(--muted)}
.opt:disabled{cursor:default}
.opt:disabled:not(.correct):not(.wrong){opacity:.55}
.correct{border-color:var(--ok)!important;background:var(--okbg)!important}
.wrong{border-color:var(--bad)!important;background:var(--badbg)!important}
.feedback{min-height:1.6em;margin-top:14px;font-weight:650}
.feedback.ok{color:var(--ok)}
.feedback.bad{color:var(--bad)}
@keyframes shake{0%,100%{transform:translateX(0)}25%{transform:translateX(-7px)}75%{transform:translateX(7px)}}
.shake{animation:shake .35s}
@keyframes pop{0%{transform:scale(1)}50%{transform:scale(1.04)}100%{transform:scale(1)}}
.correct{animation:pop .3s}
.txt{width:100%;padding:14px 16px;border-radius:14px;border:2px solid var(--border);background:var(--card2);font-size:1.15rem;outline:none;margin-top:14px}
.txt:focus{border-color:var(--primary)}
.txt.ok{border-color:var(--ok);background:var(--okbg)}
.txt.bad{border-color:var(--bad);background:var(--badbg)}
.hintline{font-family:ui-monospace,Menlo,Consolas,monospace;letter-spacing:.12em;margin-top:10px;min-height:1.5em;color:var(--primary);font-weight:700}
.pairs{display:grid;grid-template-columns:1fr 1fr;gap:18px;margin-top:10px}
.pairs>div{display:flex;flex-direction:column;gap:10px}
.pbtn.sel{border-color:var(--primary);box-shadow:0 0 0 3px rgba(99,102,241,.28)}
.pbtn.matched{border-color:var(--ok);background:var(--okbg);opacity:.7;cursor:default}
.pbtn{font-size:.95rem;min-height:52px}
.sent{padding:12px 14px;border:2px solid var(--border);border-radius:14px;background:var(--card2);line-height:2.1;margin-top:10px}
.sent .num{color:var(--muted);font-weight:700;margin-right:6px}
.sent .pl{font-size:.88rem;color:var(--muted);line-height:1.4;font-style:italic}
.sent .ans{font-size:.9rem;color:var(--bad);font-weight:700;line-height:1.4}
select.gap,select.sel{padding:5px 8px;border-radius:10px;border:2px solid var(--primary);background:var(--card);max-width:100%}
select.gap.correct{border-color:var(--ok);background:var(--okbg)}
select.gap.wrong{border-color:var(--bad);background:var(--badbg)}
.bank{display:flex;flex-wrap:wrap;gap:8px;margin:14px 0 4px}
.chip{padding:4px 12px;border-radius:99px;background:var(--card2);border:1px solid var(--border);font-size:.9rem;font-weight:600;transition:.15s}
.chip.used{opacity:.3;text-decoration:line-through}
.tf-card{display:grid;gap:6px;text-align:center;padding:26px 14px;border-radius:18px;margin-top:14px;background:linear-gradient(135deg,rgba(79,70,229,.10),rgba(124,58,237,.10));border:1px solid var(--border)}
.tf-eq{color:var(--muted);font-size:1.5rem;line-height:1}
.tf-card .big{font-size:clamp(1.3rem,4.5vw,1.9rem)}
.tf-btns{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:14px}
.tf-btns .btn{padding:.9em;font-size:1.05rem}
.slots,.tiles{display:flex;flex-wrap:wrap;gap:7px;justify-content:center}
.slots{min-height:64px;padding:12px;border:2px dashed var(--border);border-radius:14px;margin-top:12px;align-items:center}
.tiles{margin-top:16px}
.tile{width:44px;height:48px;border-radius:11px;border:2px solid var(--primary);background:var(--card);font-weight:800;font-size:1.2rem;text-transform:uppercase;cursor:pointer;transition:.12s}
.tile:hover{transform:translateY(-2px)}
.tile.used{opacity:.15;pointer-events:none}
.slots.ok{border-color:var(--ok);background:var(--okbg)}
.slots.ok .tile{border-color:var(--ok)}
.pool{display:flex;flex-wrap:wrap;gap:8px;min-height:62px;padding:12px;border-radius:14px;background:var(--card2);border:1px solid var(--border);margin:14px 0}
.sortgrid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
@media (max-width:560px){.sortgrid{grid-template-columns:1fr}}
.bucket{border:2px dashed var(--border);border-radius:14px;padding:10px;min-height:118px;background:var(--card2);cursor:pointer;transition:.15s}
.bucket:hover,.bucket.over{border-color:var(--primary)}
.bucket h4{margin:0 0 8px;font-size:.95rem}
.bbody{display:flex;flex-wrap:wrap;gap:6px}
.sitem{display:inline-flex;flex-direction:column;padding:6px 12px;border-radius:12px;background:var(--card);border:2px solid var(--primary);cursor:grab;user-select:none;line-height:1.25}
.sitem b{font-size:.95rem}
.sitem small{color:var(--muted);font-size:.72rem}
.sitem.sel{background:var(--primary);color:var(--ink)}
.sitem.sel small{color:var(--ink);opacity:.8}
.sitem.correct,.sitem.wrong{cursor:default}
.sitem .fix{color:var(--bad);font-weight:700}
.mem{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-top:14px}
.mcard{perspective:800px;border:0;background:none;padding:0;height:96px;cursor:pointer}
.minner{position:relative;width:100%;height:100%;transition:transform .45s;transform-style:preserve-3d}
.mcard.up .minner{transform:rotateY(180deg)}
.mface{position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:12px;display:flex;align-items:center;justify-content:center;text-align:center;padding:6px;font-weight:700;font-size:clamp(.66rem,2.4vw,.95rem);line-height:1.2;overflow-wrap:anywhere}
.mback{background:linear-gradient(135deg,var(--primary),var(--primary2));color:var(--ink);font-size:1.6rem}
.mfront{background:var(--card2);border:2px solid var(--primary);transform:rotateY(180deg)}
.mcard.pl .mfront{border-color:var(--primary2)}
.mcard.done .mfront{background:var(--okbg);border-color:var(--ok)}
.controls{display:flex;flex-wrap:wrap;gap:8px;align-items:center;margin:12px 0 4px}
.controls label{display:flex;align-items:center;gap:6px;font-size:.9rem;color:var(--muted);cursor:pointer}
.flash{perspective:1000px;height:250px;cursor:pointer;margin:16px 0;outline:none}
.flash:focus-visible{outline:3px solid var(--primary);outline-offset:4px;border-radius:20px}
.flash-inner{position:relative;height:100%;transition:transform .5s;transform-style:preserve-3d}
.flash.flipped .flash-inner{transform:rotateY(180deg)}
.face{position:absolute;inset:0;backface-visibility:hidden;-webkit-backface-visibility:hidden;border-radius:20px;display:flex;flex-direction:column;align-items:center;justify-content:center;gap:8px;padding:22px;text-align:center}
.face.front{background:linear-gradient(135deg,var(--primary),var(--primary2));color:var(--ink)}
.face.back{background:var(--card2);border:2px solid var(--primary);transform:rotateY(180deg)}
.ft{font-size:clamp(1.5rem,5vw,2.2rem);font-weight:800;overflow-wrap:anywhere;line-height:1.2}
.tag{font-size:.75rem;padding:2px 10px;border-radius:99px;background:rgba(255,255,255,.22);font-weight:600}
.tap{font-size:.78rem;opacity:.75}
.ex{color:var(--muted);font-style:italic}
.actions{display:flex;gap:10px;justify-content:center;align-items:center}
.actions .btn{min-width:130px}
.result{text-align:center;padding:30px 10px}
.trophy{font-size:4rem;line-height:1.1}
.result h2{margin:8px 0 0;font-size:1.8rem}
.result .score{font-size:1.1rem;font-weight:700;color:var(--primary);margin:4px 0 8px}
#confetti{position:fixed;inset:0;pointer-events:none;z-index:50}
footer{text-align:center;color:var(--muted);font-size:.85rem;margin-top:18px}
footer button{background:none;border:0;color:var(--muted);text-decoration:underline;cursor:pointer;font-size:.85rem}
@media (prefers-reduced-motion:reduce){*{animation:none!important;transition:none!important}}
</style>
</head>
<body>
<canvas id="confetti"></canvas>
<div class="wrap">
  <header>
    <div class="top">
      <div>
        <h1>🏛️ Słownictwo: polityka, prawo i wybory</h1>
        <p class="sub" id="sub"></p>
      </div>
      <button class="icon-btn" id="theme" title="Zmień motyw (jasny / ciemny)" aria-label="Zmień motyw">🌓</button>
    </div>
    <div class="mastery">
      <span>Opanowanie słownictwa (średni najlepszy wynik)</span><b id="mpct">0%</b>
      <div class="bar"><i id="mbar"></i></div>
    </div>
  </header>
  <nav id="tabs" aria-label="Ćwiczenia"></nav>
  <main id="stage" class="card"></main>
  <footer>
    Wynik ≥ 80% = zielona odznaka ✔ · Skróty klawiszowe są opisane w każdym ćwiczeniu ·
    <button id="reset">Wyzeruj postępy</button>
  </footer>
</div>
<noscript>Ta strona wymaga włączonego JavaScriptu.</noscript>

<script>
'use strict';

/* ============================================================
   DANE — słownictwo
   ============================================================ */
const GROUPS = {
  a: 'Wybory i polityka',
  b: 'Przestępstwa i zasady (s. 56)',
  c: 'Vocabulary Challenge (s. 110)'
};
/* c = kategoria do ćwiczenia „Sortowanie”: inst, party, law, system */
const A = [
  {en:'election', pl:'wybory', c:'system'},
  {en:'vote', pl:'głosować / głos', c:'system'},
  {en:'MP (Member of Parliament)', pl:'poseł do parlamentu', c:'inst', ans:['Member of Parliament']},
  {en:'government', pl:'rząd', c:'inst', conflict:'cabinet', ans:['cabinet']},
  {en:'House of Commons', pl:'Izba Gmin (w brytyjskim parlamencie)', c:'inst'},
  {en:'House of Lords', pl:'Izba Lordów (w brytyjskim parlamencie)', c:'inst'},
  {en:'Senate', pl:'Senat', c:'inst'},
  {en:'prime minister', pl:'premier', c:'inst'},
  {en:'president', pl:'prezydent', c:'inst'},
  {en:'chancellor', pl:'kanclerz', c:'inst'},
  {en:'republic', pl:'republika', c:'system'},
  {en:'monarchy', pl:'monarchia', c:'system'},
  {en:'Conservative', pl:'konserwatysta / Partia Konserwatywna', c:'party'},
  {en:'Labour', pl:'Partia Pracy', c:'party'},
  {en:'Liberal Democrats', pl:'Liberalni Demokraci', c:'party'},
  {en:'Republicans', pl:'Republikanie', c:'party'},
  {en:'electorate', pl:'elektorat / wyborcy', c:'system'},
  {en:'constitution', pl:'konstytucja', c:'system'},
  {en:'constituency', pl:'okręg wyborczy', c:'system'},
  {en:'manifesto', pl:'manifest wyborczy', c:'system'},
  {en:'policy', pl:'polityka (rządowa / programowa)', c:'system'},
  {en:'referendum', pl:'referendum', c:'system'},
  {en:'cabinet', pl:'gabinet (rząd)', c:'inst', conflict:'government'},
  {en:'the Opposition', pl:'opozycja', c:'party'},
  {en:'the minority', pl:'mniejszość', c:'party'},
  {en:'the coalition', pl:'koalicja', c:'party'},
  {en:'citizen', pl:'obywatel'},
  {en:'minister', pl:'minister', c:'inst'},
  {en:'civil servant', pl:'urzędnik państwowy', c:'inst'}
];
const B = [
  {en:'break the rules', pl:'łamać zasady', c:'law'},
  {en:'shoplifting', pl:'kradzież sklepowa', c:'law'},
  {en:'shoplifter', pl:'złodziej sklepowy', c:'law'},
  {en:'prosecute', pl:'ścigać sądownie / wytoczyć proces', c:'law'},
  {en:'fine', pl:'grzywna / kara pieniężna', c:'law'},
  {en:'community service', pl:'prace społeczne', c:'law'},
  {en:'commit a crime', pl:'popełnić przestępstwo', c:'law'},
  {en:'legal high', pl:'dopalacz (legalna substancja o działaniu narkotycznym)', c:'law'},
  {en:'designer drugs', pl:'narkotyki syntetyczne / projektowane', c:'law'},
  {en:'attendance', pl:'frekwencja'},
  {en:'crisis', pl:'kryzys'},
  {en:'strike', pl:'strajk'},
  {en:'protest', pl:'protest / protestować'},
  {en:'punish', pl:'karać', c:'law'}
];
const C = [
  {en:'debate', pl:'debata / debatować'},
  {en:'form', pl:'utworzyć / formować (np. rząd)', ex:'form a government'},
  {en:'stand', pl:'kandydować (np. w wyborach)', ex:'stand for election'},
  {en:'serve', pl:'pełnić (np. dwie kadencje)', ex:'serve two terms'},
  {en:'pass', pl:'uchwalić (np. prawo)', ex:'pass a law'},
  {en:'hold', pl:'przeprowadzić / organizować (np. wybory)', ex:'hold an election'},
  {en:'inform', pl:'informować (forma formalna)'},
  {en:'enter', pl:'wejść (forma formalna)'},
  {en:'result in', pl:'skutkować czymś / prowadzić do czegoś'},
  {en:'legislation', pl:'ustawodawstwo / prawo', c:'law'},
  {en:'charged', pl:'oskarżony', c:'law'},
  {en:'allow', pl:'pozwalać / zezwalać'}
];
const V = [
  ...A.map(x => ({...x, g:'a'})),
  ...B.map(x => ({...x, g:'b'})),
  ...C.map(x => ({...x, g:'c'}))
];

const CATS = [
  {k:'inst',   icon:'🏛️', label:'Instytucje i urzędnicy'},
  {k:'party',  icon:'🎗️', label:'Partie i grupy polityczne'},
  {k:'law',    icon:'⚖️', label:'Prawo, przestępstwa i kary'},
  {k:'system', icon:'🗳️', label:'Wybory i ustrój'}
];

const GAPS = [
  {s:'The general ___ will be held in June.', a:'election', pl:'Wybory parlamentarne odbędą się w czerwcu.'},
  {s:'The ___ lives at 10 Downing Street and leads the government.', a:'prime minister', pl:'Premier mieszka przy Downing Street 10 i kieruje rządem.'},
  {s:'Every ___ elects one MP to the House of Commons.', a:'constituency', pl:'Każdy okręg wyborczy wybiera jednego posła do Izby Gmin.'},
  {s:'Before the election, each party published a ___ full of promises.', a:'manifesto', pl:'Przed wyborami każda partia opublikowała manifest pełen obietnic.'},
  {s:'In 2016, British voters took part in a ___ on leaving the EU.', a:'referendum', pl:'W 2016 roku Brytyjczycy wzięli udział w referendum w sprawie wyjścia z UE.'},
  {s:'No party won a majority, so the two biggest parties worked together in ___.', a:'the coalition', pl:'Żadna partia nie zdobyła większości, więc dwie największe współpracowały w koalicji.'},
  {s:'During the debate, ___ strongly criticised the new policy.', a:'the Opposition', pl:'Podczas debaty opozycja ostro skrytykowała nową politykę.'},
  {s:'In Germany, the head of government is called the ___.', a:'chancellor', pl:'W Niemczech szef rządu nazywa się kanclerz.'},
  {s:'He was ___ with theft after the police found the stolen goods.', a:'charged', pl:'Został oskarżony o kradzież, gdy policja znalazła skradzione rzeczy.'},
  {s:'The shop manager called the police because a ___ had stolen three phones.', a:'shoplifter', pl:'Kierownik sklepu wezwał policję, bo złodziej sklepowy ukradł trzy telefony.'},
  {s:'Instead of going to prison, the teenager did 100 hours of ___.', a:'community service', pl:'Zamiast do więzienia nastolatek trafił na 100 godzin prac społecznych.'},
  {s:'The driver had to pay a ___ of £100 for parking illegally.', a:'fine', pl:'Kierowca musiał zapłacić 100 funtów grzywny za nielegalne parkowanie.'},
  {s:'Britain is a ___ because the king is the head of state.', a:'monarchy', pl:'Wielka Brytania jest monarchią, bo królem jest głowa państwa.'},
  {s:'The USA is a ___ and its Congress includes the Senate.', a:'republic', pl:'USA to republika, a jej Kongres obejmuje Senat.'},
  {s:'The ___ is the set of basic laws that say how a country is governed.', a:'constitution', pl:'Konstytucja to zbiór podstawowych praw określających, jak rządzi się krajem.'},
  {s:'Voter ___ was low: fewer than half of the electorate went to vote.', a:'attendance', pl:'Frekwencja była niska: do głosowania poszło mniej niż pół elektoratu.'}
];
const DISTR = ['strike','crisis','legal high','designer drugs','civil servant','Senate'];

const VERBS = ['allow','break','commit','debate','enter','form','hold','inform','pass','protest','punish','result in','serve','stand'];
const VERB_ITEMS = [
  {s:'The government will ___ a general election in May.', a:'hold', pl:'Rząd przeprowadzi wybory powszechne w maju.'},
  {s:'Parliament voted to ___ a new law on online safety.', a:'pass', pl:'Parlament zagłosował za uchwaleniem nowego prawa o bezpieczeństwie w sieci.'},
  {s:'A US president can ___ only two terms.', a:'serve', pl:'Prezydent USA może pełnić tylko dwie kadencje.'},
  {s:'She decided to ___ for election in her home town.', a:'stand', pl:'Postanowiła kandydować w wyborach w swoim rodzinnym mieście.'},
  {s:'After the election, two parties had to ___ a government together.', a:'form', pl:'Po wyborach dwie partie musiały wspólnie utworzyć rząd.'},
  {s:'The new law could ___ higher prices for everyone.', a:'result in', pl:'Nowe prawo może doprowadzić do wyższych cen dla wszystkich.'},
  {s:'MPs will ___ the new bill for two days before voting on it.', a:'debate', pl:'Posłowie będą debatować nad nową ustawą przez dwa dni, zanim nad nią zagłosują.'},
  {s:'Anyone who tries to ___ a crime will be arrested.', a:'commit', pl:'Każdy, kto spróbuje popełnić przestępstwo, zostanie aresztowany.'},
  {s:'Please ___ us immediately if you cannot attend the meeting.', a:'inform', pl:'Prosimy o natychmiastowe poinformowanie nas, jeśli nie możesz być na spotkaniu.'},
  {s:'Thousands of workers took to the streets to ___ against low pay.', a:'protest', pl:'Tysiące pracowników wyszło na ulice, by protestować przeciwko niskim płacom.'},
  {s:'The law does not ___ people under 18 to vote.', a:'allow', pl:'Prawo nie pozwala osobom poniżej 18 lat głosować.'},
  {s:'Courts can ___ people who break the law.', a:'punish', pl:'Sądy mogą karać ludzi, którzy łamią prawo.'},
  {s:'Visitors must not ___ the building without permission.', a:'enter', pl:'Odwiedzający nie mogą wchodzić do budynku bez zezwolenia.'},
  {s:'Students who ___ the rules may be sent home.', a:'break', pl:'Uczniowie, którzy łamią zasady, mogą zostać odesłani do domu.'}
];

/* ============================================================
   NARZĘDZIA
   ============================================================ */
const $ = (s, r = document) => r.querySelector(s);
const stage = document.getElementById('stage');

function h(tag, props, ...kids) {
  const e = document.createElement(tag);
  for (const [k, v] of Object.entries(props || {})) {
    if (v === false || v == null) continue;
    if (k === 'class') e.className = v;
    else if (k.startsWith('on') && typeof v === 'function') e.addEventListener(k.slice(2), v);
    else e.setAttribute(k, v);
  }
  for (const kid of kids.flat()) {
    if (kid == null || kid === false) continue;
    e.append(kid.nodeType ? kid : document.createTextNode(String(kid)));
  }
  return e;
}
const shuffle = a => { a = [...a]; for (let i = a.length - 1; i > 0; i--) { const j = Math.floor(Math.random() * (i + 1)); [a[i], a[j]] = [a[j], a[i]]; } return a; };
const sample = (a, n) => shuffle(a).slice(0, n);
const norm = s => String(s).toLowerCase().replace(/\(.*?\)/g, '').replace(/[.,!?'’"„”]/g, '').replace(/\s+/g, ' ').trim().replace(/^(the|to|a|an)\s+/, '');
const fmt = n => Number(n.toFixed(1));

function pickSet(n, pool = V) {
  const out = [];
  for (const it of shuffle(pool)) {
    if (out.length >= n) break;
    if (out.some(o => (o.conflict && o.conflict === it.en) || (it.conflict && it.conflict === o.en))) continue;
    out.push(it);
  }
  return out;
}
function speak(t) {
  try {
    const u = new SpeechSynthesisUtterance(t.replace(/\(.*?\)/g, ''));
    u.lang = 'en-GB'; u.rate = .9;
    speechSynthesis.cancel(); speechSynthesis.speak(u);
  } catch (e) {}
}
const speakBtn = text => h('button', {class:'icon-btn', title:'Posłuchaj wymowy', 'aria-label':'Posłuchaj wymowy', onclick: e => { e.stopPropagation(); speak(text); }}, '🔊');
const pbar = (cur, total) => h('div', {class:'bar'}, h('i', {style:`width:${total ? cur / total * 100 : 0}%`}));
const topline = (l, r) => h('div', {class:'topline'}, h('span', {}, l), h('span', {}, r));

/* pamięć postępów */
const KEY = 'vocab-politics-v1';
let store = {};
try { store = JSON.parse(localStorage.getItem(KEY)) || {}; } catch (e) { store = {}; }
const best = id => store[id] || 0;
function saveBest(id, pct) {
  if (pct > best(id)) { store[id] = pct; try { localStorage.setItem(KEY, JSON.stringify(store)); } catch (e) {} }
  refreshTabs();
  return best(id);
}

/* klawiatura */
let currentKey = null;
document.addEventListener('keydown', e => {
  if (!currentKey || e.ctrlKey || e.metaKey || e.altKey) return;
  const t = e.target;
  if (t && t.matches && t.matches('input,select,textarea')) return;
  if (t && t.closest && t.closest('button') && (e.key === 'Enter' || e.key === ' ')) return;
  currentKey(e);
});

/* konfetti */
function confetti() {
  if (matchMedia('(prefers-reduced-motion: reduce)').matches) return;
  const c = $('#confetti'), ctx = c.getContext('2d');
  c.width = innerWidth; c.height = innerHeight;
  const cols = ['#6366f1', '#14b8a6', '#f59e0b', '#ef4444', '#22c55e', '#ec4899'];
  const ps = Array.from({length: 130}, () => ({
    x: Math.random() * c.width, y: -20 - Math.random() * c.height * .5,
    vx: (Math.random() - .5) * 4, vy: 2 + Math.random() * 4, s: 6 + Math.random() * 8,
    r: Math.random() * 6, vr: (Math.random() - .5) * .3, col: cols[Math.floor(Math.random() * cols.length)]
  }));
  let f = 0;
  (function tick() {
    ctx.clearRect(0, 0, c.width, c.height);
    ps.forEach(p => {
      p.x += p.vx; p.y += p.vy; p.r += p.vr;
      ctx.save(); ctx.translate(p.x, p.y); ctx.rotate(p.r);
      ctx.fillStyle = p.col; ctx.fillRect(-p.s / 2, -p.s / 2, p.s, p.s * .6); ctx.restore();
    });
    if (++f < 230) requestAnimationFrame(tick); else ctx.clearRect(0, 0, c.width, c.height);
  })();
}

/* wynik końcowy */
function showResult(id, pct, text) {
  currentKey = null;
  const b = saveBest(id, pct);
  const i = EX.findIndex(e => e.id === id), nx = EX[(i + 1) % EX.length];
  const msg = pct === 100 ? 'Perfekcyjnie! Bez jednej pomyłki.'
    : pct >= 80 ? 'Świetna robota! Jesteś bardzo blisko ideału.'
    : pct >= 50 ? 'Nieźle! Jeszcze jedna runda i będzie świetnie.'
    : 'Spokojnie — powtórz fiszki i spróbuj ponownie.';
  stage.replaceChildren(h('div', {class:'result'},
    h('div', {class:'trophy'}, pct === 100 ? '🏆' : pct >= 80 ? '🎉' : pct >= 50 ? '👍' : '💪'),
    h('h2', {}, 'Wynik: ' + pct + '%'),
    h('p', {class:'score'}, text),
    h('p', {}, msg),
    h('p', {class:'muted'}, 'Twój rekord: ' + b + '%'),
    h('div', {class:'row center'},
      h('button', {class:'btn primary', onclick: () => openEx(id)}, '↻ Jeszcze raz'),
      h('button', {class:'btn', onclick: () => openEx(nx.id)}, 'Dalej: ' + nx.icon + ' ' + nx.name + ' →'))));
  if (pct >= 80) confetti();
}
const exOf = id => EX.find(e => e.id === id);
const head = (id, text) => { const e = exOf(id); return h('div', {class:'ex-head'}, h('h2', {}, e.icon + ' ' + e.name), h('p', {class:'muted'}, text)); };

/* ============================================================
   1. FISZKI (nauka)
   ============================================================ */
function runCards() {
  let group = 'all', dir = 'en', only = false, deck = [], idx = 0, flipped = false;
  const known = new Set(), unknown = new Set();
  const area = h('div');
  const gsel = h('select', {class:'sel', 'aria-label':'Grupa słówek'},
    h('option', {value:'all'}, 'Wszystkie (' + V.length + ')'),
    Object.entries(GROUPS).map(([k, l]) => h('option', {value:k}, `${l} (${V.filter(v => v.g === k).length})`)));
  gsel.addEventListener('change', () => { group = gsel.value; gsel.blur(); build(); });
  const dirLabel = () => dir === 'en' ? '🇬🇧 → 🇵🇱 pokazuj angielski' : '🇵🇱 → 🇬🇧 pokazuj polski';
  const dbtn = h('button', {class:'btn', onclick: () => { dir = dir === 'en' ? 'pl' : 'en'; dbtn.textContent = dirLabel(); flipped = false; draw(); }}, dirLabel());
  const chk = h('input', {type:'checkbox'});
  chk.addEventListener('change', () => { only = chk.checked; chk.blur(); build(); });
  const controls = h('div', {class:'controls'}, gsel, dbtn,
    h('button', {class:'btn', onclick: () => build()}, '🔀 Tasuj'),
    h('label', {}, chk, 'tylko do powtórki'));

  function build() {
    let pool = V.filter(v => group === 'all' || v.g === group);
    if (only) pool = pool.filter(v => unknown.has(v));
    deck = shuffle(pool); idx = 0; flipped = false; draw();
  }
  function mark(isKnown) {
    const it = deck[idx];
    if (isKnown) { known.add(it); unknown.delete(it); } else { unknown.add(it); known.delete(it); }
    idx++; flipped = false; draw();
  }
  function draw() {
    if (!deck.length) {
      currentKey = null;
      area.replaceChildren(h('p', {class:'muted center'}, 'Brak kart do wyświetlenia — zmień grupę albo odznacz „tylko do powtórki”.'));
      return;
    }
    if (idx >= deck.length) {
      currentKey = null;
      const k = deck.filter(x => known.has(x)).length, u = deck.filter(x => unknown.has(x)).length;
      area.replaceChildren(h('div', {class:'result'},
        h('div', {class:'trophy'}, '🎓'), h('h2', {}, 'Koniec talii!'),
        h('p', {class:'score'}, `Znasz: ${k} · Do powtórki: ${u}`),
        h('div', {class:'row center'},
          u ? h('button', {class:'btn primary', onclick: () => { chk.checked = true; only = true; build(); }}, `Powtórz trudne (${u})`) : null,
          h('button', {class:'btn', onclick: () => { chk.checked = false; only = false; build(); }}, 'Od nowa'))));
      if (!u) confetti();
      return;
    }
    const it = deck[idx];
    const front = dir === 'en' ? it.en : it.pl, back = dir === 'en' ? it.pl : it.en;
    const card = h('div', {class:'flash' + (flipped ? ' flipped' : ''), tabindex:'0', role:'button', 'aria-label':'Odwróć kartę'},
      h('div', {class:'flash-inner'},
        h('div', {class:'face front'}, h('div', {class:'tag'}, GROUPS[it.g]), h('div', {class:'ft'}, front), h('div', {class:'tap'}, 'kliknij, aby odwrócić')),
        h('div', {class:'face back'}, h('div', {class:'ft'}, back), it.ex ? h('div', {class:'ex'}, 'np. ' + it.ex) : null)));
    const flip = () => { flipped = !flipped; card.classList.toggle('flipped', flipped); };
    card.addEventListener('click', flip);
    card.addEventListener('keydown', e => { if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); e.stopPropagation(); flip(); } });
    const k = deck.filter(x => known.has(x)).length, u = deck.filter(x => unknown.has(x)).length;
    area.replaceChildren(
      topline(`Karta ${idx + 1} / ${deck.length}`, `Znam: ${k} · Do powtórki: ${u}`),
      pbar(idx, deck.length), card,
      h('div', {class:'actions'},
        h('button', {class:'btn', onclick: () => mark(false)}, '← Jeszcze nie'),
        speakBtn(it.en),
        h('button', {class:'btn primary', onclick: () => mark(true)}, 'Znam →')),
      h('p', {class:'muted center', style:'font-size:.82rem;margin-top:14px'}, 'Klawiatura: Spacja = odwróć · ← jeszcze nie · → znam'));
    currentKey = e => {
      if (e.key === ' ' || e.key === 'Enter') { e.preventDefault(); flip(); }
      else if (e.key === 'ArrowRight') mark(true);
      else if (e.key === 'ArrowLeft') mark(false);
    };
  }
  stage.replaceChildren(head('cards', 'Naucz się słówek przed ćwiczeniami. Odwracaj karty i oceń, czy już je znasz.'), controls, area);
  build();
}

/* ============================================================
   2–3. QUIZ (wielokrotny wybór)
   ============================================================ */
function runQuiz(dir) {
  const id = dir === 'en2pl' ? 'q_en' : 'q_pl';
  const items = pickSet(10);
  let i = 0, score = 0, done = false;
  function draw() {
    done = false;
    const it = items[i];
    const prompt = dir === 'en2pl' ? it.en : it.pl;
    const pool = V.filter(v => v !== it && v.en !== it.conflict && v.conflict !== it.en && (dir === 'en2pl' ? v.pl !== it.pl : v.en !== it.en));
    const opts = shuffle([it, ...pickSet(3, pool)]);
    const fb = h('div', {class:'feedback'});
    const nextBtn = h('button', {class:'btn primary hidden', onclick: () => { i++; i >= items.length ? showResult(id, Math.round(score / items.length * 100), `${score} / ${items.length} poprawnych`) : draw(); }},
      i === items.length - 1 ? 'Zobacz wynik →' : 'Dalej →');
    const btns = opts.map((o, k) => {
      const b = h('button', {class:'opt', onclick: () => pick(b, o)}, h('kbd', {}, k + 1), h('span', {}, dir === 'en2pl' ? o.pl : o.en));
      return b;
    });
    function pick(b, o) {
      if (done) return; done = true;
      const ok = o === it; if (ok) score++;
      btns.forEach((x, k) => { x.disabled = true; if (opts[k] === it) x.classList.add('correct'); });
      if (!ok) b.classList.add('wrong', 'shake');
      fb.className = 'feedback ' + (ok ? 'ok' : 'bad');
      fb.textContent = ok ? '✓ Dobrze!' : `✗ Poprawnie: ${it.en} = ${it.pl}`;
      nextBtn.classList.remove('hidden');
    }
    stage.replaceChildren(
      head(id, dir === 'en2pl' ? 'Wybierz poprawne polskie tłumaczenie. Klawisze 1–4 wybierają odpowiedź, Enter = dalej.' : 'Wybierz poprawne angielskie słowo. Klawisze 1–4 wybierają odpowiedź, Enter = dalej.'),
      topline(`Pytanie ${i + 1} / ${items.length}`, `Punkty: ${score}`), pbar(i, items.length),
      h('div', {class:'prompt'}, h('div', {class:'big'}, prompt), dir === 'en2pl' ? speakBtn(it.en) : null),
      h('div', {class:'opts'}, btns), fb, h('div', {class:'row'}, nextBtn));
    currentKey = e => {
      if (/^[1-4]$/.test(e.key) && !done) btns[Number(e.key) - 1].click();
      else if ((e.key === 'Enter' || e.key === ' ') && done) { e.preventDefault(); nextBtn.click(); }
    };
  }
  draw();
}

/* ============================================================
   4. WPISZ SŁOWO
   ============================================================ */
function runType() {
  const items = pickSet(10);
  let i = 0, score = 0;
  function draw() {
    const it = items[i], acc = new Set([it.en, ...(it.ans || [])].map(norm));
    const base = it.en.replace(/\(.*?\)/g, '').trim();
    let done = false, attempts = 0, hints = 0;
    const input = h('input', {type:'text', class:'txt', placeholder:'Wpisz angielskie słowo lub zwrot…', autocomplete:'off', autocapitalize:'off', spellcheck:'false', 'aria-label':'Twoja odpowiedź'});
    const hintLine = h('div', {class:'hintline'});
    const fb = h('div', {class:'feedback'});
    const checkBtn = h('button', {class:'btn primary', onclick: check}, 'Sprawdź ✓');
    const hintBtn = h('button', {class:'btn', onclick: hint}, '💡 Podpowiedź (−½ pkt)');
    const nextBtn = h('button', {class:'btn primary hidden', onclick: () => { i++; i >= items.length ? showResult('type', Math.round(score / items.length * 100), `${fmt(score)} / ${items.length} pkt`) : draw(); }},
      i === items.length - 1 ? 'Zobacz wynik →' : 'Dalej →');
    input.addEventListener('keydown', e => { if (e.key === 'Enter') { e.preventDefault(); e.stopPropagation(); check(); } });
    function hint() {
      if (done) return;
      hints++;
      hintLine.textContent = base.split('').map((ch, k) => ch === ' ' ? '\u00A0\u00A0' : (k < hints ? ch : '_')).join(' ');
      input.focus();
    }
    function end(ok, msg) {
      done = true; input.disabled = true; checkBtn.classList.add('hidden'); hintBtn.classList.add('hidden');
      input.classList.add(ok ? 'ok' : 'bad');
      fb.className = 'feedback ' + (ok ? 'ok' : 'bad'); fb.textContent = msg;
      nextBtn.classList.remove('hidden');
    }
    function check() {
      if (done) return;
      const v = norm(input.value);
      if (!v) { input.classList.add('shake'); setTimeout(() => input.classList.remove('shake'), 380); input.focus(); return; }
      attempts++;
      if (acc.has(v)) {
        const p = (attempts === 1 && hints === 0) ? 1 : .5;
        score += p;
        end(true, p === 1 ? '✓ Świetnie! +1 pkt' : '✓ Dobrze! +½ pkt (podpowiedź lub druga próba)');
      } else if (attempts >= 2) {
        end(false, `✗ Poprawna odpowiedź: ${it.en}`);
      } else {
        fb.className = 'feedback bad'; fb.textContent = '✗ To nie to — spróbuj jeszcze raz (ostatnia próba).';
        input.classList.add('shake'); setTimeout(() => input.classList.remove('shake'), 380); input.select();
      }
    }
    stage.replaceChildren(
      head('type', 'Przetłumacz na angielski. Enter sprawdza odpowiedź. Masz dwie próby i możesz użyć podpowiedzi.'),
      topline(`Pytanie ${i + 1} / ${items.length}`, `Punkty: ${fmt(score)}`), pbar(i, items.length),
      h('div', {class:'prompt'}, h('div', {class:'big'}, it.pl), h('div', {class:'muted'}, 'Jak to powiedzieć po angielsku?')),
      input, hintLine, fb,
      h('div', {class:'row'}, checkBtn, hintBtn, nextBtn));
    currentKey = e => { if (done && (e.key === 'Enter' || e.key === ' ')) { e.preventDefault(); nextBtn.click(); } };
    input.focus();
  }
  draw();
}

/* ============================================================
   5. DOPASUJ PARY
   ============================================================ */
function runPairs() {
  const items = pickSet(8);
  const left = shuffle(items), right = shuffle(items);
  let sL = null, sR = null, matched = 0, errors = 0;
  const faulty = new Set(), lb = new Map(), rb = new Map();
  const status = h('div', {class:'topline'});
  const bar = pbar(0, items.length);
  function upd() {
    status.replaceChildren(h('span', {}, `Dopasowano: ${matched} / ${items.length}`), h('span', {}, `Pomyłki: ${errors}`));
    bar.firstChild.style.width = (matched / items.length * 100) + '%';
  }
  function choose(side, it, btn) {
    if (btn.classList.contains('matched')) return;
    if (side === 'L') { if (sL) lb.get(sL).classList.remove('sel'); sL = (sL === it) ? null : it; if (sL) btn.classList.add('sel'); }
    else { if (sR) rb.get(sR).classList.remove('sel'); sR = (sR === it) ? null : it; if (sR) btn.classList.add('sel'); }
    if (sL && sR) evaluate();
  }
  function evaluate() {
    const a = sL, b = sR; sL = sR = null;
    const A = lb.get(a), B = rb.get(b);
    if (a === b) {
      [A, B].forEach(x => { x.classList.remove('sel'); x.classList.add('matched'); x.disabled = true; });
      matched++; upd();
      if (matched === items.length) setTimeout(() => { const ok = items.length - faulty.size; showResult('pairs', Math.round(ok / items.length * 100), `${ok} / ${items.length} par bez pomyłki`); }, 900);
    } else {
      errors++; faulty.add(a); upd();
      [A, B].forEach(x => x.classList.add('wrong', 'shake'));
      setTimeout(() => [A, B].forEach(x => x.classList.remove('wrong', 'shake', 'sel')), 450);
    }
  }
  const lcol = h('div', {}, left.map(it => { const b = h('button', {class:'pbtn', onclick: () => choose('L', it, b)}, it.en); lb.set(it, b); return b; }));
  const rcol = h('div', {}, right.map(it => { const b = h('button', {class:'pbtn', onclick: () => choose('R', it, b)}, it.pl); rb.set(it, b); return b; }));
  stage.replaceChildren(
    head('pairs', 'Kliknij angielskie słowo po lewej, a potem jego polskie tłumaczenie po prawej.'),
    status, bar, h('div', {class:'pairs'}, lcol, rcol));
  upd(); currentKey = null;
}

/* ============================================================
   6–7. UZUPEŁNIJ ZDANIA / CZASOWNIKI (luki z listą)
   ============================================================ */
function runGaps(id, items, options, intro) {
  let checked = false, final = 0;
  const selects = [], rows = [];
  const chips = options.map(o => h('span', {class:'chip'}, o));
  function updateBank() {
    const used = new Set(selects.map(s => s.value));
    chips.forEach((c, k) => c.classList.toggle('used', used.has(options[k])));
  }
  items.forEach((it, k) => {
    const parts = it.s.split('___');
    const sel = h('select', {class:'gap', 'aria-label':`Luka ${k + 1}`},
      h('option', {value:''}, '— wybierz —'), options.map(o => h('option', {value:o}, o)));
    sel.addEventListener('change', updateBank);
    selects.push(sel);
    const ans = h('div', {class:'ans hidden'});
    const row = h('div', {class:'sent'}, h('span', {class:'num'}, (k + 1) + '.'), parts[0], sel, parts[1] || '', h('div', {class:'pl'}, it.pl), ans);
    rows.push({row, ans});
  });
  const msg = h('div', {class:'feedback'});
  const btn = h('button', {class:'btn primary', onclick: check}, 'Sprawdź odpowiedzi ✓');
  function check() {
    if (checked) { showResult(id, Math.round(final / items.length * 100), `${final} / ${items.length} poprawnych luk`); return; }
    if (selects.some(s => !s.value)) { msg.className = 'feedback bad'; msg.textContent = 'Uzupełnij wszystkie luki, zanim sprawdzisz 🙂'; return; }
    checked = true; final = 0;
    items.forEach((it, k) => {
      const s = selects[k], ok = s.value === it.a;
      s.disabled = true; s.classList.add(ok ? 'correct' : 'wrong');
      if (ok) final++; else { rows[k].ans.classList.remove('hidden'); rows[k].ans.textContent = '✗ Poprawna odpowiedź: ' + it.a; }
    });
    msg.className = 'feedback ' + (final === items.length ? 'ok' : 'bad');
    msg.textContent = `Wynik: ${final} / ${items.length}`;
    btn.textContent = 'Zobacz wynik →';
  }
  stage.replaceChildren(head(id, intro), h('div', {class:'bank'}, chips), rows.map(r => r.row), msg, h('div', {class:'row'}, btn));
  currentKey = null;
}
function runSentences() {
  const items = sample(GAPS, 8);
  const opts = [...items.map(x => x.a), ...sample(DISTR, 3)].sort((a, b) => a.localeCompare(b, 'en', {sensitivity:'base'}));
  runGaps('gaps', items, opts, 'Wybierz z listy słowo pasujące do luki. W banku są też 3 słowa „na zmyłkę”. Każde pasuje tylko raz.');
}
function runVerbs() {
  runGaps('verbs', sample(VERB_ITEMS, 10), VERBS, 'Dobierz właściwy czasownik (kolokacje z sekcji Vocabulary Challenge i nie tylko). Polskie tłumaczenie pod zdaniem to podpowiedź.');
}

/* ============================================================
   8. PRAWDA / FAŁSZ
   ============================================================ */
function runTF() {
  const N = 12, items = pickSet(N);
  const truths = shuffle([...Array(N / 2).fill(true), ...Array(N / 2).fill(false)]);
  const qs = items.map((it, k) => {
    let shown = it.pl;
    if (!truths[k]) shown = sample(V.filter(v => v !== it && v.pl !== it.pl && v.en !== it.conflict && v.conflict !== it.en), 1)[0].pl;
    return {it, truth: truths[k], shown};
  });
  let i = 0, score = 0, streak = 0, done = false;
  function draw() {
    done = false;
    const q = qs[i];
    const fb = h('div', {class:'feedback'});
    const nextBtn = h('button', {class:'btn primary hidden', onclick: () => { i++; i >= N ? showResult('tf', Math.round(score / N * 100), `${score} / ${N} poprawnych`) : draw(); }},
      i === N - 1 ? 'Zobacz wynik →' : 'Dalej →');
    const bT = h('button', {class:'btn', onclick: () => answer(true)}, '✓ Prawda (T)');
    const bF = h('button', {class:'btn', onclick: () => answer(false)}, '✗ Fałsz (F)');
    function answer(val) {
      if (done) return; done = true;
      const ok = val === q.truth;
      if (ok) { score++; streak++; } else streak = 0;
      bT.disabled = bF.disabled = true;
      const chosen = val ? bT : bF;
      chosen.classList.add(ok ? 'correct' : 'wrong'); if (!ok) chosen.classList.add('shake');
      fb.className = 'feedback ' + (ok ? 'ok' : 'bad');
      fb.textContent = ok
        ? (q.truth ? '✓ Zgadza się!' : `✓ Dobrze! „${q.it.en}” to „${q.it.pl}”.`) + (streak >= 3 ? ` 🔥 Seria: ${streak}` : '')
        : (q.truth ? `✗ Tu akurat było dobrze: „${q.it.en}” = „${q.it.pl}”.` : `✗ „${q.it.en}” to „${q.it.pl}”, a nie „${q.shown}”.`);
      nextBtn.classList.remove('hidden');
    }
    stage.replaceChildren(
      head('tf', 'Czy to tłumaczenie jest poprawne? Skróty: T = prawda, F = fałsz, Enter = dalej.'),
      topline(`Pytanie ${i + 1} / ${N}`, `Punkty: ${score}` + (streak >= 2 ? ` · 🔥 ${streak}` : '')), pbar(i, N),
      h('div', {class:'tf-card'}, h('div', {class:'big'}, q.it.en), h('div', {class:'tf-eq'}, '='), h('div', {class:'big'}, q.shown)),
      h('div', {class:'tf-btns'}, bT, bF), fb, h('div', {class:'row'}, nextBtn));
    currentKey = e => {
      const k = e.key.toLowerCase();
      if (!done && (k === 't' || k === 'arrowleft')) bT.click();
      else if (!done && (k === 'f' || k === 'arrowright')) bF.click();
      else if (done && (k === 'enter' || k === ' ')) { e.preventDefault(); nextBtn.click(); }
    };
  }
  draw();
}

/* ============================================================
   9. ROZSYPANKA
   ============================================================ */
function runScramble() {
  const pool = V.filter(v => /^[A-Za-z]{4,13}$/.test(v.en));
  const items = pickSet(8, pool);
  let i = 0, score = 0;
  function draw() {
    const it = items[i], word = it.en.toLowerCase();
    let sc; do { sc = shuffle(word.split('')); } while (sc.join('') === word);
    const tiles = sc.map((ch, id) => ({ch, id, used:false}));
    let ans = [], penalty = false, over = false;
    const slots = h('div', {class:'slots'}), tilesEl = h('div', {class:'tiles'});
    const fb = h('div', {class:'feedback'});
    const nextBtn = h('button', {class:'btn primary hidden', onclick: next}, i === items.length - 1 ? 'Zobacz wynik →' : 'Dalej →');
    const checkBtn = h('button', {class:'btn primary', onclick: check}, 'Sprawdź ✓');
    const hintBtn = h('button', {class:'btn', onclick: hint}, '💡 Podpowiedź (−½ pkt)');
    const clearBtn = h('button', {class:'btn', onclick: clearAll}, '⌫ Wyczyść');
    const giveBtn = h('button', {class:'btn', onclick: giveUp}, 'Poddaję się');
    function refresh() {
      if (!ans.length) slots.replaceChildren(h('span', {class:'muted'}, 'Klikaj litery poniżej albo pisz na klawiaturze…'));
      else slots.replaceChildren(...ans.map(id => h('button', {class:'tile', onclick: () => { if (over) return; ans = ans.filter(x => x !== id); tiles[id].used = false; refresh(); }}, tiles[id].ch)));
      tilesEl.replaceChildren(...tiles.map(t => h('button', {class:'tile' + (t.used ? ' used' : ''), onclick: () => add(t.id)}, t.ch)));
    }
    function add(id) { if (over || tiles[id].used) return; tiles[id].used = true; ans.push(id); refresh(); }
    function clearAll() { if (over) return; ans = []; tiles.forEach(t => t.used = false); refresh(); }
    function lockUI(ok) {
      over = true;
      [checkBtn, hintBtn, clearBtn, giveBtn].forEach(b => b.classList.add('hidden'));
      nextBtn.classList.remove('hidden');
      if (ok) slots.classList.add('ok');
    }
    function check() {
      if (over) return;
      if (ans.length < word.length) { fb.className = 'feedback bad'; fb.textContent = 'Użyj wszystkich liter.'; return; }
      const w = ans.map(id => tiles[id].ch).join('');
      if (w === word) {
        const p = penalty ? .5 : 1; score += p;
        fb.className = 'feedback ok'; fb.textContent = p === 1 ? '✓ Brawo! +1 pkt' : '✓ Dobrze! +½ pkt'; lockUI(true);
      } else {
        penalty = true; fb.className = 'feedback bad'; fb.textContent = '✗ Jeszcze nie — spróbuj ponownie.';
        slots.classList.add('shake'); setTimeout(() => slots.classList.remove('shake'), 380);
      }
    }
    function hint() {
      if (over) return; penalty = true;
      let k = 0; while (k < ans.length && tiles[ans[k]].ch === word[k]) k++;
      ans.slice(k).forEach(id => tiles[id].used = false); ans = ans.slice(0, k);
      if (k < word.length) { const t = tiles.find(t => !t.used && t.ch === word[k]); if (t) { t.used = true; ans.push(t.id); } }
      refresh();
    }
    function giveUp() {
      if (over) return;
      tiles.forEach(t => t.used = false); ans = [];
      word.split('').forEach(ch => { const t = tiles.find(t => !t.used && t.ch === ch); t.used = true; ans.push(t.id); });
      refresh(); fb.className = 'feedback bad'; fb.textContent = `Poprawnie: ${it.en}`; lockUI(false);
    }
    function next() { i++; i >= items.length ? showResult('scramble', Math.round(score / items.length * 100), `${fmt(score)} / ${items.length} pkt`) : draw(); }
    stage.replaceChildren(
      head('scramble', 'Ułóż angielskie słowo z rozsypanych liter. Możesz pisać na klawiaturze (Backspace kasuje, Enter sprawdza).'),
      topline(`Słowo ${i + 1} / ${items.length}`, `Punkty: ${fmt(score)}`), pbar(i, items.length),
      h('div', {class:'prompt'}, h('div', {class:'big'}, it.pl), h('div', {class:'muted'}, `${word.length} liter`)),
      slots, tilesEl, fb, h('div', {class:'row center'}, checkBtn, hintBtn, clearBtn, giveBtn, nextBtn));
    refresh();
    currentKey = e => {
      const k = e.key;
      if (k === 'Enter' || k === ' ') { e.preventDefault(); over ? next() : (k === 'Enter' && check()); }
      else if (over) return;
      else if (k === 'Backspace') { e.preventDefault(); if (ans.length) { const id = ans.pop(); tiles[id].used = false; refresh(); } }
      else if (/^[a-zA-Z]$/.test(k)) { const t = tiles.find(t => !t.used && t.ch === k.toLowerCase()); if (t) add(t.id); }
    };
  }
  draw();
}

/* ============================================================
   10. SORTOWANIE DO KATEGORII
   ============================================================ */
function runSort() {
  const items = CATS.flatMap(c => sample(V.filter(v => v.c === c.k), 3)).map((v, id) => ({...v, id}));
  const order = shuffle(items);
  const place = {}; items.forEach(it => place[it.id] = null);
  let selId = null, checked = false, score = 0;
  const catLabel = k => { const c = CATS.find(c => c.k === k); return c.icon + ' ' + c.label; };
  const poolEl = h('div', {class:'pool'});
  const info = h('div', {class:'topline'});
  const fb = h('div', {class:'feedback'});
  const btn = h('button', {class:'btn primary', onclick: check, disabled:'true'}, 'Sprawdź ✓');
  function setPlace(id, k) { place[id] = k; selId = null; render(); }
  const buckets = CATS.map(c => {
    const body = h('div', {class:'bbody'});
    const el = h('div', {class:'bucket', onclick: () => { if (!checked && selId !== null) setPlace(selId, c.k); }}, h('h4', {}, c.icon + ' ' + c.label), body);
    el.addEventListener('dragover', e => { e.preventDefault(); el.classList.add('over'); });
    el.addEventListener('dragleave', () => el.classList.remove('over'));
    el.addEventListener('drop', e => { e.preventDefault(); el.classList.remove('over'); if (checked) return; const id = Number(e.dataTransfer.getData('text/plain')); if (!isNaN(id)) setPlace(id, c.k); });
    return {c, el, body};
  });
  poolEl.addEventListener('dragover', e => e.preventDefault());
  poolEl.addEventListener('drop', e => { e.preventDefault(); if (checked) return; const id = Number(e.dataTransfer.getData('text/plain')); if (!isNaN(id)) setPlace(id, null); });
  function chip(it) {
    let cls = 'sitem';
    if (checked) cls += place[it.id] === it.c ? ' correct' : ' wrong';
    else if (selId === it.id) cls += ' sel';
    const el = h('div', {class:cls, draggable: checked ? false : 'true', title:'Kliknij lub przeciągnij'},
      h('b', {}, it.en), h('small', {}, it.pl),
      checked && place[it.id] !== it.c ? h('small', {class:'fix'}, '→ ' + catLabel(it.c)) : null);
    el.addEventListener('click', e => {
      e.stopPropagation();
      if (checked) return;
      if (place[it.id] !== null) setPlace(it.id, null);
      else { selId = selId === it.id ? null : it.id; render(); }
    });
    el.addEventListener('dragstart', e => { e.dataTransfer.setData('text/plain', String(it.id)); });
    return el;
  }
  function render() {
    poolEl.replaceChildren(...order.filter(it => place[it.id] === null).map(chip));
    if (!poolEl.children.length) poolEl.replaceChildren(h('span', {class:'muted'}, 'Wszystkie słówka są już w pudełkach ✔'));
    buckets.forEach(b => b.body.replaceChildren(...items.filter(it => place[it.id] === b.c.k).map(chip)));
    const placed = items.filter(it => place[it.id] !== null).length;
    info.replaceChildren(h('span', {}, `Przypisano: ${placed} / ${items.length}`), h('span', {}, selId !== null ? 'Teraz kliknij pudełko 👇' : 'Kliknij słówko lub przeciągnij je'));
    if (!checked) btn.disabled = placed < items.length;
  }
  function check() {
    if (checked) { showResult('sort', Math.round(score / items.length * 100), `${score} / ${items.length} dobrze przypisanych`); return; }
    checked = true; selId = null;
    score = items.filter(it => place[it.id] === it.c).length;
    render();
    fb.className = 'feedback ' + (score === items.length ? 'ok' : 'bad');
    fb.textContent = `Wynik: ${score} / ${items.length}. Czerwone słówka mają podpowiedź z poprawną kategorią.`;
    btn.textContent = 'Zobacz wynik →'; btn.disabled = false;
  }
  stage.replaceChildren(
    head('sort', 'Przypisz każde słówko do właściwej kategorii. Kliknij słówko, potem pudełko (albo przeciągnij). Kliknięcie słówka w pudełku zwraca je na górę.'),
    info, poolEl, h('div', {class:'sortgrid'}, buckets.map(b => b.el)), fb, h('div', {class:'row'}, btn));
  render(); currentKey = null;
}

/* ============================================================
   11. MEMORY
   ============================================================ */
function runMemory() {
  const items = pickSet(8, V.filter(v => v.pl.length <= 30));
  const cards = shuffle(items.flatMap((it, k) => [{k, t:it.en, type:'en'}, {k, t:it.pl, type:'pl'}]));
  let first = null, lock = false, moves = 0, found = 0;
  const status = h('div', {class:'topline'});
  const bar = pbar(0, items.length);
  function upd() {
    status.replaceChildren(h('span', {}, `Znalezione pary: ${found} / ${items.length}`), h('span', {}, `Ruchy: ${moves}`));
    bar.firstChild.style.width = (found / items.length * 100) + '%';
  }
  const els = cards.map((c, idx) => {
    const el = h('button', {class:'mcard ' + c.type, 'aria-label':'Karta'},
      h('div', {class:'minner'}, h('div', {class:'mface mback'}, '?'), h('div', {class:'mface mfront'}, c.t)));
    el.addEventListener('click', () => flip(idx));
    return el;
  });
  function flip(idx) {
    const el = els[idx];
    if (lock || el.classList.contains('up')) return;
    el.classList.add('up');
    if (first === null) { first = idx; return; }
    moves++;
    const a = cards[first], b = cards[idx], fa = first; first = null;
    if (a.k === b.k) {
      [els[fa], el].forEach(x => x.classList.add('done')); found++; upd();
      if (found === items.length) setTimeout(() => {
        const pct = Math.max(10, Math.min(100, Math.round(100 - (moves - 10) * 5)));
        showResult('memory', pct, `${moves} ruchów (minimum to 8)`);
      }, 1000);
    } else {
      lock = true; upd();
      setTimeout(() => { [els[fa], el].forEach(x => x.classList.remove('up')); lock = false; }, 950);
    }
  }
  stage.replaceChildren(
    head('memory', 'Odkrywaj po dwie karty i znajdź pary: angielskie słowo + jego polskie tłumaczenie. Im mniej ruchów, tym lepszy wynik.'),
    status, bar, h('div', {class:'mem'}, els));
  upd(); currentKey = null;
}

/* ============================================================
   REJESTR ĆWICZEŃ, NAWIGACJA, START
   ============================================================ */
const EX = [
  {id:'cards',    icon:'🗂️', name:'Fiszki',            graded:false, run: runCards},
  {id:'q_en',     icon:'🇬🇧', name:'Quiz EN → PL',      graded:true,  run: () => runQuiz('en2pl')},
  {id:'q_pl',     icon:'🇵🇱', name:'Quiz PL → EN',      graded:true,  run: () => runQuiz('pl2en')},
  {id:'type',     icon:'⌨️', name:'Wpisz słowo',       graded:true,  run: runType},
  {id:'pairs',    icon:'🔗', name:'Dopasuj pary',      graded:true,  run: runPairs},
  {id:'gaps',     icon:'✍️', name:'Uzupełnij zdania',  graded:true,  run: runSentences},
  {id:'verbs',    icon:'🧩', name:'Czasowniki',        graded:true,  run: runVerbs},
  {id:'tf',       icon:'⚖️', name:'Prawda / Fałsz',    graded:true,  run: runTF},
  {id:'scramble', icon:'🔤', name:'Rozsypanka',        graded:true,  run: runScramble},
  {id:'sort',     icon:'🗃️', name:'Sortowanie',        graded:true,  run: runSort},
  {id:'memory',   icon:'🃏', name:'Memory',            graded:true,  run: runMemory}
];

function buildTabs() {
  const nav = $('#tabs');
  EX.forEach(e => nav.append(h('button', {class:'tab', 'data-id':e.id, title:e.name, onclick: () => openEx(e.id)},
    h('span', {}, e.icon), h('span', {}, e.name), h('span', {class:'badge'}))));
}
function refreshTabs() {
  const graded = EX.filter(e => e.graded);
  graded.forEach(e => {
    const b = $(`.tab[data-id="${e.id}"] .badge`), v = best(e.id);
    b.textContent = v ? (v >= 80 ? '✔ ' : '') + v + '%' : '';
    b.classList.toggle('gold', v >= 80);
  });
  const avg = Math.round(graded.reduce((s, e) => s + best(e.id), 0) / graded.length);
  $('#mpct').textContent = avg + '%';
  $('#mbar').style.width = avg + '%';
}
function openEx(id) {
  currentKey = null;
  document.querySelectorAll('.tab').forEach(t => t.classList.toggle('active', t.dataset.id === id));
  exOf(id).run();
  const r = stage.getBoundingClientRect();
  if (r.top < 0) window.scrollTo({top: window.scrollY + r.top - 70, behavior:'smooth'});
}

$('#sub').textContent = `${V.length} słówek i zwrotów · fiszki + ${EX.filter(e => e.graded).length} ćwiczeń z automatycznym sprawdzaniem`;
$('#theme').addEventListener('click', () => {
  const cur = document.documentElement.dataset.theme || (matchMedia('(prefers-color-scheme: dark)').matches ? 'dark' : 'light');
  const nx = cur === 'dark' ? 'light' : 'dark';
  document.documentElement.dataset.theme = nx;
  try { localStorage.setItem(KEY + '-theme', nx); } catch (e) {}
});
try { const t = localStorage.getItem(KEY + '-theme'); if (t) document.documentElement.dataset.theme = t; } catch (e) {}
$('#reset').addEventListener('click', () => {
  if (confirm('Na pewno wyzerować wszystkie zapisane wyniki?')) {
    store = {}; try { localStorage.removeItem(KEY); } catch (e) {}
    refreshTabs();
  }
});

buildTabs();
refreshTabs();
openEx('cards');
</script>
</body>
</html>
