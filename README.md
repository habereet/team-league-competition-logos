\# team-league-competition-logos



Logo/crest/flag assets used by a set of scheduled Claude jobs that send me daily/weekly news updates about various teams, leagues, and competitions. These jobs `git clone` this repo fresh on every run and read this file first to find the current folder layout before assuming any path — \*\*if you restructure anything below, update this file in the same commit.\*\* That's the only place the layout needs to be documented; the jobs don't hardcode paths anywhere else.



\## Sources



\- NCAA, NBA, NFL, NHL, and MLB logos were obtained from \[Eagles SVG](https://eagles-svg.com/)

\- Soccer/Football logos and badges were obtained from \[Football Logos](https://football-logos.cc/)



\## Current layout



\- `MLB/{Team Name}.svg` — plus `MLB Logo.svg`, `American League Logo.svg`, `National League Logo.svg`

\- `NBA/{Team Name}.svg` — plus `NBA Logo.svg`

\- `NFL/{Team Name}.svg` — plus `NFL Logo.svg`

\- `NHL/{Team Name}.svg` — plus `NHL Logo.svg`. Some names use accented characters (e.g. `Montréal Canadiens.svg`).

\- `NCAA/{School Name}.svg`

\- `Soccer/Club Teams and Leagues/{Country}/{League Name}/{Club Name}.svg` — plus a `{League Name} Logo.svg` in most league folders. Full coverage for the Premier League; other leagues currently only have whichever clubs are in that season's UEFA Champions League — filling in over time.

\- `Soccer/Competitions/{Competition Name}.svg` — continental/international competition logos. Currently only has the UEFA Champions League's logo; Europa League, Conference League, World Cup, Euro, Copa América, etc. are not in here yet.



\## Not yet in this repo (planned)



\- National-team badges/flags for international tournaments (World Cup, Euros, Copa América, Olympics). Until these exist, the jobs fall back to the `flag-icons` npm package for country flags. \*\*Once a folder for these is added, name it clearly (e.g. `National Teams/{Country}.svg`) and document the exact path here\*\* — the jobs are written to prefer whatever's in this repo over the flag fallback, but only once they know where to look.

\- Olympics/Paralympics/Commonwealth Games emblems.



\## If you reorganize this repo



The jobs that read this repo don't have any other source of truth for its structure — they read this README fresh on every run. So the update sequence that keeps everything working is:



1\. Move/rename the files.

2\. Update the "Current layout" section above to match, in the same commit.



No separate update to any job's prompt should be needed — that's the whole point of routing through this file instead of hardcoding paths in each job.

