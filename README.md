# worldcuptracker
Track your fav teams and players thru the world cup

⚽ World Cup 2026 Family Tracker
A kid-friendly, Pokémon-card-style World Cup 2026 tracker you build with AI and follow with your family. Every player becomes a holographic trading card (HP = stamina, MP = position-aware skill, plus a quirky signature move); group standings auto-rank, and a knockout bracket fills in as the tournament unfolds.
Built in an afternoon with Cowork in the Claude desktop app — and you can build your own in a few minutes with the prompt below.

Try it

Download world-cup-2026-tracker.html and double-click it — it opens in any browser, no install, no internet needed.
Live demo: (optional — if you enable GitHub Pages, link it here, e.g. https://<your-username>.github.io/world-cup-2026-family-tracker/world-cup-2026-tracker.html)


The downloadable file is a snapshot — scores are frozen at export time. Re-export from your own Cowork session to refresh, or build your own copy (below) and let its daily updater keep it current.


Build your own (copy-paste into Cowork)

Open the Claude desktop app and start a Cowork session.
Edit the two lines in the CUSTOMIZE ME block (your favorite teams + your timezone).
Paste the prompt below and send it.
Answer any clarifying questions, then let it research and build (a few minutes).
Ask it to set up the daily auto-update and to hand you the standalone .html to share.


Requires the Claude desktop app with Cowork enabled (it needs web search + the ability to create a live artifact and a scheduled task). It won't fully work from the plain web chat.

The prompt
Build me a World Cup 2026 family tracker as a single self-contained HTML artifact —
a fun, visual app I can follow with my kids and share with others. Treat visuals as
a priority; the audience includes children.

=== CUSTOMIZE ME ===
- My favorite teams (give these full 26-man squads + a dedicated outlook): South Korea, USA, New Zealand, France
- My timezone for the daily update: America/Detroit (8am local)
====================

RESEARCH FIRST (don't trust memory — the tournament is current):
- Web-search the official 2026 World Cup final draw: all 12 groups (A–L), 48 teams.
- Web-search the confirmed final squads. Pull FULL 26-man squads for my favorite teams
  above (cross-check against 2+ reliable sources e.g. FIFA.com, ESPN, Wikipedia squads page).
- For every OTHER team, you only need ~5 recognizable star players.
- Confirm the tournament dates and that standings start empty if it hasn't kicked off yet.

CARD MODEL (this is the heart of it — make the stats credible, not random):
- Every player is a Pokémon-style holographic trading card with:
  • HP = stamina / engine (work rate, running, durability). Box-to-box mids and flying
    fullbacks score high; aging playmakers and pure poachers lower. Scale 1–99.
  • MP = skill FOR THEIR POSITION (a keeper's MP = shot-stopping, a defender's = reading
    the game, a forward's = finishing & flair). Judge each player against their own job, not
    across positions. Scale 1–99.
  • A SIGNATURE MOVE — the real thing that player is famous for, written with a bit of humor
    (quirkier the better, but recognizable to someone who actually follows soccer).
  • Rarity by skill: Legendary (gold holo) 90+, Epic (purple) 80–89, Rare (blue) 70–79,
    Common (grey) below 70.
  • Position type-colors: GK amber, DF blue, MF green, FW red.
  • A unique procedurally-generated cartoon AVATAR per player drawn as inline SVG
    (varied face/hair/skin seeded from the name, wearing the team's kit colors; keepers in a
    distinct kit). Do NOT use real photos — external images won't load in the artifact and
    base64-embedding hundreds of headshots is impractical. Cartoon avatars keep it light and
    self-contained.
- Hand-tune the stats so they pass the eye test (e.g. a 38-year-old superstar might be low HP
  but near-max MP). Add a note that stats are opinions, not official ratings.

VIEWS / TABS:
1. Groups — all 12 group tables, auto-ranked (P, W, D, L, GF:GA, Pts), top 2 highlighted as
   qualifying. Tables must AUTO-COMPUTE from a simple results array (so updates only need new
   scores added). Remember 2026's format: top 2 of each group PLUS the 8 best 3rd-place teams
   advance to a Round of 32. Add a hover tooltip on each team showing its star rating + a
   strength tier.
2. Our Teams — a dedicated tab for my favorite teams. For each: a game-by-game GROUP PATH
   (each opponent with a color-coded target — win / draw-or-better / nick-a-point / survive —
   and a one-line why, plus that opponent's star rating), an honest "what it takes to advance/
   win the group" read that uses the real format, an honest "how far can they realistically go"
   ceiling, and tappable player chips that open the card. Keep the takes straight and credible,
   not hype.
3. Teams & Cards — a grid of all 48 teams (flag, group, a 1–5 star strength rating). Tap a team
   to see its squad as cards; tap a card to zoom it full-size.
4. Bracket — the knockout bracket (R32 → R16 → QF → SF → Final) with placeholder slots that
   fill in after the group stage.
5. How it works — a short explainer of the stats and how updates happen.

TEAM STARS: give each of the 48 teams a 1–5 star strength rating (halves allowed) reflecting
realistic tournament strength.

DATA DESIGN: keep match results in a simple array of {group, home, away, homeScore, awayScore}
and the knockout bracket in an editable structure, so future updates just append scores and the
standings/bracket recompute. Standings start empty if the tournament hasn't begun.

LOOK & FEEL: bright, glossy, collectible, kid-magnetic, but clean. Light background, works on
desktop and phone. Single self-contained HTML file (inline all CSS/JS, SVG for art) so it can be
shared and opened by double-clicking — no install, no internet needed.

AFTER BUILDING:
- Save it as a live artifact AND give me the standalone .html file to share with others.
- Set up a scheduled task that runs once each morning in my timezone: web-search finished match
  results since the last update, append them, recompute standings, advance the bracket, update a
  "last updated" stamp, and post a short family-friendly recap. The task must AUTO-SUNSET after
  the final (do nothing once the tournament is over).
- Verify before finishing: every group team has metadata and players, no missing/duplicate teams,
  no out-of-range stats, and the favorites' group-path opponents exactly match their real groups.

Customizing further (just ask Cowork after it builds)

"Add Brazil and Argentina to Our Teams too."
"Flesh out the full Japan squad." (turn any team's 5 stars into a full 26-man squad)
"Make the cards a Panini sticker-album style instead."
"Add a player search box."
"Give me a fresh .html export." (snapshots aren't live — re-export to re-share current scores)
"Host it so I have one always-current link."

Honest caveats

The shared .html file is a frozen snapshot — only the original owner's Cowork copy auto-updates. Re-export to share fresh scores.
Flag emojis look perfect on Mac; some Windows setups show country codes instead of flags.
Card stats are hand-tuned opinions, not official ratings — that's the fun of it.


Made with Cowork in the Claude desktop app. Swap in your own teams and run it for your family.
