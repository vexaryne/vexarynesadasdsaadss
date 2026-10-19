
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#0d0f15">
<title>PSITTACOLOGY / README.md</title>

<style>
:root {
  --bg: #0d0f15;
  --panel: #151820;
  --border: #393b49;
  --purple: #c8a5fa;
  --pink: #f0a0df;
  --white: #f3edf9;
  --muted: #9c91ac;
  --blue: #78b9ff;
}

* { box-sizing: border-box; }

body {
  margin: 0;
  padding: 16px;
  min-height: 100vh;
  background: var(--bg);
  color: var(--white);
  font-family: "Trebuchet MS", Arial, sans-serif;
  font-size: 12px;
}

a {
  color: var(--blue);
  text-decoration: underline;
  text-underline-offset: 3px;
}

a:hover { color: var(--pink); }

.profile {
  max-width: 920px;
  min-height: 630px;
  margin: 0 auto;
  padding: 24px 26px;
  overflow: hidden;
  border: 1px solid var(--border);
  border-radius: 5px;
  background:
    radial-gradient(ellipse at 26% 40%, #37234826, transparent 37%),
    var(--bg);
}

.topline {
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 12px;
  margin-bottom: 22px;
  font-family: monospace;
  font-size: 10px;
}

.topline strong {
  font-weight: normal;
  color: var(--purple);
}

.counter {
  padding: 3px 8px;
  background: linear-gradient(90deg, #8e69b9, #d58acb);
  color: white;
  white-space: nowrap;
}

.layout {
  display: grid;
  grid-template-columns: 235px minmax(0, 1fr);
  gap: 28px;
  align-items: start;
}

.left {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-width: 0;
}

.character-frame {
  position: relative;
  width: 100%;
  min-height: 440px;
  display: flex;
  justify-content: center;
  align-items: center;
  overflow: hidden;
  background: radial-gradient(
    ellipse at 50% 48%,
    #a77bc62a 0,
    #4c32651b 35%,
    transparent 72%
  );
}

.character-frame::before {
  content: "✧  ·  ⋆  ·  ✧";
  position: absolute;
  top: 15px;
  color: var(--pink);
  letter-spacing: 5px;
  font-size: 13px;
}

.character-frame::after {
  content: "art but make it ✦";
  position: absolute;
  right: 2px;
  bottom: 24px;
  color: #c9a4e4a8;
  font-family: Georgia, serif;
  font-style: italic;
  transform: rotate(-7deg);
}

.main-art {
  width: 195px;
  height: 300px;
  object-fit: contain;
  filter: drop-shadow(0 0 16px #b78de633);
  transition: transform .3s ease, filter .3s ease;
}

.main-art:hover {
  transform: translateY(-5px) rotate(-2deg);
  filter: drop-shadow(0 0 23px #c8a5fa66);
}

.mini-stamps {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 8px;
  margin-top: 10px;
}

.stamp {
  width: 43px;
  height: 43px;
  padding: 5px;
  object-fit: contain;
  border: 1px solid #51445e;
  background: #191620;
}

.right { min-width: 0; }

.banner {
  min-height: 42px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
  margin-bottom: 16px;
  padding: 10px 14px;
  border-radius: 5px;
  background: var(--panel);
  color: #e6dfef;
  font: 10px monospace;
  letter-spacing: .4px;
}

.copy {
  padding: 6px 9px;
  border: 1px solid #4b4e5c;
  border-radius: 4px;
  background: #20232d;
  color: var(--white);
  cursor: pointer;
}

.copy:hover { border-color: var(--purple); }

.intro { text-align: center; }

.aliases {
  margin: 12px 0;
  font-size: 13px;
}

.aliases span:nth-child(1) { color: var(--purple); }
.aliases span:nth-child(2) { color: var(--blue); }
.aliases span:nth-child(3) { color: #ff85b6; }

.pronouns {
  color: var(--purple);
  font-size: 12px;
  letter-spacing: .4px;
}

.squiggle {
  margin: 18px 0;
  color: var(--pink);
  text-align: center;
  letter-spacing: 3px;
  font-size: 13px;
}

.links {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 7px;
  margin: 17px 0;
  font-size: 12px;
}

.callout {
  margin: 18px 0;
  text-align: center;
  color: var(--pink);
  font-size: 12px;
}

.friends {
  margin-top: 18px;
  line-height: 2;
}

.friends a { white-space: nowrap; }

.art-row {
  display: grid;
  grid-template-columns: 1fr 150px;
  gap: 16px;
  align-items: center;
  margin-top: 24px;
}

.note {
  padding: 12px;
  border: 1px solid #383342;
  background: #14151c;
  color: var(--muted);
  font: italic 11px/1.8 Georgia, serif;
  text-align: center;
}

.duo {
  display: block;
  width: 145px;
  height: 140px;
  object-fit: contain;
  padding: 8px;
  background: radial-gradient(ellipse, #60417433, transparent 70%);
  filter: drop-shadow(0 0 8px #c5a0fa22);
}

.bottom {
  margin-top: 24px;
  padding-top: 14px;
  border-top: 1px solid #322b3c;
  text-align: center;
}

.bottom .squiggle { margin: 0 0 10px; }

.small-links {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 12px;
  color: var(--muted);
  font-size: 10px;
}

@media (min-width: 700px) {
  .profile { padding: 24px 30px; }
  .layout { grid-template-columns: 250px minmax(0, 1fr); }
  .character-frame { min-height: 460px; }
}

@media (max-width: 560px) {
  body { padding: 7px; }
  .profile { padding: 15px; }
  .layout { grid-template-columns: 1fr; gap: 18px; }
  .left { order: 0; }
  .right { order: 1; }
  .character-frame { min-height: 250px; }
  .main-art { height: 225px; }
  .art-row { grid-template-columns: 1fr 110px; gap: 8px; }
  .duo { width: 110px; height: 110px; }
  .topline { margin-bottom: 15px; }
}

@media (prefers-reduced-motion: reduce) {
  *, *::before, *::after { transition: none !important; }
}
</style>
</head>

<body>
<main class="profile">

  <div class="topline">
    <span><strong>PSITTACOLOGY</strong> / README.md</span>
    <span class="counter">✦ 11,407</span>
  </div>

  <div class="layout">

  <aside class="left">
      <div class="character-frame">
        <!-- CC BY-SA OpenMoji placeholder. Replace with a licensed
             transparent anime character PNG when desired. -->
        <img class="main-art"
          src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F9D9.svg"
          alt="Fantasy character placeholder">
      </div>

  <div class="mini-stamps">
        <img class="stamp"
          src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F47E.svg"
          alt="Alien sticker">
        <img class="stamp"
          src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F338.svg"
          alt="Flower sticker">
        <img class="stamp"
          src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F319.svg"
          alt="Moon sticker">
      </div>
    </aside>

   <div class="right">

   <div class="banner">
        <span>‹ · · HOW LONG ARE YOU GOING TO KEEP THIS BIT UP ? ›</span>
        <button class="copy" id="copyButton"
          aria-label="Copy profile link" title="Copy profile link">▢</button>
      </div>
      
   <div class="intro">
        <div class="aliases">
          · ☻ &nbsp;<span>fies</span>
          &nbsp;<span>rui</span>
          &nbsp;<span>ronin</span>
        </div>

  <p class="pronouns">int c+h semi-verbal ˚z .</p>
      </div>

  <div class="squiggle">━━━━━━━ ❦ ━━━━━━━</div>

   <nav class="links">
        <a href="#about">ATABOOK</a>
        <a href="#friends">STRAWPAGE (WIP)</a>
        <a href="#pronouns">PRONOUNS</a>
      </nav>

  <div class="callout">
        !! heavy dni boundary breakers !!
      </div>

  <div class="squiggle">━━━━━━━ ❦ ━━━━━━━</div>

   <section class="friends" id="friends">
        <strong>the chunguses:</strong>
        <a href="#">@ViLeyn</a>
        <a href="#">@BackstageAlchemist</a>
        <a href="#">@puppyfes</a>
        <a href="#">@WhispyVibez</a>
        <a href="#">@Emu0312</a>
        <a href="#">@theconqueringprotagonista</a>
      </section>

   <div class="squiggle">━━━━━━━ ❦ ━━━━━━━</div>

   <div class="art-row" id="about">
        <div class="note">
          currently collecting silly little trinkets,
          listening to the same song for 6 hours,
          and making this page look pretty.
          <br><br>
          ✧ thanks for stopping by ✧
        </div>

       <!-- CC BY-SA OpenMoji illustration placeholder -->
   <img class="duo"
          src="https://cdn.jsdelivr.net/gh/hfg-gmuend/openmoji/color/svg/1F46B.svg"
          alt="Two-person illustration placeholder">
      </div>

   </div>
  </div>

  <footer class="bottom" id="pronouns">
    <div class="squiggle">୨୧ · · ✦ · · ୨୧ · · ✦ · · ୨୧</div>
    <div class="small-links">
      <a href="#about">about me</a>
      <a href="#friends">my friends</a>
      <a href="https://github.com/">github</a>
      <span>creds: OpenMoji / CC BY-SA 4.0</span>
    </div>
  </footer>

</main>

<script>
document.getElementById("copyButton").addEventListener("click", async () => {
  const button = document.getElementById("copyButton");

  try {
    await navigator.clipboard.writeText(window.location.href);
    button.textContent = "✓";
    button.title = "Link copied!";
  } catch {
    button.textContent = "!";
    button.title = "Copy the URL from your browser address bar.";
  }
});
</script>
</body>
</html>
