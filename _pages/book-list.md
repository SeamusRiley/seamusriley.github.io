---
title: "Books I Have Read"
layout: single
sidebar:
  nav: false
author_profile: false
permalink: /books/
excerpt: 'Also includes comic strips and anthologies. See Also <a href="/movies-shows/">Movies &amp; Shows</a>, <a href="/stage-productions/">Stage Productions</a>'
---

Also includes comic strips and anthologies. See Also <a href="/movies-shows/">Movies &amp; Shows</a>, <a href="/stage-productions/">Stage Productions</a>
<style>
/* Bookshelf layout */
.bk-shelf {
  margin: 1.4em 0 .2em;
}

.bk-row {
  display: flex;
  align-items: flex-end;
  gap: 0;
  padding: 0 8px;
}

.bk-board {
  height: 12px;
  background: linear-gradient(#98764e,#876542 45%,#71552f);
  border-radius: 2px;
  box-shadow: 0 3px 5px rgba(0,0,0,.35);
  margin-bottom: 20px;
}

/* Spines */
.bk-spine {
  display: flex;
  flex: none;
  align-items: center;
  justify-content: center;
  border-radius: 3px 3px 1px 1px;
  box-shadow: inset -2px 0 3px rgba(0,0,0,.35),inset 2px 0 2px rgba(255,255,255,.14);
}

.bk-spine a,
.bk-spine span {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
  color: #f7f1e3;
  text-decoration: none;
  font-size: 12.5px;
  letter-spacing: .4px;
  white-space: nowrap;
  overflow: hidden;
  max-height: 220px;
}

.bk-spine.bk-long a,
.bk-spine.bk-long span {
  font-size: 10.5px;
}

/* Bookend */
.bk-bookend {
  width: 114px;
  height: 114px;
  flex: none;
  background: linear-gradient(#98764e,#876542 45%,#71552f);
  border-radius: 2px;
  box-shadow: inset 0 0 0 2px rgba(0,0,0,.18),inset 0 2px 3px rgba(255,255,255,.15),inset 0 -3px 5px rgba(0,0,0,.3);
  display: flex;
  align-items: flex-start;
  justify-content: center;
  box-sizing: border-box;
}

.bk-bookend img {
  width: 78%;
  height: auto;
  object-fit: contain;
}

/* Flat spine (review pages) */
.bk-spine-h {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  padding-left: 10px;
  border-radius: 1px 3px 3px 1px;
  box-shadow: inset 0 -2px 3px rgba(0,0,0,.35),inset 0 2px 2px rgba(255,255,255,.14);
}

.bk-spine-h span {
  color: #f7f1e3;
  font-size: 12.5px;
  letter-spacing: .4px;
  white-space: nowrap;
  overflow: hidden;
}

.bk-spine-h.bk-long span {
  font-size: 10.5px;
}

/* Legend */
.bk-legend {
  font-size: .85em;
  margin: .1em 0 1.5em;
}

.bk-dot {
  display: inline-block;
  width: .7em;
  height: .7em;
  border-radius: 2px;
  margin: 0 .3em 0 .9em;
}
</style>
<style>
/* Collections and the Children's divider (2026-11-02). Book-list page
   only; review pages keep the plainer SHELF_CSS above. */
.bk-coll {
  flex-direction: row;
  gap: 5px;
  position: relative;
  overflow: hidden;
  cursor: pointer;
  box-sizing: border-box;
  padding: 20px 4px;
}

.bk-coll::before,
.bk-coll::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  height: 9px;
  background: linear-gradient(90deg, #a87e1f, #f3d27a 30%, #d4af37 55%, #8a6414);
  z-index: 1;
}

.bk-coll::before { top: 9px; }
.bk-coll::after { bottom: 9px; }

.bk-coll-name,
.bk-coll-hint {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
  color: #f7f1e3;
  letter-spacing: .4px;
  white-space: nowrap;
  overflow: hidden;
}

.bk-coll-name { font-size: 12.5px; max-height: 100%; }
.bk-coll.bk-long .bk-coll-name { font-size: 10.5px; }
.bk-coll-hint { font-size: 9px; opacity: .85; }

.bk-controls { margin: 1.2em 0 0; }

.bk-controls button {
  font: inherit;
  font-size: .9em;
  padding: .35em 1.1em;
  border: 1px solid #71552f;
  border-radius: 3px;
  background: linear-gradient(#98764e, #876542);
  color: #f7f1e3;
  cursor: pointer;
}

.bk-divider {
  flex: none;
  align-self: stretch;
  gap: 5px;
  position: relative;
  border-radius: 3px 3px 1px 1px;
  background: linear-gradient(90deg, #71552f, #876542 45%, #98764e);
  box-shadow: inset 0 0 0 2px rgba(0,0,0,.15),
              inset -2px 0 3px rgba(255,255,255,.12),
              2px 0 4px rgba(0,0,0,.25);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.bk-divider::before,
.bk-divider::after {
  content: "";
  position: absolute;
  left: 0;
  right: 0;
  height: 9px;
  background: linear-gradient(90deg, #4c5a1e, #8fa63f 30%, #67782a 55%, #425018);
  z-index: 1;
}

.bk-divider::before { top: 9px; }
.bk-divider::after { bottom: 9px; }

.bk-divider span {
  writing-mode: vertical-rl;
  transform: rotate(180deg);
  color: #f7f1e3;
  font-size: 13px;
  letter-spacing: .4px;
  white-space: nowrap;
}

.bk-divider .bk-divider-hint { font-size: 9px; opacity: .85; }
</style>
<div class="bk-controls"><button type="button" id="bk-toggle-all">Expand all</button></div>
<div class="bk-shelf" id="bookshelf" style="display:flex;align-items:stretch;width:100%;max-width:762px">
<div style="width:16px;flex:none;border-radius:2px;background:linear-gradient(90deg,#71552f,#876542 45%,#98764e);box-shadow:inset 0 0 0 2px rgba(0,0,0,.15),inset -2px 0 3px rgba(255,255,255,.12),2px 0 4px rgba(0,0,0,.25)"></div>
<div id="bk-main" style="flex:1;min-width:0">
<div class="bk-spine" data-genre="nonfiction" data-w="27" style="width:27px;height:218.6px;background:#7a6a58"><a href="/books/born-to-run-a-hidden-tribe-superathletes-and-the-greatest-race-the-world-has-never-seen/" title="Born to Run: A Hidden Tribe, Superathletes, and the Greatest Race the World Has Never Seen" style="max-height:206.6px">Born to Run &#9733;</a></div>
<div class="bk-spine" data-genre="mind" data-w="27" style="width:27px;height:237.0px;background:#96502e"><a href="/books/codependent-no-more/" title="Codependent No More" style="max-height:225.0px">Codependent No More</a></div>
<div class="bk-spine" data-genre="mind" data-w="20" style="width:20px;height:204.3px;background:#96502e"><a href="/books/the-therapy-manifesto-a-principled-guide-to-developing-your-mental-health/" title="The Therapy Manifesto: A Principled Guide to Developing Your Mental Health" style="max-height:192.3px"><strong>The Therapy Manifesto</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="philosophy" data-w="27" style="width:27px;height:240.8px;background:#1e4d3d"><a href="/books/the-discovery-of-freedom/" title="The Discovery of Freedom" style="max-height:228.8px">The Discovery of Freedom</a></div>
<div class="bk-spine" data-genre="philosophy" data-w="27" style="width:27px;height:225.7px;background:#1e4d3d"><a href="/books/the-god-of-the-machine/" title="The God of the Machine" style="max-height:213.7px">The God of the Machine</a></div>
<div class="bk-spine" data-genre="philosophy" data-w="27" style="width:27px;height:233.8px;background:#1e4d3d"><a href="/books/the-ominous-parallels/" title="The Ominous Parallels" style="max-height:221.8px"><strong>The Ominous Parallels</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="philosophy" data-w="36" style="width:36px;height:267.2px;background:#1e4d3d"><a href="/books/opar/" title="OPAR (Objectivism: The Philosophy of Ayn Rand)" style="max-height:255.2px">OPAR</a></div>
<div class="bk-spine" data-genre="philosophy" data-w="27" style="width:27px;height:217.0px;background:#1e4d3d"><a href="/books/introduction-to-objectivist-epistemology/" title="Introduction to Objectivist Epistemology" style="max-height:205.0px"><strong>ITOE</strong></a></div>
<div class="bk-spine" data-genre="philfic" data-w="20" style="width:20px;height:187.0px;background:#2f6b4f"><a href="/books/anthem/" title="Anthem" style="max-height:175.0px">Anthem &#9733;</a></div>
<div class="bk-spine" data-genre="philfic" data-w="36" style="width:36px;height:249.0px;background:#2f6b4f"><a href="/books/atlas-shrugged/" title="Atlas Shrugged" style="max-height:237.0px"><strong>Atlas Shrugged</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="philfic" data-w="36" style="width:36px;height:249.0px;background:#2f6b4f"><a href="/books/the-fountainhead/" title="The Fountainhead" style="max-height:237.0px"><strong>The Fountainhead</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="philfic" data-w="27" style="width:27px;height:217.0px;background:#2f6b4f"><a href="/books/ideal/" title="Ideal" style="max-height:205.0px">Ideal &#9733;</a></div>
<div class="bk-spine" data-genre="philfic" data-w="27" style="width:27px;height:217.0px;background:#2f6b4f"><a href="/books/we-the-living/" title="We the Living" style="max-height:205.0px"><strong>We the Living</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:232.7px;background:#6e5133"><a href="/books/chains/" title="Chains" style="max-height:220.7px">Chains</a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:223.5px;background:#6e5133"><a href="/books/airman/" title="Airman" style="max-height:211.5px"><strong>Airman</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:219.2px;background:#6e5133"><a href="/books/bud-not-buddy/" title="Bud, Not Buddy" style="max-height:207.2px">Bud, Not Buddy</a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:219.2px;background:#6e5133"><a href="/books/elijah-of-buxton/" title="Elijah of Buxton" style="max-height:207.2px"><strong>Elijah of Buxton</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:221.3px;background:#6e5133"><a href="/books/robinson-crusoe/" title="Robinson Crusoe" style="max-height:209.3px">Robinson Crusoe</a></div>
<div class="bk-spine" data-genre="classics" data-w="20" style="width:20px;height:203.2px;background:#6e5133"><a href="/books/the-fall-line/" title="The Fall Line" style="max-height:191.2px"><strong>The Fall Line</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:243.0px;background:#6e5133"><a href="/books/alabama-moon/" title="Alabama Moon (Alabama Moon, #1)" style="max-height:231.0px"><strong>Alabama Moon</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:223.0px;background:#6e5133"><a href="/books/the-green-glass-sea/" title="The Green Glass Sea (Green Glass, #1)" style="max-height:211.0px"><strong>The Green Glass Sea</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:225.1px;background:#6e5133"><a href="/books/to-kill-a-mockingbird/" title="To Kill a Mockingbird" style="max-height:213.1px"><strong>To Kill a Mockingbird</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:219.7px;background:#6e5133"><a href="/books/all-the-pretty-horses/" title="All the Pretty Horses (The Border Trilogy, #1)" style="max-height:207.7px"><strong>All the Pretty Horses</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="classics" data-w="20" style="width:20px;height:202.2px;background:#6e5133"><a href="/books/a-single-shard/" title="A Single Shard" style="max-height:190.2px"><strong>A Single Shard</strong></a></div>
<div class="bk-spine bk-coll" data-coll="brians-saga" data-genre="classics" data-w="43" style="width:43px;height:236.0px;background:#6e5133" title="Hatchet series"><span class="bk-coll-name"><strong>Hatchet series</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="classics" data-w="27" data-volof="brians-saga" style="width:27px;height:224.0px;background:#6e5133"><a href="/books/hatchet/" title="Hatchet" style="max-height:212.0px"><strong>Hatchet</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="20" data-volof="brians-saga" style="width:20px;height:196.8px;background:#6e5133"><a href="/books/the-river/" title="The River" style="max-height:184.8px">The River</a></div>
<div class="bk-spine" data-genre="classics" data-w="20" data-volof="brians-saga" style="width:20px;height:196.8px;background:#6e5133"><a href="/books/brians-winter/" title="Brian&#x27;s Winter" style="max-height:184.8px">Brian&#x27;s Winter</a></div>
<div class="bk-spine" data-genre="classics" data-w="20" data-volof="brians-saga" style="width:20px;height:196.8px;background:#6e5133"><a href="/books/brians-return/" title="Brian&#x27;s Return" style="max-height:184.8px">Brian&#x27;s Return</a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:234.9px;background:#6e5133"><a href="/books/holes/" title="Holes" style="max-height:222.9px"><strong>Holes</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:240.3px;background:#6e5133"><a href="/books/kidnapped/" title="Kidnapped" style="max-height:228.3px">Kidnapped</a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:229.5px;background:#6e5133"><a href="/books/gullivers-travels/" title="Gulliver&#x27;s Travels" style="max-height:217.5px">Gulliver&#x27;s Travels</a></div>
<div class="bk-spine bk-long" data-genre="classics" data-w="27" style="width:27px;height:236.5px;background:#6e5133"><a href="/books/the-adventures-of-huckleberry-finn/" title="The Adventures of Huckleberry Finn" style="max-height:224.5px">The Adventures of Huckleberry Finn &#9733;</a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:236.5px;background:#6e5133"><a href="/books/the-adventures-of-tom-sawyer/" title="The Adventures of Tom Sawyer" style="max-height:224.5px"><strong>The Adventures of Tom Sawyer</strong></a></div>
<div class="bk-spine" data-genre="classics" data-w="27" style="width:27px;height:228.4px;background:#6e5133"><a href="/books/the-swiss-family-robinson/" title="The Swiss Family Robinson" style="max-height:216.4px">The Swiss Family Robinson</a></div>
<div class="bk-spine bk-coll" data-coll="hitchhikers-guide" data-genre="scifi" data-w="43" style="width:43px;height:235.5px;background:#1f4e5f" title="DON&#x27;T PANIC"><span class="bk-coll-name"><strong>DON&#x27;T PANIC</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="scifi" data-w="27" data-volof="hitchhikers-guide" style="width:27px;height:222.4px;background:#1f4e5f"><a href="/books/the-hitchhikers-guide-to-the-galaxy/" title="The Hitchhiker&#x27;s Guide to the Galaxy (The Hitchhiker&#x27;s Guide to the Galaxy, #1)" style="max-height:210.4px"><strong>DON&#x27;T PANIC</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="27" data-volof="hitchhikers-guide" style="width:27px;height:222.4px;background:#1f4e5f"><a href="/books/the-restaurant-at-the-end-of-the-universe/" title="The Restaurant at the End of the Universe (The Hitchhiker&#x27;s Guide to the Galaxy, #2)" style="max-height:210.4px"><strong>TRATEOTU</strong></a></div>
<div class="bk-spine bk-long" data-genre="scifi" data-w="27" data-volof="hitchhikers-guide" style="width:27px;height:222.4px;background:#1f4e5f"><a href="/books/life-the-universe-and-everything/" title="Life, the Universe and Everything (The Hitchhiker&#x27;s Guide to the Galaxy, #3)" style="max-height:210.4px"><strong>Life, the Universe and Everything</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="20" data-volof="hitchhikers-guide" style="width:20px;height:191.3px;background:#1f4e5f"><a href="/books/so-long-and-thanks-for-all-the-fish/" title="So Long, and Thanks for All the Fish (The Hitchhiker&#x27;s Guide to the Galaxy, #4)" style="max-height:179.3px"><strong>SLATFATF</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="27" data-volof="hitchhikers-guide" style="width:27px;height:222.4px;background:#1f4e5f"><a href="/books/mostly-harmless/" title="Mostly Harmless (Hitchhiker&#x27;s Guide to the Galaxy, #5)" style="max-height:210.4px"><strong>Mostly Harmless</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="27" data-volof="hitchhikers-guide" style="width:27px;height:223.5px;background:#1f4e5f"><a href="/books/and-another-thing/" title="And Another Thing... (The Hitchhiker&#x27;s Guide to the Galaxy, #6)" style="max-height:211.5px"><strong>And Another Thing...</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="27" style="width:27px;height:237.6px;background:#1f4e5f"><a href="/books/enders-game/" title="Ender&#x27;s Game (Ender&#x27;s Saga, #1)" style="max-height:225.6px"><strong>Ender&#x27;s Game</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="27" style="width:27px;height:241.4px;background:#1f4e5f"><a href="/books/leviathan/" title="Leviathan (Leviathan, #1)" style="max-height:229.4px"><strong>Leviathan</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="36" style="width:36px;height:272.4px;background:#1f4e5f"><a href="/books/behemoth/" title="Behemoth (Leviathan, #2)" style="max-height:260.4px"><strong>Behemoth</strong></a></div>
<div class="bk-spine" data-genre="scifi" data-w="36" style="width:36px;height:272.4px;background:#1f4e5f"><a href="/books/goliath/" title="Goliath (Leviathan, #3)" style="max-height:260.4px"><strong>Goliath</strong></a></div>
<div class="bk-spine bk-coll" data-coll="inheritance" data-genre="fantasy" data-w="43" style="width:43px;height:271.4px;background:#9a5c26" title="The Inheritance Cycle"><span class="bk-coll-name"><strong>The Inheritance Cycle</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="inheritance" style="width:36px;height:259.4px;background:#9a5c26"><a href="/books/eragon/" title="Eragon (Inheritance, #1)" style="max-height:247.39999999999998px">Eragon</a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="inheritance" style="width:36px;height:259.4px;background:#9a5c26"><a href="/books/eldest/" title="Eldest (Inheritance, #2)" style="max-height:247.39999999999998px"><strong>Eldest</strong></a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="inheritance" style="width:36px;height:259.4px;background:#9a5c26"><a href="/books/brisingr/" title="Brisingr (Inheritance, #3)" style="max-height:247.39999999999998px"><strong>Brisingr</strong></a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="inheritance" style="width:36px;height:259.4px;background:#9a5c26"><a href="/books/inheritance/" title="Inheritance (Inheritance, #4)" style="max-height:247.39999999999998px">Inheritance</a></div>
<div class="bk-spine" data-genre="fantasy" data-w="27" style="width:27px;height:241.9px;background:#9a5c26"><a href="/books/nation/" title="Nation" style="max-height:229.9px"><strong>Nation</strong></a></div>
<div class="bk-spine bk-coll" data-coll="heroes-of-olympus" data-genre="fantasy" data-w="43" style="width:43px;height:281.8px;background:#9a5c26" title="The Heroes of Olympus"><span class="bk-coll-name"><strong>The Heroes of Olympus</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="heroes-of-olympus" style="width:36px;height:269.8px;background:#9a5c26"><a href="/books/the-lost-hero/" title="The Lost Hero (The Heroes of Olympus, #1)" style="max-height:257.8px">The Lost Hero</a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="heroes-of-olympus" style="width:36px;height:269.8px;background:#9a5c26"><a href="/books/the-son-of-neptune/" title="The Son of Neptune (The Heroes of Olympus, #2)" style="max-height:257.8px"><strong>The Son of Neptune</strong></a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="heroes-of-olympus" style="width:36px;height:269.8px;background:#9a5c26"><a href="/books/the-mark-of-athena/" title="The Mark of Athena (The Heroes of Olympus, #3)" style="max-height:257.8px">The Mark of Athena</a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="heroes-of-olympus" style="width:36px;height:269.8px;background:#9a5c26"><a href="/books/the-house-of-hades/" title="The House of Hades (The Heroes of Olympus, #4)" style="max-height:257.8px"><strong>The House of Hades</strong></a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" data-volof="heroes-of-olympus" style="width:36px;height:269.8px;background:#9a5c26"><a href="/books/the-blood-of-olympus/" title="The Blood of Olympus (The Heroes of Olympus, #5)" style="max-height:257.8px">The Blood of Olympus</a></div>
<div class="bk-spine" data-genre="fantasy" data-w="36" style="width:36px;height:256.8px;background:#9a5c26"><a href="/books/mistborn-the-final-empire/" title="Mistborn: The Final Empire" style="max-height:244.8px">Mistborn &#9733;</a></div>
<div class="bk-spine" data-genre="fantasy" data-w="27" style="width:27px;height:226.8px;background:#9a5c26"><a href="/books/the-fellowship-of-the-ring/" title="The Fellowship of the Ring" style="max-height:214.8px">The Fellowship of the Ring</a></div>
<div class="bk-spine" data-genre="fantasy" data-w="27" style="width:27px;height:226.8px;background:#9a5c26"><a href="/books/the-hobbit/" title="The Hobbit" style="max-height:214.8px">The Hobbit</a></div>
<div class="bk-spine" data-genre="dystopian" data-w="27" style="width:27px;height:218.1px;background:#b45a1b"><a href="/books/rootless/" title="Rootless (Rootless, #1)" style="max-height:206.1px"><strong>Rootless</strong></a></div>
<div class="bk-spine" data-genre="dystopian" data-w="27" style="width:27px;height:236.0px;background:#b45a1b"><a href="/books/legend/" title="Legend (Legend, #1)" style="max-height:224.0px">Legend</a></div>
<div class="bk-spine" data-genre="thriller" data-w="27" style="width:27px;height:220.8px;background:#26221e"><a href="/books/i-am-justice/" title="I Am Justice" style="max-height:208.8px">I Am Justice &#9733;</a></div>
<div class="bk-divider" id="bk-divider" data-w="48" title="All The Children's Books: click to show or hide" style="width:48px"><span>All The Children's Books</span><span class="bk-divider-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:209.8px;background:#67782a"><a href="/books/mr-poppers-penguins/" title="Mr. Popper&#x27;s Penguins" style="max-height:197.8px">Mr. Popper&#x27;s Penguins</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:231.1px;background:#67782a"><a href="/books/double-fudge/" title="Double Fudge" style="max-height:219.1px">Double Fudge</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:238.1px;background:#67782a"><a href="/books/trackers/" title="Trackers" style="max-height:226.1px">Trackers</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:238.1px;background:#67782a"><a href="/books/trackers-shantorian/" title="Trackers: Shantorian" style="max-height:226.1px">Trackers</a></div>
<div class="bk-spine bk-coll" data-coll="the-39-clues" data-genre="children" data-w="43" style="width:43px;height:251.2px;background:#67782a" title="The 39 Clues"><span class="bk-coll-name"><strong>The 39 Clues</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:239.2px;background:#67782a"><a href="/books/the-maze-of-bones/" title="The Maze of Bones" style="max-height:227.2px"><strong>The Maze of Bones</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="the-39-clues" style="width:20px;height:197.8px;background:#67782a"><a href="/books/one-false-note/" title="One False Note" style="max-height:185.8px"><strong>One False Note</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:238.7px;background:#67782a"><a href="/books/the-sword-thief/" title="The Sword Thief" style="max-height:226.7px"><strong>The Sword Thief</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="the-39-clues" style="width:20px;height:200.0px;background:#67782a"><a href="/books/beyond-the-grave/" title="Beyond the Grave" style="max-height:188.0px"><strong>Beyond the Grave</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:238.1px;background:#67782a"><a href="/books/the-black-circle/" title="The Black Circle" style="max-height:226.1px"><strong>The Black Circle</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:230.5px;background:#67782a"><a href="/books/in-too-deep/" title="In Too Deep" style="max-height:218.5px"><strong>In Too Deep</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:238.7px;background:#67782a"><a href="/books/the-vipers-nest/" title="The Viper&#x27;s Nest" style="max-height:226.7px"><strong>The Viper&#x27;s Nest</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:224.6px;background:#67782a"><a href="/books/the-emperors-code/" title="The Emperor&#x27;s Code" style="max-height:212.6px"><strong>The Emperor&#x27;s Code</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:234.3px;background:#67782a"><a href="/books/storm-warning/" title="Storm Warning" style="max-height:222.3px"><strong>Storm Warning</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-39-clues" style="width:27px;height:235.4px;background:#67782a"><a href="/books/into-the-gauntlet/" title="Into the Gauntlet" style="max-height:223.4px"><strong>Into the Gauntlet</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:193.5px;background:#67782a"><a href="/books/the-artemis-fowl-files/" title="The Artemis Fowl Files" style="max-height:181.5px"><strong>The Artemis Fowl Files</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:223.5px;background:#67782a"><a href="/books/half-moon-investigations/" title="Half Moon Investigations" style="max-height:211.5px">Half Moon Investigations</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:223.5px;background:#67782a"><a href="/books/the-supernaturalist/" title="The Supernaturalist" style="max-height:211.5px">The Supernaturalist</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:223.5px;background:#67782a"><a href="/books/the-wish-list/" title="The Wish List" style="max-height:211.5px">The Wish List</a></div>
<div class="bk-spine bk-coll" data-coll="artemis-fowl" data-genre="children" data-w="43" style="width:43px;height:235.5px;background:#67782a" title="Artemis Fowl"><span class="bk-coll-name"><strong>Artemis Fowl</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl/" title="Artemis Fowl" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl-the-arctic-incident/" title="Artemis Fowl: The Arctic Incident" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl-the-eternity-code/" title="Artemis Fowl: The Eternity Code" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl-the-opal-deception/" title="Artemis Fowl: The Opal Deception" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl-the-lost-colony/" title="Artemis Fowl: The Lost Colony" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl-the-time-paradox/" title="Artemis Fowl: The Time Paradox" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl-the-atlantis-complex/" title="Artemis Fowl: The Atlantis Complex" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="artemis-fowl" style="width:27px;height:223.5px;background:#67782a"><a href="/books/artemis-fowl-the-last-guardian/" title="Artemis Fowl: The Last Guardian" style="max-height:211.5px"><strong>Artemis Fowl</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:210.8px;background:#67782a"><a href="/books/georges-marvelous-medicine/" title="George&#x27;s Marvelous Medicine" style="max-height:198.8px">George&#x27;s Marvelous Medicine</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:231.6px;background:#67782a"><a href="/books/the-tale-of-despereaux/" title="The Tale of Despereaux" style="max-height:219.6px">The Tale of Despereaux</a></div>
<div class="bk-spine bk-coll" data-coll="the-hardy-boys" data-genre="children" data-w="43" style="width:43px;height:206.6px;background:#67782a" title="The Hardy Boys"><span class="bk-coll-name">The Hardy Boys &#9733;</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="the-hardy-boys" style="width:20px;height:194.6px;background:#67782a"><a href="/books/the-tower-treasure/" title="The Tower Treasure" style="max-height:182.6px">The Tower Treasure &#9733;</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="the-hardy-boys" style="width:20px;height:194.6px;background:#67782a"><a href="/books/the-house-on-the-cliff/" title="The House on the Cliff" style="max-height:182.6px">The House on the Cliff</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="the-hardy-boys" style="width:20px;height:194.6px;background:#67782a"><a href="/books/hunting-for-hidden-gold/" title="Hunting for Hidden Gold" style="max-height:182.6px">Hunting for Hidden Gold</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="the-hardy-boys" style="width:20px;height:194.6px;background:#67782a"><a href="/books/the-secret-of-the-lost-tunnel/" title="The Secret of the Lost Tunnel" style="max-height:182.6px">The Secret of the Lost Tunnel</a></div>
<div class="bk-spine bk-coll" data-coll="book-of-ember" data-genre="children" data-w="43" style="width:43px;height:239.3px;background:#67782a" title="Book of Ember"><span class="bk-coll-name"><strong>Book of Ember</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="book-of-ember" style="width:27px;height:227.3px;background:#67782a"><a href="/books/the-city-of-ember/" title="The City of Ember (Book of Ember, #1)" style="max-height:215.3px"><strong>The City of Ember</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="book-of-ember" style="width:27px;height:227.3px;background:#67782a"><a href="/books/the-people-of-sparks/" title="The People of Sparks (The City of Ember #2)" style="max-height:215.3px"><strong>The People of Sparks</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="book-of-ember" style="width:27px;height:227.3px;background:#67782a"><a href="/books/the-prophet-of-yonwood/" title="The Prophet of Yonwood (Book of Ember, #3)" style="max-height:215.3px"><strong>The Prophet of Yonwood</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="book-of-ember" style="width:27px;height:227.3px;background:#67782a"><a href="/books/the-diamond-of-darkhold/" title="The Diamond of Darkhold (Book of Ember, #4)" style="max-height:215.3px"><strong>The Diamond of Darkhold</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:206.5px;background:#67782a"><a href="/books/westward-home-joshuas-diary/" title="Westward Home: Joshua&#x27;s Diary" style="max-height:194.5px"><strong>Westward Home</strong></a></div>
<div class="bk-spine bk-coll" data-coll="diary-of-a-wimpy-kid" data-genre="children" data-w="43" style="width:43px;height:239.8px;background:#67782a" title="Diary of a Wimpy Kid"><span class="bk-coll-name">Diary of a Wimpy Kid</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="diary-of-a-wimpy-kid" style="width:27px;height:227.8px;background:#67782a"><a href="/books/diary-of-a-wimpy-kid/" title="Diary of a Wimpy Kid" style="max-height:215.8px">Diary of a Wimpy Kid</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="diary-of-a-wimpy-kid" style="width:27px;height:227.8px;background:#67782a"><a href="/books/diary-of-a-wimpy-kid-rodrick-rules/" title="Diary of a Wimpy Kid: Rodrick Rules" style="max-height:215.8px">Diary of a Wimpy Kid</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="diary-of-a-wimpy-kid" style="width:27px;height:227.8px;background:#67782a"><a href="/books/diary-of-a-wimpy-kid-the-last-straw/" title="Diary of a Wimpy Kid: The Last Straw" style="max-height:215.8px">Diary of a Wimpy Kid</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="diary-of-a-wimpy-kid" style="width:27px;height:227.8px;background:#67782a"><a href="/books/diary-of-a-wimpy-kid-dog-days/" title="Diary of a Wimpy Kid: Dog Days" style="max-height:215.8px">Diary of a Wimpy Kid</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="diary-of-a-wimpy-kid" style="width:27px;height:227.8px;background:#67782a"><a href="/books/diary-of-a-wimpy-kid-the-ugly-truth/" title="Diary of a Wimpy Kid: The Ugly Truth" style="max-height:215.8px">Diary of a Wimpy Kid</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="diary-of-a-wimpy-kid" style="width:27px;height:227.8px;background:#67782a"><a href="/books/diary-of-a-wimpy-kid-cabin-fever/" title="Diary of a Wimpy Kid: Cabin Fever" style="max-height:215.8px">Diary of a Wimpy Kid</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="diary-of-a-wimpy-kid" style="width:27px;height:227.8px;background:#67782a"><a href="/books/diary-of-a-wimpy-kid-the-third-wheel/" title="Diary of a Wimpy Kid: The Third Wheel" style="max-height:215.8px">Diary of a Wimpy Kid</a></div>
<div class="bk-spine bk-coll" data-coll="the-chronicles-of-narnia" data-genre="children" data-w="43" style="width:43px;height:229.5px;background:#67782a" title="The Chronicles of Narnia"><span class="bk-coll-name"><strong>The Chronicles of Narnia</strong></span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine bk-long" data-genre="children" data-w="27" data-volof="the-chronicles-of-narnia" style="width:27px;height:217.5px;background:#67782a"><a href="/books/the-lion-the-witch-and-the-wardrobe/" title="The Lion, the Witch and the Wardrobe" style="max-height:205.5px">The Lion, the Witch and the Wardrobe</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-chronicles-of-narnia" style="width:27px;height:217.5px;background:#67782a"><a href="/books/prince-caspian/" title="Prince Caspian" style="max-height:205.5px">Prince Caspian</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-chronicles-of-narnia" style="width:27px;height:217.5px;background:#67782a"><a href="/books/the-voyage-of-the-dawn-treader/" title="The Voyage of the Dawn Treader" style="max-height:205.5px">The Voyage of the Dawn Treader</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-chronicles-of-narnia" style="width:27px;height:217.5px;background:#67782a"><a href="/books/the-silver-chair/" title="The Silver Chair" style="max-height:205.5px">The Silver Chair</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-chronicles-of-narnia" style="width:27px;height:217.5px;background:#67782a"><a href="/books/the-horse-and-his-boy/" title="The Horse and His Boy" style="max-height:205.5px">The Horse and His Boy</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="the-chronicles-of-narnia" style="width:20px;height:189.2px;background:#67782a"><a href="/books/the-magicians-nephew/" title="The Magician&#x27;s Nephew (Chronicles of Narnia, #6)" style="max-height:177.2px"><strong>The Magician&#x27;s Nephew</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="the-chronicles-of-narnia" style="width:27px;height:217.5px;background:#67782a"><a href="/books/the-last-battle/" title="The Last Battle" style="max-height:205.5px">The Last Battle</a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:207.6px;background:#67782a"><a href="/books/shiloh/" title="Shiloh (Shiloh, #1)" style="max-height:195.6px"><strong>Shiloh</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:207.6px;background:#67782a"><a href="/books/shiloh-season/" title="Shiloh Season (Shiloh, #2)" style="max-height:195.6px"><strong>Shiloh Season</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:207.6px;background:#67782a"><a href="/books/saving-shiloh/" title="Saving Shiloh (Shiloh, #3)" style="max-height:195.6px"><strong>Saving Shiloh</strong></a></div>
<div class="bk-spine bk-coll" data-coll="magic-tree-house" data-genre="children" data-w="43" style="width:43px;height:217.4px;background:#67782a" title="Magic Tree House"><span class="bk-coll-name">Magic Tree House</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/dinosaurs-before-dark/" title="Dinosaurs Before Dark" style="max-height:193.4px">Dinosaurs Before Dark</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/the-knight-at-dawn/" title="The Knight at Dawn" style="max-height:193.4px">The Knight at Dawn</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/mummies-in-the-morning/" title="Mummies in the Morning" style="max-height:193.4px">Mummies in the Morning</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/pirates-past-noon/" title="Pirates Past Noon" style="max-height:193.4px">Pirates Past Noon</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/night-of-the-ninjas/" title="Night of the Ninjas" style="max-height:193.4px">Night of the Ninjas</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/afternoon-on-the-amazon/" title="Afternoon on the Amazon" style="max-height:193.4px">Afternoon on the Amazon</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/sunset-of-the-sabertooth/" title="Sunset of the Sabertooth" style="max-height:193.4px">Sunset of the Sabertooth</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/midnight-on-the-moon/" title="Midnight on the Moon" style="max-height:193.4px">Midnight on the Moon</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/dolphins-at-daybreak/" title="Dolphins at Daybreak" style="max-height:193.4px">Dolphins at Daybreak</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/ghost-town-at-sundown/" title="Ghost Town at Sundown" style="max-height:193.4px">Ghost Town at Sundown</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/lions-at-lunchtime/" title="Lions at Lunchtime" style="max-height:193.4px">Lions at Lunchtime</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/polar-bears-past-bedtime/" title="Polar Bears Past Bedtime" style="max-height:193.4px">Polar Bears Past Bedtime</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/vacation-under-the-volcano/" title="Vacation Under the Volcano" style="max-height:193.4px">Vacation Under the Volcano</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/day-of-the-dragon-king/" title="Day of the Dragon King" style="max-height:193.4px">Day of the Dragon King</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/viking-ships-at-sunrise/" title="Viking Ships at Sunrise" style="max-height:193.4px">Viking Ships at Sunrise</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/hour-of-the-olympics/" title="Hour of the Olympics" style="max-height:193.4px">Hour of the Olympics</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/tonight-on-the-titanic/" title="Tonight on the Titanic" style="max-height:193.4px">Tonight on the Titanic</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/buffalo-before-breakfast/" title="Buffalo Before Breakfast" style="max-height:193.4px">Buffalo Before Breakfast</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/tigers-at-twilight/" title="Tigers at Twilight" style="max-height:193.4px">Tigers at Twilight</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/dingoes-at-dinnertime/" title="Dingoes at Dinnertime" style="max-height:193.4px">Dingoes at Dinnertime</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/civil-war-on-sunday/" title="Civil War on Sunday" style="max-height:193.4px">Civil War on Sunday</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/revolutionary-war-on-wednesday/" title="Revolutionary War on Wednesday" style="max-height:193.4px">Rev. War on Wednesday</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/twister-on-tuesday/" title="Twister on Tuesday" style="max-height:193.4px">Twister on Tuesday</a></div>
<div class="bk-spine bk-long" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/earthquake-in-the-early-morning/" title="Earthquake in the Early Morning" style="max-height:193.4px">Earthquake in the Early Morning</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/stage-fright-on-a-summer-night/" title="Stage Fright on a Summer Night" style="max-height:193.4px">Stage Fright on a Summer Night</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/good-morning-gorillas/" title="Good Morning, Gorillas" style="max-height:193.4px">Good Morning, Gorillas</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/thanksgiving-on-thursday/" title="Thanksgiving on Thursday" style="max-height:193.4px">Thanksgiving on Thursday</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/high-tide-in-hawaii/" title="High Tide in Hawaii" style="max-height:193.4px">High Tide in Hawaii</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/christmas-in-camelot/" title="Christmas in Camelot" style="max-height:193.4px">Christmas in Camelot</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/haunted-castle-on-hallows-eve/" title="Haunted Castle on Hallows Eve" style="max-height:193.4px">Haunted Castle on Hallows Eve</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/summer-of-the-sea-serpent/" title="Summer of the Sea Serpent" style="max-height:193.4px">Summer of the Sea Serpent</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/winter-of-the-ice-wizard/" title="Winter of the Ice Wizard" style="max-height:193.4px">Winter of the Ice Wizard</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/carnival-at-candlelight/" title="Carnival at Candlelight" style="max-height:193.4px">Carnival at Candlelight</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/season-of-the-sandstorms/" title="Season of the Sandstorms" style="max-height:193.4px">Season of the Sandstorms</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/night-of-the-new-magicians/" title="Night of the New Magicians" style="max-height:193.4px">Night of the New Magicians</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/blizzard-of-the-blue-moon/" title="Blizzard of the Blue Moon" style="max-height:193.4px">Blizzard of the Blue Moon</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="magic-tree-house" style="width:20px;height:205.4px;background:#67782a"><a href="/books/dragon-of-the-red-dawn/" title="Dragon of the Red Dawn" style="max-height:193.4px">Dragon of the Red Dawn</a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:213.0px;background:#67782a"><a href="/books/the-higher-power-of-lucky/" title="The Higher Power of Lucky (The Hard Pan Trilogy, #1)" style="max-height:201.0px"><strong>The Higher Power of Lucky</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:213.0px;background:#67782a"><a href="/books/lucky-breaks/" title="Lucky Breaks (The Hard Pan Trilogy, #2)" style="max-height:201.0px"><strong>Lucky Breaks</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:196.8px;background:#67782a"><a href="/books/masters-of-disaster/" title="Masters of Disaster" style="max-height:184.8px">Masters of Disaster</a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:196.8px;background:#67782a"><a href="/books/the-voyage-of-the-frog/" title="The Voyage of the Frog" style="max-height:184.8px"><strong>The Voyage of the Frog</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:239.8px;background:#67782a"><a href="/books/steel-trapp/" title="Steel Trapp" style="max-height:227.8px">Steel Trapp</a></div>
<div class="bk-spine bk-coll" data-coll="addy" data-genre="children" data-w="43" style="width:43px;height:202.2px;background:#67782a" title="American Girl: Addy"><span class="bk-coll-name">American Girl: Addy</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="addy" style="width:20px;height:190.2px;background:#67782a"><a href="/books/meet-addy/" title="Meet Addy" style="max-height:178.2px">Meet Addy</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="addy" style="width:20px;height:190.2px;background:#67782a"><a href="/books/addy-learns-a-lesson/" title="Addy Learns a Lesson" style="max-height:178.2px">Addy Learns a Lesson</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="addy" style="width:20px;height:190.2px;background:#67782a"><a href="/books/addys-surprise/" title="Addy&#x27;s Surprise" style="max-height:178.2px">Addy&#x27;s Surprise</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="addy" style="width:20px;height:190.2px;background:#67782a"><a href="/books/happy-birthday-addy/" title="Happy Birthday, Addy!" style="max-height:178.2px">Happy Birthday, Addy!</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="addy" style="width:20px;height:190.2px;background:#67782a"><a href="/books/addy-saves-the-day/" title="Addy Saves the Day" style="max-height:178.2px">Addy Saves the Day</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="addy" style="width:20px;height:190.2px;background:#67782a"><a href="/books/changes-for-addy/" title="Changes for Addy" style="max-height:178.2px">Changes for Addy</a></div>
<div class="bk-spine" data-genre="children" data-w="20" style="width:20px;height:192.4px;background:#67782a"><a href="/books/the-westing-game/" title="The Westing Game" style="max-height:180.4px"><strong>The Westing Game</strong></a></div>
<div class="bk-spine bk-coll bk-long" data-coll="percy-jackson" data-genre="children" data-w="43" style="width:43px;height:251.2px;background:#67782a" title="Percy Jackson and the Olympians"><span class="bk-coll-name">Percy Jackson and the Olympians</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="percy-jackson" style="width:27px;height:239.2px;background:#67782a"><a href="/books/the-lightning-thief/" title="The Lightning Thief (Percy Jackson and the Olympians, #1)" style="max-height:227.2px">The Lightning Thief</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="percy-jackson" style="width:27px;height:239.2px;background:#67782a"><a href="/books/the-sea-of-monsters/" title="The Sea of Monsters (Percy Jackson and the Olympians, #2)" style="max-height:227.2px">The Sea of Monsters</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="percy-jackson" style="width:27px;height:239.2px;background:#67782a"><a href="/books/the-titans-curse/" title="The Titan&#x27;s Curse (Percy Jackson and the Olympians, #3)" style="max-height:227.2px">The Titan&#x27;s Curse</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="percy-jackson" style="width:27px;height:239.2px;background:#67782a"><a href="/books/the-battle-of-the-labyrinth/" title="The Battle of the Labyrinth (Percy Jackson and the Olympians, #4)" style="max-height:227.2px">The Battle of the Labyrinth</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="percy-jackson" style="width:27px;height:239.2px;background:#67782a"><a href="/books/the-last-olympian/" title="The Last Olympian (Percy Jackson and the Olympians, #5)" style="max-height:227.2px">The Last Olympian</a></div>
<div class="bk-spine bk-coll" data-coll="harry-potter" data-genre="children" data-w="43" style="width:43px;height:274.0px;background:#67782a" title="Harry Potter"><span class="bk-coll-name">Harry Potter</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="harry-potter" style="width:27px;height:226.2px;background:#67782a"><a href="/books/harry-potter-and-the-sorcerers-stone/" title="Harry Potter and the Sorcerer&#x27;s Stone (Harry Potter, #1)" style="max-height:214.2px">Sorcerer&#x27;s Stone</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="harry-potter" style="width:27px;height:226.2px;background:#67782a"><a href="/books/harry-potter-and-the-chamber-of-secrets/" title="Harry Potter and the Chamber of Secrets (Harry Potter, #2)" style="max-height:214.2px">Chamber of Secrets</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="harry-potter" style="width:27px;height:226.2px;background:#67782a"><a href="/books/harry-potter-and-the-prisoner-of-azkaban/" title="Harry Potter and the Prisoner of Azkaban (Harry Potter, #3)" style="max-height:214.2px">Prisoner of Azkaban</a></div>
<div class="bk-spine" data-genre="children" data-w="36" data-volof="harry-potter" style="width:36px;height:262.0px;background:#67782a"><a href="/books/harry-potter-and-the-goblet-of-fire/" title="Harry Potter and the Goblet of Fire (Harry Potter, #4)" style="max-height:250.0px">Goblet of Fire</a></div>
<div class="bk-spine" data-genre="children" data-w="36" data-volof="harry-potter" style="width:36px;height:262.0px;background:#67782a"><a href="/books/harry-potter-and-the-order-of-the-phoenix/" title="Harry Potter and the Order of the Phoenix (Harry Potter, #5)" style="max-height:250.0px">Order of the Phoenix</a></div>
<div class="bk-spine" data-genre="children" data-w="36" data-volof="harry-potter" style="width:36px;height:262.0px;background:#67782a"><a href="/books/harry-potter-and-the-half-blood-prince/" title="Harry Potter and the Half-Blood Prince (Harry Potter, #6)" style="max-height:250.0px">Half-Blood Prince</a></div>
<div class="bk-spine" data-genre="children" data-w="36" data-volof="harry-potter" style="width:36px;height:262.0px;background:#67782a"><a href="/books/harry-potter-and-the-deathly-hallows/" title="Harry Potter and the Deathly Hallows (Harry Potter, #7)" style="max-height:250.0px">Deathly Hallows</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:230.0px;background:#67782a"><a href="/books/reality-leak/" title="Reality Leak" style="max-height:218.0px">Reality Leak</a></div>
<div class="bk-spine bk-coll bk-long" data-coll="a-series-of-unfortunate-events" data-genre="children" data-w="43" style="width:43px;height:245.2px;background:#67782a" title="A Series of Unfortunate Events"><span class="bk-coll-name">A Series of Unfortunate Events</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="a-series-of-unfortunate-events" style="width:20px;height:201.1px;background:#67782a"><a href="/books/the-bad-beginning/" title="The Bad Beginning" style="max-height:189.1px">The Bad Beginning</a></div>
<div class="bk-spine" data-genre="children" data-w="20" data-volof="a-series-of-unfortunate-events" style="width:20px;height:201.1px;background:#67782a"><a href="/books/the-reptile-room/" title="The Reptile Room" style="max-height:189.1px">The Reptile Room</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-wide-window/" title="The Wide Window" style="max-height:221.2px">The Wide Window</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-miserable-mill/" title="The Miserable Mill" style="max-height:221.2px">The Miserable Mill</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-austere-academy/" title="The Austere Academy" style="max-height:221.2px">The Austere Academy</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-ersatz-elevator/" title="The Ersatz Elevator" style="max-height:221.2px">The Ersatz Elevator</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-vile-village/" title="The Vile Village" style="max-height:221.2px">The Vile Village</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-hostile-hospital/" title="The Hostile Hospital" style="max-height:221.2px">The Hostile Hospital</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-carnivorous-carnival/" title="The Carnivorous Carnival" style="max-height:221.2px">The Carnivorous Carnival</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-slippery-slope/" title="The Slippery Slope" style="max-height:221.2px">The Slippery Slope</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-grim-grotto/" title="The Grim Grotto" style="max-height:221.2px">The Grim Grotto</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-penultimate-peril/" title="The Penultimate Peril" style="max-height:221.2px">The Penultimate Peril</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="a-series-of-unfortunate-events" style="width:27px;height:233.2px;background:#67782a"><a href="/books/the-end/" title="The End" style="max-height:221.2px">The End</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:220.2px;background:#67782a"><a href="/books/a-whole-nother-story/" title="A Whole Nother Story" style="max-height:208.2px">A Whole Nother Story</a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:220.2px;background:#67782a"><a href="/books/another-whole-nother-story/" title="Another Whole Nother Story" style="max-height:208.2px">Another Whole Nother Story</a></div>
<div class="bk-spine bk-long" data-genre="children" data-w="36" style="width:36px;height:275.0px;background:#67782a"><a href="/books/the-mysterious-benedict-society/" title="The Mysterious Benedict Society" style="max-height:263.0px"><strong>The Mysterious Benedict Society</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:242.5px;background:#67782a"><a href="/books/the-mysterious-benedict-society-and-the-perilous-journey/" title="The Mysterious Benedict Society and the Perilous Journey" style="max-height:230.5px"><strong>Perilous Journey</strong></a></div>
<div class="bk-spine" data-genre="children" data-w="27" style="width:27px;height:242.5px;background:#67782a"><a href="/books/the-mysterious-benedict-society-and-the-prisoners-dilemma/" title="The Mysterious Benedict Society and the Prisoner&#x27;s Dilemma" style="max-height:230.5px"><strong>Prisoner&#x27;s Dilemma</strong></a></div>
<div class="bk-spine bk-coll" data-coll="bartimaeus" data-genre="children" data-w="43" style="width:43px;height:276.6px;background:#67782a" title="Bartimaeus"><span class="bk-coll-name">Bartimaeus</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="children" data-w="36" data-volof="bartimaeus" style="width:36px;height:264.6px;background:#67782a"><a href="/books/the-amulet-of-samarkand/" title="The Amulet of Samarkand" style="max-height:252.60000000000002px">The Amulet of Samarkand</a></div>
<div class="bk-spine" data-genre="children" data-w="36" data-volof="bartimaeus" style="width:36px;height:264.6px;background:#67782a"><a href="/books/the-golems-eye/" title="The Golem&#x27;s Eye" style="max-height:252.60000000000002px">The Golem&#x27;s Eye</a></div>
<div class="bk-spine" data-genre="children" data-w="36" data-volof="bartimaeus" style="width:36px;height:264.6px;background:#67782a"><a href="/books/ptolemys-gate/" title="Ptolemy&#x27;s Gate" style="max-height:252.60000000000002px">Ptolemy&#x27;s Gate</a></div>
<div class="bk-spine" data-genre="children" data-w="27" data-volof="bartimaeus" style="width:27px;height:228.9px;background:#67782a"><a href="/books/the-ring-of-solomon/" title="The Ring of Solomon" style="max-height:216.9px">The Ring of Solomon</a></div>
<div class="bk-spine bk-long" data-genre="children" data-w="27" style="width:27px;height:232.2px;background:#67782a"><a href="/books/neil-flambe-and-the-marco-polo-murders/" title="Neil Flambe and the Marco Polo Murders" style="max-height:220.2px">Neil Flambe and the Marco Polo Murders</a></div>
<div class="bk-spine bk-long" data-genre="children" data-w="27" style="width:27px;height:232.2px;background:#67782a"><a href="/books/neil-flambe-and-the-aztec-abduction/" title="Neil Flambe and the Aztec Abduction" style="max-height:220.2px">Neil Flambe and the Aztec Abduction</a></div>
<div class="bk-spine" data-genre="comics" data-w="36" style="width:36px;height:251.6px;background:#2e4a7a"><a href="/books/foxtrot/" title="FoxTrot" style="max-height:239.6px"><strong>FoxTrot</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="27" style="width:27px;height:221.9px;background:#2e4a7a"><a href="/books/groovitude-a-get-fuzzy-treasury/" title="Groovitude: A Get Fuzzy Treasury" style="max-height:209.9px"><strong>Groovitude</strong></a></div>
<div class="bk-spine bk-coll" data-coll="garfield" data-genre="comics" data-w="43" style="width:43px;height:210.9px;background:#2e4a7a" title="Garfield"><span class="bk-coll-name">Garfield</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-at-large/" title="Garfield at Large" style="max-height:186.9px">Garfield at Large</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-gains-weight/" title="Garfield Gains Weight" style="max-height:186.9px">Garfield Gains Weight</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-bigger-than-life/" title="Garfield Bigger Than Life" style="max-height:186.9px">Garfield Bigger Than Life</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-weighs-in/" title="Garfield Weighs In" style="max-height:186.9px">Garfield Weighs In</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-takes-the-cake/" title="Garfield Takes the Cake" style="max-height:186.9px">Garfield Takes the Cake</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-eats-his-heart-out/" title="Garfield Eats His Heart Out" style="max-height:186.9px">Garfield Eats His Heart Out</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-sits-around-the-house/" title="Garfield Sits Around the House" style="max-height:186.9px">Garfield Sits Around the House</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-tips-the-scales/" title="Garfield Tips the Scales" style="max-height:186.9px">Garfield Tips the Scales</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-loses-his-feet/" title="Garfield Loses His Feet" style="max-height:186.9px">Garfield Loses His Feet</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-makes-it-big/" title="Garfield Makes It Big" style="max-height:186.9px">Garfield Makes It Big</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-rolls-on/" title="Garfield Rolls On" style="max-height:186.9px">Garfield Rolls On</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-out-to-lunch/" title="Garfield Out to Lunch" style="max-height:186.9px">Garfield Out to Lunch</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-food-for-thought/" title="Garfield Food for Thought" style="max-height:186.9px">Garfield Food for Thought</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-swallows-his-pride/" title="Garfield Swallows His Pride" style="max-height:186.9px">Garfield Swallows His Pride</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-worldwide/" title="Garfield Worldwide" style="max-height:186.9px">Garfield Worldwide</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-rounds-out/" title="Garfield Rounds Out" style="max-height:186.9px">Garfield Rounds Out</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-chews-the-fat/" title="Garfield Chews the Fat" style="max-height:186.9px">Garfield Chews the Fat</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-goes-to-waist/" title="Garfield Goes to Waist" style="max-height:186.9px">Garfield Goes to Waist</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-hangs-out/" title="Garfield Hangs Out" style="max-height:186.9px">Garfield Hangs Out</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-takes-up-space/" title="Garfield Takes Up Space" style="max-height:186.9px">Garfield Takes Up Space</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-says-a-mouthful/" title="Garfield Says a Mouthful" style="max-height:186.9px">Garfield Says a Mouthful</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-by-the-pound/" title="Garfield by the Pound" style="max-height:186.9px">Garfield by the Pound</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-keeps-his-chins-up/" title="Garfield Keeps His Chins Up" style="max-height:186.9px">Garfield Keeps His Chins Up</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-takes-his-licks/" title="Garfield Takes His Licks" style="max-height:186.9px">Garfield Takes His Licks</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-hits-the-big-time/" title="Garfield Hits the Big Time" style="max-height:186.9px">Garfield Hits the Big Time</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-pulls-his-weight/" title="Garfield Pulls His Weight" style="max-height:186.9px">Garfield Pulls His Weight</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-dishes-it-out/" title="Garfield Dishes It Out" style="max-height:186.9px">Garfield Dishes It Out</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-life-in-the-fat-lane/" title="Garfield Life in the Fat Lane" style="max-height:186.9px">Garfield Life in the Fat Lane</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-tons-of-fun/" title="Garfield Tons of Fun" style="max-height:186.9px">Garfield Tons of Fun</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-bigger-and-better/" title="Garfield Bigger and Better" style="max-height:186.9px">Garfield Bigger and Better</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-hams-it-up/" title="Garfield Hams It Up" style="max-height:186.9px">Garfield Hams It Up</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-thinks-big/" title="Garfield Thinks Big" style="max-height:186.9px">Garfield Thinks Big</a></div>
<div class="bk-spine bk-long" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-throws-his-weight-around/" title="Garfield Throws His Weight Around" style="max-height:186.9px">Garfield Throws His Weight Around</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-life-to-the-fullest/" title="Garfield: Life to the Fullest" style="max-height:186.9px">Garfield</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-feeds-the-kitty/" title="Garfield Feeds the Kitty" style="max-height:186.9px">Garfield Feeds the Kitty</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-hogs-the-spotlight/" title="Garfield Hogs the Spotlight" style="max-height:186.9px">Garfield Hogs the Spotlight</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-beefs-up/" title="Garfield Beefs Up" style="max-height:186.9px">Garfield Beefs Up</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-gets-cookin/" title="Garfield Gets Cookin&#x27;" style="max-height:186.9px">Garfield Gets Cookin&#x27;</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-eats-crow/" title="Garfield Eats Crow" style="max-height:186.9px">Garfield Eats Crow</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="garfield" style="width:20px;height:198.9px;background:#2e4a7a"><a href="/books/garfield-survival-of-the-fattest/" title="Garfield: Survival of the Fattest" style="max-height:186.9px">Garfield</a></div>
<div class="bk-spine bk-coll" data-coll="the-far-side" data-genre="comics" data-w="43" style="width:43px;height:207.7px;background:#2e4a7a" title="The Far Side"><span class="bk-coll-name"><strong>The Far Side</strong> &#9733;</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="the-far-side" style="width:20px;height:195.7px;background:#2e4a7a"><a href="/books/the-far-side-gallery/" title="The Far Side Gallery" style="max-height:183.7px"><strong>The Far Side Gallery</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="the-far-side" style="width:20px;height:195.7px;background:#2e4a7a"><a href="/books/the-far-side-gallery-2/" title="The Far Side Gallery 2" style="max-height:183.7px"><strong>The Far Side Gallery 2</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="the-far-side" style="width:20px;height:195.7px;background:#2e4a7a"><a href="/books/the-far-side-gallery-3/" title="The Far Side Gallery 3" style="max-height:183.7px"><strong>The Far Side Gallery 3</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="the-far-side" style="width:20px;height:195.7px;background:#2e4a7a"><a href="/books/the-far-side-gallery-4/" title="The Far Side Gallery 4" style="max-height:183.7px"><strong>The Far Side Gallery 4</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="the-far-side" style="width:20px;height:195.7px;background:#2e4a7a"><a href="/books/the-far-side-gallery-5/" title="The Far Side Gallery 5" style="max-height:183.7px"><strong>The Far Side Gallery 5</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" style="width:20px;height:211.9px;background:#2e4a7a"><a href="/books/where-the-sidewalk-ends/" title="Where the Sidewalk Ends" style="max-height:199.9px"><strong>Where the Sidewalk Ends</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" style="width:20px;height:208.7px;background:#2e4a7a"><a href="/books/cul-de-sac-this-exit/" title="Cul de Sac: This Exit" style="max-height:196.7px"><strong>Cul de Sac</strong></a></div>
<div class="bk-spine bk-coll" data-coll="calvin-and-hobbes" data-genre="comics" data-w="43" style="width:43px;height:266.2px;background:#2e4a7a" title="Calvin and Hobbes"><span class="bk-coll-name"><strong>Calvin and Hobbes</strong> &#9733;</span><span class="bk-coll-hint">click to expand</span></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="calvin-and-hobbes" style="width:20px;height:188.1px;background:#2e4a7a"><a href="/books/something-under-the-bed-is-drooling/" title="Something Under the Bed Is Drooling" style="max-height:176.1px"><strong>SUTBID</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="calvin-and-hobbes" style="width:20px;height:188.1px;background:#2e4a7a"><a href="/books/yukon-ho/" title="Yukon Ho!" style="max-height:176.1px"><strong>Yukon Ho!</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="calvin-and-hobbes" style="width:20px;height:188.1px;background:#2e4a7a"><a href="/books/weirdos-from-another-planet/" title="Weirdos from Another Planet!" style="max-height:176.1px"><strong>WFAP</strong> &#9733;</a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="calvin-and-hobbes" style="width:20px;height:188.1px;background:#2e4a7a"><a href="/books/the-revenge-of-the-baby-sat/" title="The Revenge of the Baby-Sat" style="max-height:176.1px"><strong>Revenge of the Baby-Sat</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="calvin-and-hobbes" style="width:20px;height:188.1px;background:#2e4a7a"><a href="/books/scientific-progress-goes-boink/" title="Scientific Progress Goes &quot;Boink&quot;" style="max-height:176.1px"><strong>Progress Goes Boink</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="calvin-and-hobbes" style="width:20px;height:188.1px;background:#2e4a7a"><a href="/books/attack-of-the-deranged-mutant-killer-monster-snow-goons/" title="Attack of the Deranged Mutant Killer Monster Snow Goons" style="max-height:176.1px"><strong>AOTDMKMSG</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="20" data-volof="calvin-and-hobbes" style="width:20px;height:188.1px;background:#2e4a7a"><a href="/books/the-days-are-just-packed/" title="The Days Are Just Packed" style="max-height:176.1px"><strong>The Days Are Just Packed</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="36" data-volof="calvin-and-hobbes" style="width:36px;height:254.2px;background:#2e4a7a"><a href="/books/the-complete-calvin-and-hobbes-volume-1/" title="The Complete Calvin and Hobbes, Volume 1" style="max-height:242.2px"><strong>Complete Calvin and Hobbes 1</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="36" data-volof="calvin-and-hobbes" style="width:36px;height:254.2px;background:#2e4a7a"><a href="/books/the-complete-calvin-and-hobbes-volume-2/" title="The Complete Calvin and Hobbes, Volume 2" style="max-height:242.2px"><strong>Complete Calvin and Hobbes 2</strong></a></div>
<div class="bk-spine" data-genre="comics" data-w="36" data-volof="calvin-and-hobbes" style="width:36px;height:254.2px;background:#2e4a7a"><a href="/books/the-complete-calvin-and-hobbes-volume-3/" title="The Complete Calvin and Hobbes, Volume 3" style="max-height:242.2px"><strong>Complete Calvin and Hobbes 3</strong></a></div>
<a class="bk-bookend" data-w="114" href="https://www.seamusriley.com/blog/crest/" title="The Riley Crest" style="text-decoration:none"><img src="/assets/images/crest_brown.svg" alt="Crest"></a>
</div>
<div style="width:16px;flex:none;border-radius:2px;background:linear-gradient(90deg,#98764e,#876542 55%,#71552f);box-shadow:inset 0 0 0 2px rgba(0,0,0,.15),inset 2px 0 3px rgba(255,255,255,.12),-2px 0 4px rgba(0,0,0,.25)"></div>
</div>
<p class="bk-legend">Bold titles are favorites, starred titles are reviewed. Click books for full titles. Spine color indicates category. Gold-banded spines are series collections: click one to see its books.<br>
<span class="bk-dot" style="background:#7a6a58"></span>Non-Fiction (1)<br>
<span class="bk-dot" style="background:#96502e"></span>Non-Fiction - Mind &amp; Self (2)<br>
<span class="bk-dot" style="background:#1e4d3d"></span>Non-Fiction - Philosophy (5)<br>
<span class="bk-dot" style="background:#2f6b4f"></span>Fiction - Philosophy (5)<br>
<span class="bk-dot" style="background:#6e5133"></span>Fiction - Classics &amp; Literary Fiction (21)<br>
<span class="bk-dot" style="background:#1f4e5f"></span>Fiction - Science Fiction (10)<br>
<span class="bk-dot" style="background:#9a5c26"></span>Fiction - Fantasy (13)<br>
<span class="bk-dot" style="background:#b45a1b"></span>Fiction - Dystopia (2)<br>
<span class="bk-dot" style="background:#26221e"></span>Fiction - Thriller (1)<br>
<span class="bk-dot" style="background:#67782a"></span>Fiction - Children's &amp; Middle Grade (140)<br>
<span class="bk-dot" style="background:#2e4a7a"></span>Comics &amp; Collections (59)<br>
<span class="bk-dot" style="background:transparent"></span>Total (259)<br>
<span class="bk-dot" style="background:transparent"></span>Serious Total (60)<br>
<span class="bk-dot" style="background:transparent"></span>Fiction Total (192)</p>

<script>
(function(){
  var main = document.getElementById('bk-main');
  if (!main) return;
  var items = Array.prototype.slice.call(main.children);
  var openColls = {};
  var shelfEl = document.getElementById('bookshelf');
  var ROW_H = 283;
  function budget(){
    // Rows wrap to the bookcase's inner width. The frame is a
    // fixed width (100% of the column, capped at 762px), so this
    // is stable: it does not change when collections open or
    // close. Never wider than the designed 730px.
    var w = main.clientWidth;
    if (!w && shelfEl && shelfEl.parentElement)
      w = shelfEl.parentElement.clientWidth - 34;
    if (!w || w < 120) w = 730;
    return Math.min(730, w);
  }
  var childrenCollapsed = true;  // Children's starts collapsed.
  var toggleBtn = document.getElementById('bk-toggle-all');
  var dividerEl = document.getElementById('bk-divider');
  function anyClosed(){
    if (childrenCollapsed) return true;
    for (var i = 0; i < items.length; i++) {
      var el = items[i];
      if (el.classList.contains('bk-coll') &&
          !openColls[el.getAttribute('data-coll')]) return true;
    }
    return false;
  }
  function syncBtn(){
    if (toggleBtn)
      toggleBtn.textContent = anyClosed() ? 'Expand all' : 'Collapse all';
    if (dividerEl) {
      var dh = dividerEl.querySelector('.bk-divider-hint');
      if (dh) dh.textContent =
        childrenCollapsed ? 'click to expand' : 'click to collapse';
    }
  }
  function isVis(el){
    if (el.classList.contains('bk-bookend') || el.id === 'bk-divider')
      return true;
    if (childrenCollapsed && el.getAttribute('data-genre') === 'children')
      return false;
    var vf = el.getAttribute('data-volof');
    if (vf && !openColls[vf]) return false;
    return true;
  }
  function wOf(el){ return parseInt(el.getAttribute('data-w'), 10) || 38; }
  function rowW(r){ return r.reduce(function(s, el){ return s + wOf(el); }, 0); }
  function reflow(){
    var MAXW = budget();
    main.innerHTML = '';
    items.forEach(function(el){
      // Undo any stretch from the previous layout.
      if (!el.classList.contains('bk-bookend')) {
        el.style.width = wOf(el) + 'px';
        el.style.flex = '';
      }
    });
    var rows = [], cur = [], curW = 0, bookend = null;
    items.forEach(function(el){
      if (!isVis(el)) return;
      if (el.classList.contains('bk-bookend')) { bookend = el; return; }
      var w = wOf(el);
      if (cur.length && curW + w > MAXW) { rows.push(cur); cur = []; curW = 0; }
      cur.push(el); curW += w;
    });
    rows.push(cur);
    var endW = 114;
    if (bookend) {
      // The bookend closes the shelf (his design, 2026-11-02): its
      // height never changes; only its width squishes, down to
      // fill the last row's remaining gap, and the crest — sized
      // by that width — stays inscribed in the top of the plaque,
      // its offset from the top equal to its offset from the
      // sides. The width may squish as far as a small book's width
      // (20px); below that there is no bookend at all and the
      // row's books stretch to fill the shelf instead. It never
      // pushes books onto a new shelf.
      var last = rows[rows.length - 1];
      var gap = MAXW - rowW(last);
      if (gap < 20) {
        endW = 0;
      } else {
        endW = Math.min(114, gap);
        bookend.style.width = endW + 'px';
        bookend.style.height = '114px';
        // The crest lives in a square box of 78% of the width,
        // centered in the square that fits the top of the plaque
        // (in the full-size square, simply centered). The box is
        // sized in pixels: a percentage height on the image made
        // its box follow the plaque's height instead, and
        // object-fit then centered the crest in the wrong box.
        var crest = bookend.querySelector('img');
        var cs = Math.round(endW * 0.78);
        bookend.style.paddingTop = Math.round((endW - cs) / 2) + 'px';
        if (crest) {
          crest.style.width = cs + 'px';
          crest.style.height = cs + 'px';
        }
        // A squished bookend also flexes by sub-pixel amounts, so
        // the frame's fractional width leaves no sliver beside it.
        bookend.style.flex = endW < 114 ? '1 1 auto' : '';
        last.push(bookend);
      }
    }
    rows.forEach(function(r){
      if (!r.length) return;
      var row = document.createElement('div');
      row.className = 'bk-row';
      row.style.padding = '0';
      row.style.height = ROW_H + 'px';
      // Fill the shelf: stretch the books slightly so a modest
      // wrap remainder disappears and the row fills the frame
      // edge to edge, books touching. A large remainder (the
      // last, partly-filled shelf) keeps natural widths.
      var rw = rowW(r);
      var hasEnd = bookend && r.indexOf(bookend) >= 0;
      var target = hasEnd ? MAXW - endW : MAXW;
      var base = hasEnd ? rw - 114 : rw;
      if (base > 0 && target > base && target / base <= 1.25) {
        // Integer widths that sum exactly to the target, so no
        // rounding pixel is left white at the right end.
        var scale = target / base;
        var pairs = [], used = 0;
        r.forEach(function(el){
          if (el === bookend) return;
          var nw = Math.floor(wOf(el) * scale);
          pairs.push([el, nw]); used += nw;
        });
        var extra = target - used;
        for (var i = 0; extra > 0 && pairs.length;
             i = (i + 1) % pairs.length) { pairs[i][1]++; extra--; }
        pairs.forEach(function(p){ p[0].style.width = p[1] + 'px'; });
        // The last book also flexes: the frame's true inner width
        // can be a fraction of a pixel, and whole-pixel widths
        // alone leave that fraction showing as a white sliver.
        if (pairs.length)
          pairs[pairs.length - 1][0].style.flex = '1 1 auto';
      }
      r.forEach(function(el){ row.appendChild(el); });
      main.appendChild(row);
      var board = document.createElement('div');
      board.className = 'bk-board';
      main.appendChild(board);
    });
    syncBtn();
  }
  items.forEach(function(el){
    if (el.classList.contains('bk-coll')) {
      el.addEventListener('click', function(){
        var k = el.getAttribute('data-coll');
        openColls[k] = !openColls[k];
        el.querySelector('.bk-coll-hint').textContent =
          openColls[k] ? 'click to collapse' : 'click to expand';
        reflow();
      });
    }
    if (el.id === 'bk-divider') {
      el.addEventListener('click', function(){
        childrenCollapsed = !childrenCollapsed;
        reflow();
      });
    }
  });
  if (toggleBtn) toggleBtn.addEventListener('click', function(){
    var open = anyClosed();
    childrenCollapsed = !open;
    items.forEach(function(el){
      if (el.classList.contains('bk-coll')) {
        openColls[el.getAttribute('data-coll')] = open;
        var hint = el.querySelector('.bk-coll-hint');
        if (hint)
          hint.textContent = open ? 'click to collapse' : 'click to expand';
      }
    });
    reflow();
  });
  window.addEventListener('resize', reflow);
  reflow();
})();
</script>

<table class="sortable">
<thead>
<tr><th>Rating</th><th>Name</th><th>Author</th><th>Recommender</th><th>Review</th></tr>
</thead>
<tbody>
<tr><td>&mdash;</td><td><a href="/books/addy-learns-a-lesson/">Addy Learns a Lesson</a></td><td>Connie Porter</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/addy-saves-the-day/">Addy Saves the Day</a></td><td>Connie Porter</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/addys-surprise/">Addy&#x27;s Surprise</a></td><td>Connie Porter</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-adventures-of-huckleberry-finn/">The Adventures of Huckleberry Finn</a></td><td>Mark Twain</td><td>&mdash;</td><td><a href="/books/the-adventures-of-huckleberry-finn/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-adventures-of-tom-sawyer/">The Adventures of Tom Sawyer</a></td><td>Mark Twain</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/afternoon-on-the-amazon/">Afternoon on the Amazon</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/airman/">Airman</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/alabama-moon/">Alabama Moon (Alabama Moon, #1)</a></td><td>Watt Key</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/all-the-pretty-horses/">All the Pretty Horses (The Border Trilogy, #1)</a></td><td>Cormac McCarthy</td><td>Eli</td><td><a href="/books/all-the-pretty-horses/">Review</a></td></tr>
<tr><td>&mdash;</td><td><a href="/books/the-amulet-of-samarkand/">The Amulet of Samarkand</a></td><td>Jonathan Stroud</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/and-another-thing/">And Another Thing... (The Hitchhiker&#x27;s Guide to the Galaxy, #6)</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/another-whole-nother-story/">Another Whole Nother Story</a></td><td>Cuthbert Soup</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/anthem/">Anthem</a></td><td>Ayn Rand</td><td>&mdash;</td><td><a href="/books/anthem/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl/">Artemis Fowl</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-artemis-fowl-files/">The Artemis Fowl Files</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl-the-arctic-incident/">Artemis Fowl: The Arctic Incident</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl-the-atlantis-complex/">Artemis Fowl: The Atlantis Complex</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl-the-eternity-code/">Artemis Fowl: The Eternity Code</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl-the-last-guardian/">Artemis Fowl: The Last Guardian</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl-the-lost-colony/">Artemis Fowl: The Lost Colony</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl-the-opal-deception/">Artemis Fowl: The Opal Deception</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/artemis-fowl-the-time-paradox/">Artemis Fowl: The Time Paradox</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/atlas-shrugged/">Atlas Shrugged</a></td><td>Ayn Rand</td><td>&mdash;</td><td><a href="/books/atlas-shrugged/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/attack-of-the-deranged-mutant-killer-monster-snow-goons/">Attack of the Deranged Mutant Killer Monster Snow Goons</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-austere-academy/">The Austere Academy</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-bad-beginning/">The Bad Beginning</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-battle-of-the-labyrinth/">The Battle of the Labyrinth (Percy Jackson and the Olympians, #4)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/behemoth/">Behemoth (Leviathan, #2)</a></td><td>Scott Westerfeld</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/beyond-the-grave/">Beyond the Grave</a></td><td>Jude Watson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-black-circle/">The Black Circle</a></td><td>Patrick Carman</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/blizzard-of-the-blue-moon/">Blizzard of the Blue Moon</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-blood-of-olympus/">The Blood of Olympus (The Heroes of Olympus, #5)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/born-to-run-a-hidden-tribe-superathletes-and-the-greatest-race-the-world-has-never-seen/">Born to Run: A Hidden Tribe, Superathletes, and the Greatest Race the World Has Never Seen</a></td><td>Christopher McDougall</td><td>&mdash;</td><td><a href="/books/born-to-run-a-hidden-tribe-superathletes-and-the-greatest-race-the-world-has-never-seen/">Review</a></td></tr>
<tr><td>&mdash;</td><td><a href="/books/brians-return/">Brian&#x27;s Return</a></td><td>Gary Paulsen</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/brians-winter/">Brian&#x27;s Winter</a></td><td>Gary Paulsen</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/brisingr/">Brisingr (Inheritance, #3)</a></td><td>Christopher Paolini</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/bud-not-buddy/">Bud, Not Buddy</a></td><td>Christopher Paul Curtis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/buffalo-before-breakfast/">Buffalo Before Breakfast</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/carnival-at-candlelight/">Carnival at Candlelight</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-carnivorous-carnival/">The Carnivorous Carnival</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/chains/">Chains</a></td><td>Laurie Halse Anderson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/changes-for-addy/">Changes for Addy</a></td><td>Connie Porter</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/christmas-in-camelot/">Christmas in Camelot</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-city-of-ember/">The City of Ember (Book of Ember, #1)</a></td><td>Jeanne DuPrau</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/civil-war-on-sunday/">Civil War on Sunday</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/codependent-no-more/">Codependent No More</a></td><td>Melody Beattie</td><td>Don Michelson</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-complete-calvin-and-hobbes-volume-1/">The Complete Calvin and Hobbes, Volume 1</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-complete-calvin-and-hobbes-volume-2/">The Complete Calvin and Hobbes, Volume 2</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-complete-calvin-and-hobbes-volume-3/">The Complete Calvin and Hobbes, Volume 3</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/cul-de-sac-this-exit/">Cul de Sac: This Exit</a></td><td>Richard Thompson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/day-of-the-dragon-king/">Day of the Dragon King</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-days-are-just-packed/">The Days Are Just Packed</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-diamond-of-darkhold/">The Diamond of Darkhold (Book of Ember, #4)</a></td><td>Jeanne DuPrau</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/diary-of-a-wimpy-kid/">Diary of a Wimpy Kid</a></td><td>Jeff Kinney</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/diary-of-a-wimpy-kid-cabin-fever/">Diary of a Wimpy Kid: Cabin Fever</a></td><td>Jeff Kinney</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/diary-of-a-wimpy-kid-dog-days/">Diary of a Wimpy Kid: Dog Days</a></td><td>Jeff Kinney</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/diary-of-a-wimpy-kid-rodrick-rules/">Diary of a Wimpy Kid: Rodrick Rules</a></td><td>Jeff Kinney</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/diary-of-a-wimpy-kid-the-last-straw/">Diary of a Wimpy Kid: The Last Straw</a></td><td>Jeff Kinney</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/diary-of-a-wimpy-kid-the-third-wheel/">Diary of a Wimpy Kid: The Third Wheel</a></td><td>Jeff Kinney</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/diary-of-a-wimpy-kid-the-ugly-truth/">Diary of a Wimpy Kid: The Ugly Truth</a></td><td>Jeff Kinney</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/dingoes-at-dinnertime/">Dingoes at Dinnertime</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/dinosaurs-before-dark/">Dinosaurs Before Dark</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-discovery-of-freedom/">The Discovery of Freedom</a></td><td>Rose Wilder Lane</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/dolphins-at-daybreak/">Dolphins at Daybreak</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/double-fudge/">Double Fudge</a></td><td>Judy Blume</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/dragon-of-the-red-dawn/">Dragon of the Red Dawn</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/earthquake-in-the-early-morning/">Earthquake in the Early Morning</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/eldest/">Eldest (Inheritance, #2)</a></td><td>Christopher Paolini</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/elijah-of-buxton/">Elijah of Buxton</a></td><td>Christopher Paul Curtis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-emperors-code/">The Emperor&#x27;s Code</a></td><td>Gordon Korman</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-end/">The End</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/enders-game/">Ender&#x27;s Game (Ender&#x27;s Saga, #1)</a></td><td>Orson Scott Card</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/eragon/">Eragon (Inheritance, #1)</a></td><td>Christopher Paolini</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-ersatz-elevator/">The Ersatz Elevator</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-fall-line/">The Fall Line</a></td><td>Lucid Fitzpatrick</td><td>&mdash;</td><td><a href="/books/the-fall-line/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-far-side-gallery/">The Far Side Gallery</a></td><td>Gary Larson</td><td>&mdash;</td><td><a href="/books/the-far-side-gallery/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-far-side-gallery-2/">The Far Side Gallery 2</a></td><td>Gary Larson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-far-side-gallery-3/">The Far Side Gallery 3</a></td><td>Gary Larson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-far-side-gallery-4/">The Far Side Gallery 4</a></td><td>Gary Larson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-far-side-gallery-5/">The Far Side Gallery 5</a></td><td>Gary Larson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-fellowship-of-the-ring/">The Fellowship of the Ring</a></td><td>J.R.R. Tolkien</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-fountainhead/">The Fountainhead</a></td><td>Ayn Rand</td><td>&mdash;</td><td><a href="/books/the-fountainhead/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/foxtrot/">FoxTrot</a></td><td>Bill Amend</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-at-large/">Garfield at Large</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-beefs-up/">Garfield Beefs Up</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-bigger-and-better/">Garfield Bigger and Better</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-bigger-than-life/">Garfield Bigger Than Life</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-by-the-pound/">Garfield by the Pound</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-chews-the-fat/">Garfield Chews the Fat</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-dishes-it-out/">Garfield Dishes It Out</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-eats-crow/">Garfield Eats Crow</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-eats-his-heart-out/">Garfield Eats His Heart Out</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-feeds-the-kitty/">Garfield Feeds the Kitty</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-food-for-thought/">Garfield Food for Thought</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-gains-weight/">Garfield Gains Weight</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-gets-cookin/">Garfield Gets Cookin&#x27;</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-goes-to-waist/">Garfield Goes to Waist</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-hams-it-up/">Garfield Hams It Up</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-hangs-out/">Garfield Hangs Out</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-hits-the-big-time/">Garfield Hits the Big Time</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-hogs-the-spotlight/">Garfield Hogs the Spotlight</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-keeps-his-chins-up/">Garfield Keeps His Chins Up</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-life-in-the-fat-lane/">Garfield Life in the Fat Lane</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-loses-his-feet/">Garfield Loses His Feet</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-makes-it-big/">Garfield Makes It Big</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-out-to-lunch/">Garfield Out to Lunch</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-pulls-his-weight/">Garfield Pulls His Weight</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-rolls-on/">Garfield Rolls On</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-rounds-out/">Garfield Rounds Out</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-says-a-mouthful/">Garfield Says a Mouthful</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-sits-around-the-house/">Garfield Sits Around the House</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-swallows-his-pride/">Garfield Swallows His Pride</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-takes-his-licks/">Garfield Takes His Licks</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-takes-the-cake/">Garfield Takes the Cake</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-takes-up-space/">Garfield Takes Up Space</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-thinks-big/">Garfield Thinks Big</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-throws-his-weight-around/">Garfield Throws His Weight Around</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-tips-the-scales/">Garfield Tips the Scales</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-tons-of-fun/">Garfield Tons of Fun</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-weighs-in/">Garfield Weighs In</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-worldwide/">Garfield Worldwide</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-life-to-the-fullest/">Garfield: Life to the Fullest</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/garfield-survival-of-the-fattest/">Garfield: Survival of the Fattest</a></td><td>Jim Davis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/georges-marvelous-medicine/">George&#x27;s Marvelous Medicine</a></td><td>Roald Dahl</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/ghost-town-at-sundown/">Ghost Town at Sundown</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-god-of-the-machine/">The God of the Machine</a></td><td>Isabel Paterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/the-golems-eye/">The Golem&#x27;s Eye</a></td><td>Jonathan Stroud</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/goliath/">Goliath (Leviathan, #3)</a></td><td>Scott Westerfeld</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/good-morning-gorillas/">Good Morning, Gorillas</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-green-glass-sea/">The Green Glass Sea (Green Glass, #1)</a></td><td>Ellen Klages</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-grim-grotto/">The Grim Grotto</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/groovitude-a-get-fuzzy-treasury/">Groovitude: A Get Fuzzy Treasury</a></td><td>Darby Conley</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/gullivers-travels/">Gulliver&#x27;s Travels</a></td><td>Jonathan Swift</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/half-moon-investigations/">Half Moon Investigations</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/happy-birthday-addy/">Happy Birthday, Addy!</a></td><td>Connie Porter</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/harry-potter-and-the-chamber-of-secrets/">Harry Potter and the Chamber of Secrets (Harry Potter, #2)</a></td><td>J.K. Rowling</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/harry-potter-and-the-deathly-hallows/">Harry Potter and the Deathly Hallows (Harry Potter, #7)</a></td><td>J.K. Rowling</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/harry-potter-and-the-goblet-of-fire/">Harry Potter and the Goblet of Fire (Harry Potter, #4)</a></td><td>J.K. Rowling</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/harry-potter-and-the-half-blood-prince/">Harry Potter and the Half-Blood Prince (Harry Potter, #6)</a></td><td>J.K. Rowling</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/harry-potter-and-the-order-of-the-phoenix/">Harry Potter and the Order of the Phoenix (Harry Potter, #5)</a></td><td>J.K. Rowling</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/harry-potter-and-the-prisoner-of-azkaban/">Harry Potter and the Prisoner of Azkaban (Harry Potter, #3)</a></td><td>J.K. Rowling</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/harry-potter-and-the-sorcerers-stone/">Harry Potter and the Sorcerer&#x27;s Stone (Harry Potter, #1)</a></td><td>J.K. Rowling</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/hatchet/">Hatchet</a></td><td>Gary Paulsen</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/haunted-castle-on-hallows-eve/">Haunted Castle on Hallows Eve</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/high-tide-in-hawaii/">High Tide in Hawaii</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-higher-power-of-lucky/">The Higher Power of Lucky (The Hard Pan Trilogy, #1)</a></td><td>Susan Patron</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-hitchhikers-guide-to-the-galaxy/">The Hitchhiker&#x27;s Guide to the Galaxy (The Hitchhiker&#x27;s Guide to the Galaxy, #1)</a></td><td>Douglas Adams</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-hobbit/">The Hobbit</a></td><td>J.R.R. Tolkien</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/holes/">Holes</a></td><td>Louis Sachar</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-horse-and-his-boy/">The Horse and His Boy</a></td><td>C.S. Lewis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-hostile-hospital/">The Hostile Hospital</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/hour-of-the-olympics/">Hour of the Olympics</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-house-of-hades/">The House of Hades (The Heroes of Olympus, #4)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-house-on-the-cliff/">The House on the Cliff</a></td><td>Franklin W. Dixon</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/hunting-for-hidden-gold/">Hunting for Hidden Gold</a></td><td>Franklin W. Dixon</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/i-am-justice/">I Am Justice</a></td><td>D.P. Watkins</td><td>&mdash;</td><td><a href="/books/i-am-justice/">Review</a></td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/ideal/">Ideal</a></td><td>Ayn Rand</td><td>&mdash;</td><td><a href="/books/ideal/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/in-too-deep/">In Too Deep</a></td><td>Jude Watson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/inheritance/">Inheritance (Inheritance, #4)</a></td><td>Christopher Paolini</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/into-the-gauntlet/">Into the Gauntlet</a></td><td>Margaret Peterson Haddix</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/introduction-to-objectivist-epistemology/">Introduction to Objectivist Epistemology</a></td><td>Ayn Rand</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/kidnapped/">Kidnapped</a></td><td>Robert Louis Stevenson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/the-knight-at-dawn/">The Knight at Dawn</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-last-battle/">The Last Battle</a></td><td>C.S. Lewis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-last-olympian/">The Last Olympian (Percy Jackson and the Olympians, #5)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/legend/">Legend (Legend, #1)</a></td><td>Marie Lu</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/leviathan/">Leviathan (Leviathan, #1)</a></td><td>Scott Westerfeld</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/life-the-universe-and-everything/">Life, the Universe and Everything (The Hitchhiker&#x27;s Guide to the Galaxy, #3)</a></td><td>Douglas Adams</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-lightning-thief/">The Lightning Thief (Percy Jackson and the Olympians, #1)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-lion-the-witch-and-the-wardrobe/">The Lion, the Witch and the Wardrobe</a></td><td>C.S. Lewis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/lions-at-lunchtime/">Lions at Lunchtime</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-lost-hero/">The Lost Hero (The Heroes of Olympus, #1)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/lucky-breaks/">Lucky Breaks (The Hard Pan Trilogy, #2)</a></td><td>Susan Patron</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-magicians-nephew/">The Magician&#x27;s Nephew (Chronicles of Narnia, #6)</a></td><td>C.S. Lewis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-mark-of-athena/">The Mark of Athena (The Heroes of Olympus, #3)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/masters-of-disaster/">Masters of Disaster</a></td><td>Gary Paulsen</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-maze-of-bones/">The Maze of Bones</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/meet-addy/">Meet Addy</a></td><td>Connie Porter</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/midnight-on-the-moon/">Midnight on the Moon</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-miserable-mill/">The Miserable Mill</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/mistborn-the-final-empire/">Mistborn: The Final Empire</a></td><td>Brandon Sanderson</td><td>&mdash;</td><td><a href="/books/mistborn-the-final-empire/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/mostly-harmless/">Mostly Harmless (Hitchhiker&#x27;s Guide to the Galaxy, #5)</a></td><td>Douglas Adams</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/mr-poppers-penguins/">Mr. Popper&#x27;s Penguins</a></td><td>Richard and Florence Atwater</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/mummies-in-the-morning/">Mummies in the Morning</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-mysterious-benedict-society/">The Mysterious Benedict Society</a></td><td>Trenton Lee Stewart</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-mysterious-benedict-society-and-the-perilous-journey/">The Mysterious Benedict Society and the Perilous Journey</a></td><td>Trenton Lee Stewart</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-mysterious-benedict-society-and-the-prisoners-dilemma/">The Mysterious Benedict Society and the Prisoner&#x27;s Dilemma</a></td><td>Trenton Lee Stewart</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/nation/">Nation</a></td><td>Terry Pratchett</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/neil-flambe-and-the-aztec-abduction/">Neil Flambe and the Aztec Abduction</a></td><td>Kevin Sylvester</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/neil-flambe-and-the-marco-polo-murders/">Neil Flambe and the Marco Polo Murders</a></td><td>Kevin Sylvester</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/night-of-the-new-magicians/">Night of the New Magicians</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/night-of-the-ninjas/">Night of the Ninjas</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-ominous-parallels/">The Ominous Parallels</a></td><td>Leonard Peikoff</td><td>&mdash;</td><td><a href="/books/the-ominous-parallels/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/one-false-note/">One False Note</a></td><td>Gordon Korman</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/opar/">OPAR (Objectivism: The Philosophy of Ayn Rand)</a></td><td>Leonard Peikoff</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-penultimate-peril/">The Penultimate Peril</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-people-of-sparks/">The People of Sparks (The City of Ember #2)</a></td><td>Jeanne DuPrau</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/pirates-past-noon/">Pirates Past Noon</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/polar-bears-past-bedtime/">Polar Bears Past Bedtime</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/prince-caspian/">Prince Caspian</a></td><td>C.S. Lewis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-prophet-of-yonwood/">The Prophet of Yonwood (Book of Ember, #3)</a></td><td>Jeanne DuPrau</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/ptolemys-gate/">Ptolemy&#x27;s Gate</a></td><td>Jonathan Stroud</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/reality-leak/">Reality Leak</a></td><td>Joni Sensel</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-reptile-room/">The Reptile Room</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-restaurant-at-the-end-of-the-universe/">The Restaurant at the End of the Universe (The Hitchhiker&#x27;s Guide to the Galaxy, #2)</a></td><td>Douglas Adams</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-revenge-of-the-baby-sat/">The Revenge of the Baby-Sat</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/revolutionary-war-on-wednesday/">Revolutionary War on Wednesday</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/the-ring-of-solomon/">The Ring of Solomon</a></td><td>Jonathan Stroud</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/the-river/">The River</a></td><td>Gary Paulsen</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/robinson-crusoe/">Robinson Crusoe</a></td><td>Daniel Defoe</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/rootless/">Rootless (Rootless, #1)</a></td><td>Chris Howard</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/saving-shiloh/">Saving Shiloh (Shiloh, #3)</a></td><td>Phyllis Reynolds Naylor</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/scientific-progress-goes-boink/">Scientific Progress Goes &quot;Boink&quot;</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-sea-of-monsters/">The Sea of Monsters (Percy Jackson and the Olympians, #2)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/season-of-the-sandstorms/">Season of the Sandstorms</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-secret-of-the-lost-tunnel/">The Secret of the Lost Tunnel</a></td><td>Franklin W. Dixon</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/shiloh/">Shiloh (Shiloh, #1)</a></td><td>Phyllis Reynolds Naylor</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/shiloh-season/">Shiloh Season (Shiloh, #2)</a></td><td>Phyllis Reynolds Naylor</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-silver-chair/">The Silver Chair</a></td><td>C.S. Lewis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/a-single-shard/">A Single Shard</a></td><td>Linda Sue Park</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-slippery-slope/">The Slippery Slope</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/so-long-and-thanks-for-all-the-fish/">So Long, and Thanks for All the Fish (The Hitchhiker&#x27;s Guide to the Galaxy, #4)</a></td><td>Douglas Adams</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/something-under-the-bed-is-drooling/">Something Under the Bed Is Drooling</a></td><td>Bill Watterson</td><td>&mdash;</td><td><a href="/books/something-under-the-bed-is-drooling/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-son-of-neptune/">The Son of Neptune (The Heroes of Olympus, #2)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/stage-fright-on-a-summer-night/">Stage Fright on a Summer Night</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/steel-trapp/">Steel Trapp</a></td><td>Ridley Pearson</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/storm-warning/">Storm Warning</a></td><td>Linda Sue Park</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/summer-of-the-sea-serpent/">Summer of the Sea Serpent</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/sunset-of-the-sabertooth/">Sunset of the Sabertooth</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-supernaturalist/">The Supernaturalist</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-swiss-family-robinson/">The Swiss Family Robinson</a></td><td>Johann David Wyss</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-sword-thief/">The Sword Thief</a></td><td>Peter Lerangis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/the-tale-of-despereaux/">The Tale of Despereaux</a></td><td>Kate DiCamillo</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/thanksgiving-on-thursday/">Thanksgiving on Thursday</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-therapy-manifesto-a-principled-guide-to-developing-your-mental-health/">The Therapy Manifesto: A Principled Guide to Developing Your Mental Health</a></td><td>Mark Derian</td><td>&mdash;</td><td><a href="/books/the-therapy-manifesto-a-principled-guide-to-developing-your-mental-health/">Review</a></td></tr>
<tr><td>&mdash;</td><td><a href="/books/tigers-at-twilight/">Tigers at Twilight</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-titans-curse/">The Titan&#x27;s Curse (Percy Jackson and the Olympians, #3)</a></td><td>Rick Riordan</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/to-kill-a-mockingbird/">To Kill a Mockingbird</a></td><td>Harper Lee</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/tonight-on-the-titanic/">Tonight on the Titanic</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-tower-treasure/">The Tower Treasure</a></td><td>Franklin W. Dixon</td><td>&mdash;</td><td><a href="/books/the-tower-treasure/">Review</a></td></tr>
<tr><td>&mdash;</td><td><a href="/books/trackers/">Trackers</a></td><td>Patrick Carman</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/trackers-shantorian/">Trackers: Shantorian</a></td><td>Patrick Carman</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/twister-on-tuesday/">Twister on Tuesday</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/vacation-under-the-volcano/">Vacation Under the Volcano</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/viking-ships-at-sunrise/">Viking Ships at Sunrise</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-vile-village/">The Vile Village</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-vipers-nest/">The Viper&#x27;s Nest</a></td><td>Peter Lerangis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>1/2 Nice</td><td><a href="/books/the-voyage-of-the-dawn-treader/">The Voyage of the Dawn Treader</a></td><td>C.S. Lewis</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-voyage-of-the-frog/">The Voyage of the Frog</a></td><td>Gary Paulsen</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/we-the-living/">We the Living</a></td><td>Ayn Rand</td><td>&mdash;</td><td><a href="/books/we-the-living/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/weirdos-from-another-planet/">Weirdos from Another Planet!</a></td><td>Bill Watterson</td><td>&mdash;</td><td><a href="/books/weirdos-from-another-planet/">Review</a></td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/the-westing-game/">The Westing Game</a></td><td>Ellen Raskin</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/westward-home-joshuas-diary/">Westward Home: Joshua&#x27;s Diary</a></td><td>Patricia Hermes</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/where-the-sidewalk-ends/">Where the Sidewalk Ends</a></td><td>Shel Silverstein</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/a-whole-nother-story/">A Whole Nother Story</a></td><td>Cuthbert Soup</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>0/2 Not For Me</td><td><a href="/books/the-wide-window/">The Wide Window</a></td><td>Lemony Snicket</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/winter-of-the-ice-wizard/">Winter of the Ice Wizard</a></td><td>Mary Pope Osborne</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>&mdash;</td><td><a href="/books/the-wish-list/">The Wish List</a></td><td>Eoin Colfer</td><td>&mdash;</td><td>&mdash;</td></tr>
<tr><td>2/2 Wonderful</td><td><a href="/books/yukon-ho/">Yukon Ho!</a></td><td>Bill Watterson</td><td>&mdash;</td><td>&mdash;</td></tr>
</tbody>
</table>

### Want to Read

- Annihilation
  - Written by Jeff VanderMeer
  - Recommended by Me
- The DIM Hypothesis
  - Written by Leonard Peikoff
  - Recommended by Me
- Emotion and Meaning in Music
  - Written by Leonard B. Meyer
  - Recommended by Tim White
- The Franklin Project
  - Recommended by Me
- Freehold
  - Written by Michael Z. Williamson
  - Recommended by Erek
- Heroes and Champions
  - Written by Andrew Bernstein
  - Recommended by Me
- How We Know
  - Written by Harry Binswanger
  - Recommended by Me
- Less Than Words Can Say
  - Written by Richard Mitchell
  - Recommended by Me
- A Little Princess
  - Written by Frances Hodgson Burnett
  - Recommended by Andre
- Loving Life
  - Written by Craig Biddle
  - Recommended by Me
- Miracleman
  - Recommended by Me
- Mr. A
  - Recommended by Me
- Myths to Live By
  - Written by Joseph Campbell
  - Recommended by Angel
- Netochka Nezvanova
  - Written by Fyodor Dostoevsky
- Nostrilia
  - Recommended by Erek
- Open Veins of Latin America
  - Written by Eduardo Galeano
  - Recommended by Olive
- Piranesi
  - Written by Susanna Clarke
  - Recommended by Patrick
- The Productivity Project
  - Written by Chris Bailey
  - Recommended by Me
- The Reckoning (Rootless, #3)
  - Written by Chris Howard
- The Rift (Rootless, #2)
  - Written by Chris Howard
- The Shame Core
  - Written by John Bradshaw
  - Recommended by Andrew Dowdy
- Touching the Art
  - Written by Luc Travers
  - Recommended by Me
- The Witcher Books
  - Written by Andrzej Sapkowski
  - Recommended by Me

<style>
table.sortable th{cursor:pointer}
table.sortable th.srt[data-dir="asc"]::after{content:" ▴"}
table.sortable th.srt[data-dir="desc"]::after{content:" ▾"}
</style>
<script>
document.querySelectorAll('table.sortable').forEach(function(tbl){
  var ths = tbl.querySelectorAll('thead th');
  function key(td){
    var t = td.textContent.trim().toLowerCase();
    if (t === '—') return '~~~~';
    return t.replace(/^(the|a|an)\s+/, '');
  }
  ths.forEach(function(th, i){
    th.title = 'Click to sort';
    th.addEventListener('click', function(){
      var tbody = tbl.querySelector('tbody');
      var rows = Array.prototype.slice.call(tbody.querySelectorAll('tr'));
      var asc = th.getAttribute('data-dir') !== 'asc';
      ths.forEach(function(o){ o.removeAttribute('data-dir'); o.classList.remove('srt'); });
      th.setAttribute('data-dir', asc ? 'asc' : 'desc');
      th.classList.add('srt');
      rows.sort(function(a, b){
        var x = key(a.children[i]), y = key(b.children[i]);
        return (x < y ? -1 : x > y ? 1 : 0) * (asc ? 1 : -1);
      });
      rows.forEach(function(r){ tbody.appendChild(r); });
    });
  });
});
</script>
