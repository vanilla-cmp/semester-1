<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1,viewport-fit=cover">
<meta name="description" content="Vania Beigi, Computer Science (AI) student at the University of Leeds.">
<style>:root{color-scheme:light;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}body{margin:0;font:14px/1.5 system-ui,-apple-system,sans-serif}img{max-width:100%}[hidden]{display:none!important}</style>
</head>
<body>
<title>Vania Beigi</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Unbounded:wght@200;300;400;500&family=Instrument+Sans:wght@400;500;600&family=JetBrains+Mono:wght@400&display=swap">
<style id="css">
/* Layout: a terminal-and-HUD opening with a live network, then wide-set chapters on a narrow reading measure, one burgundy band for the quote. */
:root{
  --ivory:#F6F0E4; --paper:#EEE5D4; --ink:#241719; --muted:#7A6560; --faint:#B9A89F; --line:#DCCDB9;
  --wine:#6B1626; --wine-2:#8C2B3D; --band:#5C1120; --on-band:#F6EEE0;
  --display:"Unbounded","Helvetica Neue",Arial,system-ui,sans-serif;
  --body:"Instrument Sans","Helvetica Neue",Arial,system-ui,sans-serif;
  --mono:"JetBrains Mono",ui-monospace,Menlo,Consolas,monospace;
  --measure:68ch; --wide:1180px;
  --ease:cubic-bezier(.2,.7,.1,1);
}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]){
  --ivory:#140C0E; --paper:#1C1316; --ink:#F1E7D8; --muted:#A8948D; --faint:#6E5C58; --line:#352628;
  --wine:#D07A8A; --wine-2:#E29AA6; --band:#4A0E1A; --on-band:#F3E9DB; color-scheme:dark }}
:root[data-theme="dark"]{
  --ivory:#140C0E; --paper:#1C1316; --ink:#F1E7D8; --muted:#A8948D; --faint:#6E5C58; --line:#352628;
  --wine:#D07A8A; --wine-2:#E29AA6; --band:#4A0E1A; --on-band:#F3E9DB; color-scheme:dark }

html{scroll-behavior:smooth}
body{background:var(--ivory);color:var(--ink);font-family:var(--body);font-size:17px;line-height:1.65;-webkit-font-smoothing:antialiased;text-rendering:optimizeLegibility}
::selection{background:var(--wine);color:var(--ivory)}
a{color:inherit}
.wrap{max-width:var(--wide);margin:0 auto;padding-left:max(24px,env(safe-area-inset-left,0px));padding-right:max(24px,env(safe-area-inset-right,0px))}
@media (max-width:520px){.wrap{padding-left:max(18px,env(safe-area-inset-left,0px));padding-right:max(18px,env(safe-area-inset-right,0px))}}
.grain{position:fixed;inset:0;pointer-events:none;z-index:60;opacity:.07;mix-blend-mode:multiply}
@media (prefers-color-scheme: dark){:root:not([data-theme="light"]) .grain{mix-blend-mode:screen;opacity:.05}}
:root[data-theme="dark"] .grain{mix-blend-mode:screen;opacity:.05}

/* nav */
body::before{content:"";position:fixed;inset:0 0 auto;height:env(safe-area-inset-top,0px);z-index:41;background:var(--ivory)}
.nav{position:sticky;top:env(safe-area-inset-top,0px);z-index:40;background:color-mix(in srgb,var(--ivory) 86%,transparent);backdrop-filter:blur(14px) saturate(1.2);-webkit-backdrop-filter:blur(14px) saturate(1.2);border-bottom:1px solid transparent;transition:border-color .4s}
.nav.scrolled{border-bottom-color:var(--line)}
.nav .wrap{display:flex;align-items:center;justify-content:space-between;gap:24px;height:58px}
.brand{font-family:var(--display);font-size:1rem;font-weight:400;text-decoration:none;letter-spacing:.005em;white-space:nowrap}
.brand i{color:var(--wine);font-weight:300;font-style:normal}
.links{display:flex;gap:26px;overflow-x:auto;scrollbar-width:none;min-width:0}
.links::-webkit-scrollbar{display:none}
.links a{font-size:.86rem;color:var(--muted);text-decoration:none;white-space:nowrap;transition:color .3s;position:relative;padding-block:4px}
.links a:hover,.links a.active{color:var(--ink)}
.links a.active::after{content:"";position:absolute;left:0;right:0;bottom:-2px;height:1px;background:var(--wine)}
@media (max-width:760px){.links{gap:18px}.links a:not(.keep){display:none}}

/* shared */
.label{font-family:var(--mono);font-size:.74rem;letter-spacing:.04em;color:var(--wine);display:flex;align-items:center;gap:10px}
.label::before{content:"";width:22px;height:1px;background:currentColor}
.h2{font-family:var(--display);font-weight:300;font-size:clamp(1.9rem,4.2vw,3.3rem);line-height:1.08;letter-spacing:-.03em;margin:18px 0 0;text-wrap:balance}
.h2 em{font-style:normal;color:var(--wine)}
section{scroll-margin-top:70px}
.chapter{padding-block:clamp(80px,12vw,150px)}
.rule{height:1px;background:var(--line);border:0;margin:0}
.js .rv{transition:transform 1.1s var(--ease),opacity 1.1s var(--ease)}
.js .rv.pre{transform:translateY(22px);opacity:.55}

/* hero */
.hero{position:relative;padding-block:clamp(56px,9vw,110px) clamp(40px,6vw,70px);overflow:hidden}
.sky{position:absolute;inset:0;width:100%;height:100%;pointer-events:none}
.sky .thread{fill:none;stroke:var(--wine);stroke-width:1;opacity:.55;stroke-dasharray:1;stroke-dashoffset:0}
.js .sky .thread{animation:draw 4.2s var(--ease) .3s both}
.sky .star{fill:var(--wine)}
.sky .halo{fill:var(--wine);opacity:.12;transform-box:fill-box;transform-origin:center;animation:twinkle 5s ease-in-out infinite}
@keyframes draw{from{stroke-dashoffset:1}to{stroke-dashoffset:0}}
@keyframes twinkle{0%,100%{transform:scale(1);opacity:.1}50%{transform:scale(1.9);opacity:.2}}
.hero .wrap{position:relative}
.eyebrow{font-family:var(--mono);font-size:.76rem;color:var(--muted);letter-spacing:.03em;max-width:48ch}
.name{font-family:var(--display);font-weight:200;font-size:clamp(3.2rem,12vw,9.6rem);line-height:.92;letter-spacing:-.05em;margin:28px 0 0}
.name .l1{display:block}
.name .l2{display:block;color:var(--wine);font-weight:200;padding-left:clamp(0px,11vw,170px)}
.js .name .l1,.js .name .l2{animation:rise 1.6s var(--ease) both}
.js .name .l2{animation-delay:.18s}
@keyframes rise{from{transform:translateY(.18em);opacity:.2;filter:blur(6px)}to{transform:none;opacity:1;filter:none}}
.tagline{font-family:var(--body);font-size:clamp(1.1rem,1.9vw,1.4rem);line-height:1.45;max-width:32ch;margin:38px 0 0 auto;color:var(--ink);text-wrap:balance}
.credits{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:24px;margin-top:clamp(56px,8vw,96px);padding-top:22px;border-top:1px solid var(--line)}
.credit{min-width:0}
.credit .k{font-family:var(--mono);font-size:.7rem;color:var(--muted);display:block;margin-bottom:6px}
.credit .v{font-family:var(--body);font-size:1.05rem;line-height:1.25;display:block}
@media (max-width:760px){.credits{grid-template-columns:repeat(2,minmax(0,1fr))}.tagline{margin-left:0}}

/* statement */
.statement{padding-block:clamp(90px,14vw,190px)}
.statement p{font-family:var(--display);font-weight:300;font-size:clamp(1.5rem,3.4vw,2.7rem);line-height:1.25;letter-spacing:-.03em;max-width:26ch;margin:0;text-wrap:pretty}
.statement .w{color:var(--faint);transition:color .5s ease}
.statement .w.on{color:var(--ink)}
.statement .sig{margin-top:34px;font-family:var(--mono);font-size:.76rem;color:var(--muted)}

/* about */
.about-grid{display:grid;grid-template-columns:minmax(0,1.25fr) minmax(0,.75fr);gap:clamp(40px,7vw,110px);margin-top:56px;align-items:start}
.prose p{margin:0 0 1.2em;max-width:var(--measure);font-size:1.06rem}
.portrait{margin:0 0 34px;aspect-ratio:4/5;max-width:100%;overflow:hidden;background:var(--paper)}
.portrait img{width:100%;height:100%;object-fit:cover;display:block;filter:sepia(.12) contrast(1.02);transition:transform 1.6s var(--ease)}
.portrait:hover img{transform:scale(1.03)}
.offclock h3{font-family:var(--mono);font-weight:400;font-size:.74rem;color:var(--muted);margin:0 0 14px}
.offclock ul{list-style:none;margin:0;padding:0}
.offclock li{padding:16px 0;border-top:1px solid var(--line);display:grid;gap:2px}
.offclock li:last-child{border-bottom:1px solid var(--line)}
.offline{margin:0;color:var(--muted);font-size:.98rem}
.offline .sep{color:var(--faint);margin:0 .5em}
.offclock span{color:var(--muted);font-size:.95rem}
@media (max-width:860px){.about-grid{grid-template-columns:minmax(0,1fr)}}

/* quote band */
.band{background:var(--band);color:var(--on-band);position:relative;overflow:hidden}
.band .wrap{padding-block:clamp(90px,13vw,170px)}
.band blockquote{margin:0;font-family:var(--display);font-weight:200;font-size:clamp(1.5rem,3.5vw,2.7rem);line-height:1.25;letter-spacing:-.03em;max-width:28ch;text-wrap:balance}
.band .mark{font-family:var(--display);font-size:clamp(6rem,14vw,11rem);line-height:.6;display:block;opacity:.35;height:.45em}
.band cite{display:block;margin-top:34px;font-style:normal;font-family:var(--mono);font-size:.78rem;opacity:.8}
.band canvas{position:absolute;inset:0;width:100%;height:100%;opacity:.55;pointer-events:none}

/* work */
.intro{max-width:52ch;color:var(--muted);margin:26px 0 0;font-size:1.05rem}
.projects{list-style:none;margin:64px 0 0;padding:0;border-top:1px solid var(--line)}
.proj{display:grid;grid-template-columns:minmax(0,9rem) minmax(0,1fr) minmax(0,15rem);gap:clamp(18px,3vw,44px);padding:clamp(30px,4vw,46px) 0;border-bottom:1px solid var(--line);position:relative;align-items:baseline}
.proj .meta{font-family:var(--mono);font-size:.74rem;color:var(--muted);display:grid;gap:6px}
.status{display:inline-flex;align-items:center;gap:8px;color:var(--ink)}
.status::before{content:"";width:7px;height:7px;border-radius:50%;border:1px solid var(--wine)}
.status.done::before{background:var(--wine)}
.proj h3{font-family:var(--display);font-weight:300;font-size:clamp(1.4rem,2.5vw,2rem);line-height:1.15;margin:0;letter-spacing:-.03em;transition:transform .7s var(--ease),color .5s}
.proj h3 a{text-decoration:none}
.proj:hover h3{transform:translateX(10px);color:var(--wine)}
.proj p{margin:14px 0 0;max-width:56ch;color:var(--ink)}
.proj .tech{font-family:var(--mono);font-size:.74rem;color:var(--muted);line-height:1.7;padding-top:.6em}
@media (max-width:860px){.proj{grid-template-columns:minmax(0,1fr)}.proj .meta{grid-auto-flow:column;justify-content:start;gap:18px}.proj .tech{padding-top:0}}

/* skills */
.skills{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:clamp(28px,4vw,56px);margin-top:64px}
.skill h3{font-family:var(--mono);font-weight:400;font-size:.74rem;color:var(--wine);margin:0 0 18px;padding-bottom:14px;border-bottom:1px solid var(--line)}
.skill .items{font-family:var(--body);font-size:1.12rem;line-height:1.6}
.skill .items span{display:block}
.skill .items span:first-child{font-family:var(--display);font-weight:300;font-size:1.5rem;letter-spacing:-.03em;line-height:1.2;margin-bottom:8px}
@media (max-width:860px){.skills{grid-template-columns:repeat(2,minmax(0,1fr))}}
@media (max-width:460px){.skills{grid-template-columns:minmax(0,1fr)}}

/* achievements */
.ach{list-style:none;margin:64px 0 0;padding:0}
.ach li{display:grid;grid-template-columns:minmax(0,13rem) minmax(0,1fr) auto;gap:clamp(18px,4vw,56px);align-items:baseline;padding:30px 0;border-top:1px solid var(--line)}
.ach li:last-child{border-bottom:1px solid var(--line)}
.ach .big{font-family:var(--display);font-weight:300;font-size:clamp(2.6rem,5.4vw,4.2rem);line-height:.95;letter-spacing:-.05em;color:var(--wine);font-weight:200}
.ach h3{font-family:var(--display);font-weight:300;font-size:1.25rem;letter-spacing:-.02em;line-height:1.15;margin:0}
.ach p{margin:8px 0 0;color:var(--muted);max-width:56ch}
.ach .yr{font-family:var(--mono);font-size:.74rem;color:var(--muted)}
@media (max-width:760px){.ach li{grid-template-columns:minmax(0,1fr)}.ach .big:empty{display:none}}

/* cv */
.cv-head{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:end;gap:28px}
.btn{font:500 .9rem var(--body);display:inline-flex;align-items:center;gap:10px;padding:13px 22px;border-radius:999px;border:1px solid var(--ink);background:transparent;color:var(--ink);text-decoration:none;cursor:pointer;transition:background .35s,color .35s,border-color .35s}
.btn:hover{background:var(--ink);color:var(--ivory)}
.btn.solid{background:var(--wine);border-color:var(--wine);color:var(--ivory)}
.btn.solid:hover{background:var(--ink);border-color:var(--ink)}
.btn .arr{transition:transform .4s var(--ease)}
.btn:hover .arr{transform:translateX(4px)}
.note{font-family:var(--mono);font-size:.74rem;color:var(--muted)}
.timeline{list-style:none;margin:64px 0 0;padding:0}
.timeline li{display:grid;grid-template-columns:minmax(0,10rem) minmax(0,1fr);gap:clamp(18px,4vw,56px);padding:30px 0;border-top:1px solid var(--line)}
.timeline li:last-child{border-bottom:1px solid var(--line)}
.timeline .when{font-family:var(--mono);font-size:.78rem;color:var(--wine);padding-top:.5em;font-variant-numeric:tabular-nums}
.timeline h3{font-family:var(--display);font-weight:300;font-size:1.25rem;letter-spacing:-.02em;line-height:1.15;margin:0}
.timeline .where{display:block;font-family:var(--mono);font-size:.78rem;color:var(--muted);margin-top:6px}
.timeline p{margin:10px 0 0;max-width:60ch}
@media (max-width:640px){.timeline li{grid-template-columns:minmax(0,1fr);gap:6px}}

/* contact */
.contact{padding-block:clamp(100px,15vw,200px) clamp(60px,8vw,90px)}
.hello{font-family:var(--display);font-weight:200;font-size:clamp(3rem,10vw,8rem);line-height:.95;letter-spacing:-.05em;margin:22px 0 0}
.hello em{font-style:normal;color:var(--wine)}
.contact .sub{max-width:46ch;margin:30px 0 0;color:var(--muted);font-size:1.08rem}
.mail{display:flex;flex-wrap:wrap;align-items:center;gap:14px 22px;margin-top:54px;padding-block:26px;border-top:1px solid var(--line);border-bottom:1px solid var(--line)}
.mail .addr{font-family:var(--display);font-weight:300;letter-spacing:-.03em;font-size:clamp(1.05rem,3vw,2rem);line-height:1.1;user-select:all;min-width:0;overflow-wrap:anywhere}
.mail .copy{margin-left:auto}
.elsewhere{display:flex;flex-wrap:wrap;gap:16px 44px;margin-top:34px}
.elsewhere a,.elsewhere span.soon{font-family:var(--display);font-weight:300;font-size:1.1rem;text-decoration:none;display:inline-flex;align-items:baseline;gap:10px}
.elsewhere a small,.elsewhere .soon small{font-family:var(--mono);font-size:.7rem;color:var(--muted)}
.elsewhere a:hover{color:var(--wine)}
.elsewhere .soon{color:var(--muted)}
.ul{background:linear-gradient(currentColor,currentColor) 0 100%/0 1px no-repeat;transition:background-size .6s var(--ease)}
a:hover .ul{background-size:100% 1px}
footer{padding-block:34px 44px;font-family:var(--mono);font-size:.72rem;color:var(--muted)}
footer .wrap{display:flex;flex-wrap:wrap;justify-content:space-between;gap:12px}

:focus-visible{outline:2px solid var(--wine);outline-offset:3px;border-radius:2px}

/* computer-science details */
.hero::before{content:"";position:absolute;inset:0;pointer-events:none;background-image:radial-gradient(color-mix(in srgb,var(--ink) 22%,transparent) 1px,transparent 1.3px);background-size:26px 26px;-webkit-mask-image:linear-gradient(to bottom,#000 10%,transparent 95%);mask-image:linear-gradient(to bottom,#000 10%,transparent 95%);opacity:.55}
.eyebrow .prompt{color:var(--wine)}
.eyebrow .cmd{color:var(--ink)}
.eyebrow .cmt{display:block;margin-top:6px}
.caret{display:inline-block;width:.5em;height:1em;background:var(--wine);vertical-align:-.12em;margin-left:6px;animation:blink 1.1s steps(1) infinite}
@keyframes blink{50%{opacity:0}}
.label.code::before{display:none}
.label.code{gap:0;white-space:pre}
.label .kw{color:var(--muted)}
.label .pn{color:var(--muted)}
.links a{font-family:var(--mono);font-size:.76rem}
.brand .us{color:var(--wine);font-family:var(--mono);font-size:.9em;animation:blink 1.1s steps(1) infinite}
.sky .edge{fill:none;stroke:var(--wine);stroke-width:1;opacity:.13;stroke-dasharray:1;stroke-dashoffset:0}
.js .sky .edge{animation:draw 2.6s var(--ease) both}
.sky .node{fill:var(--ivory);stroke:var(--wine);stroke-width:1.2}
.sky .node.on{fill:var(--wine)}
.sky .pulse{fill:var(--wine)}
@media (max-width:760px){.sky{opacity:.45}}
.codeblock{font-family:var(--mono);font-size:.78rem;line-height:1.75;border:1px solid var(--line);margin:0 0 34px;background:color-mix(in srgb,var(--paper) 55%,transparent)}
.codeblock .tab{display:flex;gap:7px;align-items:center;padding:9px 14px;border-bottom:1px solid var(--line);color:var(--muted);font-size:.7rem}
.codeblock .tab i{width:8px;height:8px;border-radius:50%;border:1px solid var(--faint)}
.codeblock .tab span{margin-left:8px}
.codeblock pre{margin:0;padding:16px 16px 18px;white-space:pre-wrap;overflow-wrap:anywhere;color:var(--ink);font:inherit}
.codeblock .ln{color:var(--faint);user-select:none;display:inline-block;width:2ch;margin-right:12px;text-align:right}
.tk-k{color:var(--wine)}.tk-s{color:var(--muted)}.tk-n{color:var(--wine-2)}.tk-c{color:var(--faint);font-style:italic}
footer .exit{color:var(--wine)}

/* futuristic layer */
.progress{position:absolute;left:0;bottom:-1px;height:1px;width:100%;background:var(--wine);transform-origin:0 50%;transform:scaleX(0)}
.hud{position:absolute;right:max(24px,env(safe-area-inset-right,0px));top:clamp(56px,9vw,110px);font-family:var(--mono);font-size:.68rem;line-height:1.8;color:var(--muted);text-align:right}
.hud b{font-weight:400;color:var(--wine)}
.hud .dot{display:inline-block;width:6px;height:6px;border-radius:50%;background:var(--wine);margin-right:6px;vertical-align:1px;animation:blink 1.6s ease-in-out infinite}
@media (max-width:760px){.hud{display:none}}
.codeblock{position:relative;border-color:transparent;background:color-mix(in srgb,var(--paper) 45%,transparent)}
.codeblock::before,.codeblock::after{content:"";position:absolute;width:14px;height:14px;border:1px solid var(--wine);pointer-events:none}
.codeblock::before{top:-1px;left:-1px;border-right:0;border-bottom:0}
.codeblock::after{bottom:-1px;right:-1px;border-left:0;border-top:0}
.codeblock .tab{border-bottom-color:var(--line)}

/* editing */
.eo,.ed{display:none}
.editing .eo{display:block;font-family:var(--mono);font-size:.74rem;color:var(--muted);margin-top:10px}
.editing .ed{display:inline-flex}
.editing [data-path]{outline:1px dashed color-mix(in srgb,var(--wine) 45%,transparent);outline-offset:4px;border-radius:2px;cursor:text;min-width:2ch;display:inline-block}
.editing [data-path]:focus{outline:1.5px solid var(--wine);background:color-mix(in srgb,var(--wine) 6%,transparent)}
.editing [data-path]:empty::before{content:attr(data-ph);color:var(--faint)}
.editing .statement p [data-path],.editing .prose [data-path],.editing .band [data-path]{display:block}
.ed-btn{font:500 .78rem var(--body);border:1px dashed var(--wine);color:var(--wine);background:transparent;border-radius:999px;padding:6px 14px;cursor:pointer;margin-top:14px;gap:6px;align-items:center}
.ed-btn:hover{background:var(--wine);color:var(--ivory)}
.ed-row{gap:10px;flex-wrap:wrap}
.editbar{position:fixed;z-index:70;left:50%;transform:translateX(-50%);bottom:calc(18px + env(safe-area-inset-bottom,0px));display:flex;align-items:center;gap:10px;background:var(--ink);color:var(--ivory);padding:8px 8px 8px 20px;border-radius:999px;box-shadow:0 18px 50px -18px rgba(30,10,14,.55);max-width:calc(100vw - 32px);flex-wrap:wrap;justify-content:center}
.editbar .msg{font-size:.82rem;opacity:.85}
.editbar button{font:500 .82rem var(--body);border-radius:999px;padding:9px 16px;cursor:pointer;border:1px solid color-mix(in srgb,var(--ivory) 35%,transparent);background:transparent;color:var(--ivory)}
.editbar button.save{background:var(--wine);border-color:var(--wine);color:#fff}
.editbar button:disabled{opacity:.5;cursor:default}
.editpill{position:fixed;z-index:70;right:calc(18px + env(safe-area-inset-right,0px));bottom:calc(18px + env(safe-area-inset-bottom,0px));font:500 .82rem var(--body);background:var(--ink);color:var(--ivory);border:0;border-radius:999px;padding:11px 18px;cursor:pointer;box-shadow:0 14px 40px -16px rgba(30,10,14,.6);display:inline-flex;gap:8px;align-items:center}
.editpill:hover{background:var(--wine)}

@media (prefers-reduced-motion:reduce){
  *,*::before,*::after{animation:none!important;transition:none!important}
  html{scroll-behavior:auto}
  .js .rv.pre{transform:none;opacity:1}
}
</style>
<div id="app"></div>
<script type="application/json" id="content">{"name": "Vania Beigi", "first": "Vania", "last": "Beigi", "eyebrow": "portfolio v1.0 · University of Leeds · 2026", "tagline": "Learning to build the AI that comes next, and to make it useful for everyone.", "credits": [{"k": "Studying", "v": "Computer Science (AI) with Industrial Year"}, {"k": "At", "v": "University of Leeds"}, {"k": "Graduating", "v": "Class of 2030"}, {"k": "Currently", "v": "Writing Python, every day"}], "statement": "I got into AI because I believe it has good uses most people haven't heard of yet. I'm here to learn how to build them, and to help people find them.", "statementSig": "Why I'm here", "aboutTitle": "A little about me", "about": ["I'm Vania, a first-year Computer Science (Artificial Intelligence) student at the University of Leeds, on the four-year course with an industrial placement year. I graduate in 2030.", "Right now I write Python and I'm getting better at it every week. I haven't picked my corner of AI yet. Language models, computer vision, AI for good: I'm exploring all of it to find where I fit.", "What I do know is what I care about: useful things, made carefully, for people who wouldn't normally think AI was for them."], "offTitle": "Off the clock", "off": [{"t": "Reading", "d": ""}, {"t": "Friends", "d": ""}, {"t": "Animals", "d": ""}], "photo": "", "quote": "And, when you want something, all the universe conspires in helping you to achieve it.", "quoteBy": "Paulo Coelho, The Alchemist", "workTitle": "Things I've made, and things I want to make", "workIntro": "One finished project and a few I'm planning. I'll update this page as each one ships.", "projects": [{"title": "A game about the night sky", "status": "Finished · second place", "year": "2023", "desc": "An astronomy game I designed and built with a friend, teaching players about stars and planets through play. It won second place in a competition.", "tech": "Game design · Teamwork", "link": ""}, {"title": "Shelter match", "status": "Planned", "year": "2027", "desc": "A small Python model that looks at adoption data from animal shelters and flags the animals who might need extra attention to find a home.", "tech": "Python · pandas · scikit-learn", "link": ""}, {"title": "Echo", "status": "Idea", "year": "2028", "desc": "A phone assistant that describes the world out loud for people with low vision, using the camera and a vision-language model.", "tech": "Python · Computer vision · LLMs", "link": ""}, {"title": "Plain words", "status": "Planned", "year": "2027", "desc": "A tool that uses a language model to turn confusing letters and forms into plain English, for anyone who finds official writing hard to read.", "tech": "Python · LLM APIs", "link": ""}], "skillsTitle": "What I'm learning", "skills": [{"group": "Using now", "items": "Python · Problem solving · Writing clear code"}, {"group": "Learning now", "items": "Git & GitHub · Maths for machine learning · Data structures"}, {"group": "Next up", "items": "NumPy & pandas · scikit-learn · PyTorch"}, {"group": "Beyond code", "items": "Teamwork · Game design · Curiosity"}], "achTitle": "Milestones", "achievements": [{"big": "2nd", "title": "Second place, astronomy game", "desc": "Designed and built a game about astronomy with a friend, and placed second in the competition.", "year": "2023"}, {"big": "2026", "title": "Started at the University of Leeds", "desc": "Accepted onto Computer Science (Artificial Intelligence) with Industrial Year.", "year": "2026"}, {"big": "Next", "title": "First hackathon at Leeds", "desc": "Planning to join a university hackathon and the computing and AI societies.", "year": "2027"}], "cvTitle": "So far", "cv": [{"when": "2026 – 2030", "title": "BSc Computer Science (Artificial Intelligence) with Industrial Year", "where": "University of Leeds", "desc": "First year. Programming, mathematics for computing and computer systems."}, {"when": "2028 – 2029", "title": "Industrial year", "where": "Coming up", "desc": "A year working in industry as part of my degree. Still a long way off, and still deciding where."}, {"when": "2023", "title": "Second place, astronomy game competition", "where": "Built with a friend", "desc": "Game design, teamwork and teaching through play."}], "cvFile": "", "cvNote": "First chapter. More to come.", "helloA": "Say", "helloB": "hello.", "contactSub": "Want to swap book recommendations, start a study group, or build something fun together? Say hi.", "email": "vaniabeigi359@gmail.com", "github": "vanilla-cmp", "linkedin": "", "footer": "Built from scratch in HTML, CSS and JavaScript. Made in Leeds.", "focus": "machine learning · language models · AI for good"}</script>
<script id="main">
(function(){
"use strict";
var RESET=':root{color-scheme:light;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}body{margin:0;font:14px/1.5 system-ui,-apple-system,"Segoe UI",sans-serif}img{max-width:100%}[hidden]{display:none!important}';
var FONTS='<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Unbounded:wght@200;300;400;500&family=Instrument+Sans:wght@400;500;600&family=JetBrains+Mono:wght@400&display=swap">';
var S;
try{S=JSON.parse(document.getElementById('content').textContent)}catch(e){S={}}
var editing=false, artifact=null, assets=null, canEdit=false;
var app=document.getElementById('app');
document.documentElement.classList.add('js');

function esc(v){return String(v==null?'':v).replace(/[&<>"']/g,function(c){return{'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]})}
function get(p){return p.split('.').reduce(function(o,k){return o==null?o:o[k]},S)}
function set(p,v){var ks=p.split('.'),o=S;for(var i=0;i<ks.length-1;i++)o=o[ks[i]];o[ks[ks.length-1]]=v}
function f(p,tag,cls,ph){tag=tag||'span';return '<'+tag+(cls?' class="'+cls+'"':'')+' data-path="'+p+'" data-ph="'+esc(ph||'Type here')+'">'+esc(get(p))+'</'+tag+'>'}
function safeUrl(u){u=String(u||'').trim();return /^https:\/\//i.test(u)?u:''}
function blob(id){return id&&/^[0-9a-f]{32}$/i.test(id)?'/_blob/'+id:''}
function del(list,i,what){return '<button class="ed ed-btn" data-del="'+list+'.'+i+'">Remove '+what+'</button>'}
function add(list,what){return '<button class="ed ed-btn" data-add="'+list+'">+ Add '+what+'</button>'}
function splitItems(s){return String(s||'').split('·').map(function(x){return x.trim()}).filter(Boolean)}

function render(){
  var h='';
  h+='<nav class="nav" id="nav"><div class="wrap"><a class="brand" href="#top">'+esc(S.first)+' <i>'+esc(S.last)+'</i><span class="us" aria-hidden="true">_</span></a><div class="links">'+
     [['about','About'],['work','Projects'],['skills','Skills'],['achievements','Achievements'],['cv','CV'],['contact','Contact']].map(function(l){return '<a href="#'+l[0]+'"'+(l[0]==='contact'?' class="keep"':'')+'>./'+l[1].toLowerCase()+'</a>'}).join('')+'</div></div><div class="progress" id="progress"></div></nav>';

  // hero
  h+='<header class="hero" id="top"><svg class="sky" id="sky" aria-hidden="true"></svg><div class="hud" aria-hidden="true"><span class="dot"></span>status: <b>learning</b><br>53.80° N, 1.55° W · Leeds<br>build 2026.1 · uptime: year 1</div><div class="wrap">'+
     '<div class="eyebrow"><span class="prompt">vania@leeds:~$</span> <span class="cmd" id="cmd">whoami</span><span class="cmt"># '+f('eyebrow')+'</span></div>'+
     '<h1 class="name"><span class="l1">'+f('first')+'</span><span class="l2">'+f('last')+'</span></h1>'+
     '<p class="tagline">'+f('tagline')+(editing?'':'<span class="caret" aria-hidden="true"></span>')+'</p>'+
     '<div class="credits">'+S.credits.map(function(c,i){return '<div class="credit rv">'+f('credits.'+i+'.k','span','k')+f('credits.'+i+'.v','span','v')+'</div>'}).join('')+'</div>'+
     '</div></header>';

  // statement
  var st=editing?f('statement'):'<span data-path="statement">'+String(S.statement||'').split(/\s+/).map(function(w){return '<span class="w">'+esc(w)+'</span>'}).join(' ')+'</span>';
  h+='<section class="statement" id="statement"><div class="wrap"><p>'+st+'</p><div class="sig">— '+f('statementSig')+'</div></div></section><hr class="rule">';

  // about
  var ph=blob(S.photo);
  h+='<section class="chapter" id="about"><div class="wrap"><div class="label">About</div><h2 class="h2 rv">'+f('aboutTitle')+'</h2>'+
     '<div class="about-grid"><div class="prose rv">'+S.about.map(function(p,i){return '<p>'+f('about.'+i)+'</p>'+(editing?del('about',i,'paragraph'):'')}).join('')+add('about','paragraph')+'</div>'+
     '<aside class="rv">'+(ph?'<figure class="portrait"><img src="'+ph+'" alt="Portrait of '+esc(S.name)+'"></figure>':'')+
       '<div class="ed ed-row" style="margin-bottom:24px"><button class="ed-btn" data-upload="photo">'+(ph?'Replace photo':'+ Add a photo of you')+'</button>'+(ph?'<button class="ed-btn" data-clear="photo">Remove photo</button>':'')+'</div>'+
       codeBlock()+'<div class="offclock"><h3>'+f('offTitle')+'</h3><p class="offline">'+S.off.map(function(o,i){return f('off.'+i+'.t')+(editing?del('off',i,''):'')}).join('<span class="sep">·</span>')+'</p>'+add('off','item')+'</div>'+
     '</aside></div></div></section>';

  // quote band
  h+='<section class="band" aria-label="A favourite quote"><canvas id="bandsky" aria-hidden="true"></canvas><div class="wrap" style="position:relative"><span class="mark" aria-hidden="true">“</span><blockquote>'+f('quote')+'</blockquote><cite>'+f('quoteBy')+'</cite></div></section>';

  // projects
  h+='<section class="chapter" id="work"><div class="wrap"><div class="label">Projects</div><h2 class="h2 rv">'+f('workTitle')+'</h2><p class="intro">'+f('workIntro')+'</p><ol class="projects">'+
     S.projects.map(function(p,i){
       var u=safeUrl(p.link), done=/finish|done|live|shipped|won|place/i.test(p.status||'');
       var title=(!editing&&u)?'<a href="'+esc(u)+'" target="_blank" rel="noopener"><span class="ul">'+esc(p.title)+'</span> <span aria-hidden="true">↗</span></a>':f('projects.'+i+'.title');
       return '<li class="proj rv"><div class="meta"><span class="status'+(done?' done':'')+'">'+f('projects.'+i+'.status')+'</span>'+f('projects.'+i+'.year')+'</div>'+
         '<div><h3>'+title+'</h3><p>'+f('projects.'+i+'.desc')+'</p><div class="eo">Link (https://…): '+f('projects.'+i+'.link','span','','optional')+'</div>'+(editing?del('projects',i,'project'):'')+'</div>'+
         '<div class="tech">'+f('projects.'+i+'.tech')+'</div></li>';
     }).join('')+'</ol>'+add('projects','project')+'</div></section><hr class="rule">';

  // skills
  h+='<section class="chapter" id="skills"><div class="wrap"><div class="label">Technical skills</div><h2 class="h2 rv">'+f('skillsTitle')+'</h2><div class="skills">'+
     S.skills.map(function(s,i){
       var items=editing?f('skills.'+i+'.items'):'<span data-path="skills.'+i+'.items" style="display:contents">'+splitItems(s.items).map(function(x){return '<span>'+esc(x)+'</span>'}).join('')+'</span>';
       return '<div class="skill rv"><h3>'+f('skills.'+i+'.group')+'</h3><div class="items">'+items+'</div>'+(editing?'<div class="eo">Separate items with ·</div>'+del('skills',i,'group'):'')+'</div>';
     }).join('')+'</div>'+add('skills','group')+'</div></section><hr class="rule">';

  // achievements
  h+='<section class="chapter" id="achievements"><div class="wrap"><div class="label">Creative achievements</div><h2 class="h2 rv">'+f('achTitle')+'</h2><ul class="ach">'+
     S.achievements.map(function(a,i){return '<li class="rv">'+f('achievements.'+i+'.big','div','big','2nd')+'<div>'+f('achievements.'+i+'.title','h3')+'<p>'+f('achievements.'+i+'.desc')+'</p>'+(editing?del('achievements',i,'achievement'):'')+'</div>'+f('achievements.'+i+'.year','div','yr')+'</li>'}).join('')+
     '</ul>'+add('achievements','achievement')+'</div></section><hr class="rule">';

  // cv
  var cvu=blob(S.cvFile);
  h+='<section class="chapter" id="cv"><div class="wrap"><div class="label">CV</div><div class="cv-head"><h2 class="h2 rv">'+f('cvTitle')+'</h2>'+
     '<div>'+(cvu?'<a class="btn solid" href="'+cvu+'" target="_blank" rel="noopener">Open full CV (PDF) <span class="arr">→</span></a>':'<span class="note">'+f('cvNote')+'</span>')+
     '<div class="ed ed-row"><button class="ed-btn" data-upload="cvFile">'+(cvu?'Replace CV PDF':'+ Upload CV PDF')+'</button>'+(cvu?'<button class="ed-btn" data-clear="cvFile">Remove CV</button>':'')+'</div></div></div>'+
     '<ol class="timeline">'+S.cv.map(function(c,i){return '<li class="rv">'+f('cv.'+i+'.when','div','when')+'<div>'+f('cv.'+i+'.title','h3')+f('cv.'+i+'.where','span','where')+'<p>'+f('cv.'+i+'.desc')+'</p>'+(editing?del('cv',i,'entry'):'')+'</div></li>'}).join('')+'</ol>'+add('cv','entry')+'</div></section>';

  // contact
  var gh=String(S.github||'').trim(), li=safeUrl(S.linkedin);
  h+='<section class="contact" id="contact"><div class="wrap"><div class="label">Contact</div><h2 class="hello">'+f('helloA')+' <em>'+f('helloB')+'</em></h2><p class="sub">'+f('contactSub')+'</p>'+
     '<div class="mail"><span class="addr" id="addr">'+f('email')+'</span><button class="btn copy" id="copy" type="button">Copy email</button></div>'+
     '<div class="elsewhere">'+
       (editing?'<div class="eo" style="display:block">GitHub username: '+f('github')+'<br>LinkedIn URL (https://…): '+f('linkedin','span','','add when ready')+'</div>':
       (gh?'<a href="https://github.com/'+esc(encodeURIComponent(gh))+'" target="_blank" rel="noopener"><span class="ul">GitHub</span> <small>@'+esc(gh)+'</small></a>':'')+
       (li?'<a href="'+esc(li)+'" target="_blank" rel="noopener"><span class="ul">LinkedIn</span> <small>↗</small></a>':'<span class="soon">LinkedIn <small>coming soon</small></span>'))+
     '</div></div></section>';

  h+='<footer><div class="wrap"><span>© '+new Date().getFullYear()+' '+esc(S.name)+'</span>'+f('footer')+'</div></footer>';
  h+='<input type="file" id="fileIn" hidden>';

  if(canEdit){
    h+=editing?'<div class="editbar" role="toolbar" aria-label="Editing"><span class="msg" id="edmsg">Click any outlined text to change it.</span><button id="cancel" type="button">Cancel</button><button class="save" id="save" type="button">Save &amp; publish</button></div>'
              :'<button class="editpill" id="editbtn" type="button">✎ Edit page</button>';
  }
  h=h.replace(/<div class="label">([^<]+)<\/div>/g,function(m,t){return '<div class="label code"><span class="kw">def </span>'+t.trim().toLowerCase().replace(/\s+/g,'_')+'<span class="pn">():</span></div>'});
  app.innerHTML=h;
  document.body.classList.toggle('editing',editing);
  wire();
}

function codeBlock(){
  var k=function(s){return '<span class="tk-k">'+s+'</span>'}, s=function(v){return '<span class="tk-s">"'+esc(v)+'"</span>'};
  var cr=S.credits||[], loves=splitItems(S.focus).map(function(o){return s(o.toLowerCase())}).join(', ');
  var lines=[
    k('class')+' Vania:',
    '    course = '+s(((cr[0]&&cr[0].v)||'').replace(/\s+with\s+.*$/i,'')),
    '    uni = '+s((cr[1]&&cr[1].v)||''),
    '    graduating = <span class="tk-n">'+esc(String(((cr[2]&&cr[2].v)||'').replace(/\D/g,'')||'2030'))+'</span>',
    '    focus = ['+loves+']',
    '',
    '    '+k('def')+' future(self):',
    '        '+k('return')+' '+s('AI that helps people'),
    '<span class="tk-c"># training in progress… epoch 1 of 4</span>'
  ];
  return '<figure class="codeblock" aria-label="A short Python description of Vania"><div class="tab"><i></i><i></i><i></i><span>vania.py</span></div><pre>'+
    lines.map(function(l,i){return '<span class="ln">'+(i+1)+'</span>'+l}).join('\n')+'</pre></figure>'+(editing?'<div class="eo" style="margin:-22px 0 28px">focus (separate with ·): '+f('focus')+'</div>':'');
}

function collect(){
  app.querySelectorAll('[data-path]').forEach(function(el){
    var p=el.getAttribute('data-path');
    var v=(el.innerText||el.textContent||'').replace(/ /g,' ').replace(/\n{3,}/g,'\n\n').trim();
    if(p==='name')return;
    set(p,v);
  });
  S.name=((S.first||'')+' '+(S.last||'')).trim();
}

var templates={
  about:function(){return 'A new paragraph about you.'},
  off:function(){return {t:'Something you love',d:'A line about it.'}},
  projects:function(){return {title:'New project',status:'Planned',year:String(new Date().getFullYear()),desc:'What it does and why it matters.',tech:'Python',link:''}},
  skills:function(){return {group:'New group',items:'Skill one · Skill two'}},
  achievements:function(){return {big:'',title:'New achievement',desc:'What happened.',year:String(new Date().getFullYear())}},
  cv:function(){return {when:String(new Date().getFullYear()),title:'New entry',where:'Where',desc:'What you did.'}}
};

function msg(t){var m=document.getElementById('edmsg');if(m)m.textContent=t}

function wire(){
  if(editing){
    app.querySelectorAll('[data-path]').forEach(function(el){
      try{el.contentEditable='plaintext-only'}catch(e){el.contentEditable='true'}
      if(el.contentEditable!=='plaintext-only')el.contentEditable='true';
      el.spellcheck=true;
      el.addEventListener('keydown',function(e){if(e.key==='Enter'&&!/^(about\.\d+|statement|quote)$/.test(el.dataset.path)){e.preventDefault();el.blur()}});
    });
  }
  app.querySelectorAll('[data-add]').forEach(function(b){b.onclick=function(){collect();var k=b.dataset.add;S[k].push(templates[k]());render()}});
  app.querySelectorAll('[data-del]').forEach(function(b){b.onclick=function(){collect();var p=b.dataset.del.split('.');S[p[0]].splice(+p[1],1);render()}});
  app.querySelectorAll('[data-clear]').forEach(function(b){b.onclick=function(){collect();S[b.dataset.clear]='';render()}});
  app.querySelectorAll('[data-upload]').forEach(function(b){b.onclick=function(){
    if(!assets){msg('Uploads are not available in this view.');return}
    var key=b.dataset.upload, inp=document.getElementById('fileIn');
    inp.accept=key==='photo'?'image/*':'application/pdf';
    inp.onchange=function(){
      var file=inp.files&&inp.files[0]; if(!file)return;
      collect(); msg('Uploading…');
      assets.upload(file).then(function(r){S[key]=r.id;render();msg((key==='photo'?'Photo':'CV')+' added. Save to publish it.')})
        .catch(function(e){msg('Upload failed: '+((e&&e.message)||'try a smaller file')+'.')});
    };
    inp.value='';inp.click();
  }});
  var eb=document.getElementById('editbtn'); if(eb)eb.onclick=function(){editing=true;render();msg('Click any outlined text to change it.')};
  var cb=document.getElementById('cancel'); if(cb)cb.onclick=function(){try{S=JSON.parse(document.getElementById('content').textContent)}catch(e){}editing=false;render()};
  var sb=document.getElementById('save'); if(sb)sb.onclick=save;
  var cp=document.getElementById('copy'); if(cp)cp.onclick=function(){
    var addr=String(S.email||'');
    var sel=function(){var r=document.createRange();r.selectNodeContents(document.getElementById('addr'));var s=getSelection();s.removeAllRanges();s.addRange(r);cp.textContent='Selected, press Ctrl+C'};
    try{navigator.clipboard.writeText(addr).then(function(){cp.textContent='Copied';setTimeout(function(){cp.textContent='Copy email'},1800)},sel)}catch(e){sel()}
  };
  if(!editing){drawSky();statementWords();reveal();}
  drawBand();navState();
}

function buildDoc(){
  var css=document.getElementById('css').textContent;
  var js=document.getElementById('main').textContent;
  var data=JSON.stringify(S).replace(/</g,'\\u003c');
  return '<!doctype html><html><head><meta charset=utf8><meta name=viewport content="width=device-width,initial-scale=1,viewport-fit=cover"><style>'+RESET+'</style></head><body>'+
    '<title>'+esc(S.name||'Portfolio')+'</title>\n<meta name="claude:viewport-fit-sides" content="cover">\n'+FONTS+'\n'+
    '<style id="css">'+css+'</style>\n<div id="app"></div>\n'+
    '<script type="application/json" id="content">'+data+'<\/script>\n'+
    '<script id="main">'+js+'<\/script></body></html>';
}

function save(){
  collect();
  var sb=document.getElementById('save'); if(sb)sb.disabled=true;
  msg('Publishing…');
  if(!artifact){msg('Saving is not available in this view.');if(sb)sb.disabled=false;return}
  artifact.publish(buildDoc()).then(function(){msg('Published. Reloading…')}).catch(function(e){
    var c=e&&e.code;
    if(c==='conflict')msg('A newer version was saved elsewhere. Loading it now.');
    else if(c==='not_writer'||c==='not_granted'||c==='not_declared'||c==='consent_required'){msg('This view is read-only, so changes cannot be saved here.');}
    else if(c==='too_large')msg('The page is too large to save. Try a smaller photo.');
    else if(c==='rate_limited')msg('Saving too often. Wait a minute, then save again.');
    else msg('Could not save just now. Your edits are still here; try Save again.');
    if(sb)sb.disabled=false;
  });
}

/* ---------- visuals ---------- */
function rng(seed){return function(){seed=(seed*16807)%2147483647;return (seed-1)/2147483646}}
function drawSky(){
  var svg=document.getElementById('sky'); if(!svg)return;
  var W=1200,H=700; svg.setAttribute('viewBox','0 0 '+W+' '+H); svg.setAttribute('preserveAspectRatio','xMaxYMin slice');
  var r=rng(20302026), sizes=[3,5,5,4,2], layers=[], s='', i, j, L;
  for(L=0;L<sizes.length;L++){var x=W*(0.64+0.32*L/(sizes.length-1)),col=[];
    for(i=0;i<sizes[L];i++)col.push([x+(r()-.5)*16, H*0.43+(i-(sizes[L]-1)/2)*60+(r()-.5)*12]);layers.push(col)}
  for(L=0;L<layers.length-1;L++)layers[L].forEach(function(a){layers[L+1].forEach(function(b){
    s+='<line class="edge" pathLength="1" x1="'+a[0].toFixed(1)+'" y1="'+a[1].toFixed(1)+'" x2="'+b[0].toFixed(1)+'" y2="'+b[1].toFixed(1)+'" style="animation-delay:'+(0.25+L*0.45).toFixed(2)+'s"/>'})});
  var reduce=matchMedia('(prefers-reduced-motion: reduce)').matches;
  if(!reduce)for(j=0;j<5;j++){var d='',pt;for(L=0;L<layers.length;L++){pt=layers[L][Math.floor(r()*layers[L].length)];d+=(L?' L':'M')+pt[0].toFixed(1)+' '+pt[1].toFixed(1)}
    s+='<circle class="pulse" r="2.4" opacity="0"><animateMotion dur="3.2s" begin="'+(2.6+j*1.3).toFixed(1)+'s;p'+j+'.end+'+(2+r()*3).toFixed(1)+'s" id="p'+j+'" path="'+d+'" fill="freeze"/><animate attributeName="opacity" values="0;.9;.9;0" dur="3.2s" begin="'+(2.6+j*1.3).toFixed(1)+'s;p'+j+'.end+'+(2+r()*3).toFixed(1)+'s"/></circle>'}
  layers.forEach(function(col,L){col.forEach(function(p,k){s+='<circle class="node'+((L+k)%4===0?' on':'')+'" cx="'+p[0].toFixed(1)+'" cy="'+p[1].toFixed(1)+'" r="'+(L===0||L===layers.length-1?4.5:3.5)+'"/>'})});
  svg.innerHTML=s;
  var cmd=document.getElementById('cmd');
  if(cmd&&!reduce){var full=cmd.textContent,n=0;cmd.textContent='';var t=setInterval(function(){cmd.textContent=full.slice(0,++n);if(n>=full.length)clearInterval(t)},110)}
}
function drawBand(){
  var c=document.getElementById('bandsky'); if(!c)return;
  var dpr=Math.min(2,window.devicePixelRatio||1),w=c.clientWidth,h=c.clientHeight; if(!w||!h)return;
  c.width=w*dpr;c.height=h*dpr;var x=c.getContext('2d');x.scale(dpr,dpr);
  var col=getComputedStyle(document.documentElement).getPropertyValue('--on-band').trim()||'#F6EEE0';
  var r=rng(7),stars=[];
  for(var i=0;i<70;i++)stars.push([r()*w,r()*h,r()*1.1+.2,r()]);
  x.fillStyle=col;
  stars.forEach(function(s){x.globalAlpha=.15+s[3]*.45;x.beginPath();x.arc(s[0],s[1],s[2],0,7);x.fill()});
  // one small constellation, top right
  var cs=[[.72,.22],[.78,.16],[.85,.2],[.88,.31],[.82,.38]].map(function(p){return [p[0]*w,p[1]*h]});
  x.globalAlpha=.4;x.strokeStyle=col;x.lineWidth=.7;x.beginPath();cs.forEach(function(p,i){i?x.lineTo(p[0],p[1]):x.moveTo(p[0],p[1])});x.stroke();
  x.globalAlpha=.85;cs.forEach(function(p){x.beginPath();x.arc(p[0],p[1],1.8,0,7);x.fill()});
}
function grain(){
  try{var c=document.createElement('canvas');c.width=c.height=160;var x=c.getContext('2d'),d=x.createImageData(160,160);
    for(var i=0;i<d.data.length;i+=4){var v=Math.random()*255|0;d.data[i]=d.data[i+1]=d.data[i+2]=v;d.data[i+3]=255}
    x.putImageData(d,0,0);var g=document.createElement('div');g.className='grain';g.style.backgroundImage='url('+c.toDataURL()+')';document.body.appendChild(g)}catch(e){}
}
var wordsTick=null;
function statementWords(){
  var sec=document.getElementById('statement'); if(!sec)return;
  var ws=sec.querySelectorAll('.w');
  wordsTick=function(){
    var r=sec.getBoundingClientRect(),vh=innerHeight;
    var p=Math.min(1,Math.max(0,(vh*0.85-r.top)/(r.height*0.75)));
    var k=Math.round(p*ws.length);
    ws.forEach(function(w,i){w.classList.toggle('on',i<k)});
  };
  if(matchMedia('(prefers-reduced-motion: reduce)').matches){ws.forEach(function(w){w.classList.add('on')});wordsTick=null;return}
  wordsTick();
}
function scramble(el){
  var final=el.textContent,glyphs='01<>/{}[]=+*#',start=null,dur=700;
  function step(t){if(start===null)start=t;var p=Math.min(1,(t-start)/dur),n=Math.floor(p*final.length),out='';
    for(var i=0;i<final.length;i++){var c=final[i];out+=(i<n||c===' ')?c:glyphs[Math.floor(Math.random()*glyphs.length)]}
    el.textContent=out;if(p<1)requestAnimationFrame(step);else el.textContent=final}
  requestAnimationFrame(step);
}
function reveal(){
  if(!matchMedia('(prefers-reduced-motion: reduce)').matches&&('IntersectionObserver' in window)){
    var so=new IntersectionObserver(function(es){es.forEach(function(e){if(e.isIntersecting){var t=e.target.querySelector('[data-path]');if(t&&!editing)scramble(t);so.unobserve(e.target)}})},{rootMargin:'0px 0px -12% 0px'});
    app.querySelectorAll('.h2').forEach(function(h){so.observe(h)});
  }
  if(!('IntersectionObserver' in window))return;
  var vh=innerHeight;
  var io=new IntersectionObserver(function(es){es.forEach(function(e){if(e.isIntersecting){e.target.classList.remove('pre');io.unobserve(e.target)}})},{rootMargin:'0px 0px -8% 0px'});
  app.querySelectorAll('.rv').forEach(function(el){if(el.getBoundingClientRect().top>vh*0.92){el.classList.add('pre');io.observe(el)}});
}
function navState(){
  var nav=document.getElementById('nav'),links=[].slice.call(app.querySelectorAll('.links a'));
  var secs=links.map(function(a){return document.getElementById(a.getAttribute('href').slice(1))});
  function tick(){
    nav.classList.toggle('scrolled',scrollY>20);
    var pr=document.getElementById('progress'),mx=document.documentElement.scrollHeight-innerHeight;if(pr)pr.style.transform='scaleX('+(mx>0?Math.min(1,scrollY/mx):0)+')';
    var cur=null;secs.forEach(function(s,i){if(s&&s.getBoundingClientRect().top<innerHeight*0.4)cur=i});
    links.forEach(function(a,i){a.classList.toggle('active',i===cur)});
    if(wordsTick)wordsTick();
  }
  window.onscroll=tick;tick();
}
var rz;window.addEventListener('resize',function(){clearTimeout(rz);rz=setTimeout(drawBand,200)});

grain();
render();

/* editing is offered only to people who can publish this page */
if(window.claude&&window.claude.use){
  Promise.all([window.claude.use('artifact'),window.claude.use('user'),window.claude.use('assets')]).then(function(r){
    artifact=r[0];assets=r[2];
    var u=r[1];
    return (u&&u.canEdit?u.canEdit():Promise.resolve(false)).then(function(ok){
      canEdit=!!(ok&&artifact);
      if(canEdit&&!editing)render();
    });
  }).catch(function(){});
}
})();
</script>

</body>
</html>
