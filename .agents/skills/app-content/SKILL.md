---
name: app-content
description: Use for any content work in this app - researching, writing, extending, correcting or reviewing its competencies, chapters, pages, rounds, questions, exercises, figures, terms or sources. This app's own content decisions; they take precedence over the generic lernapps content skills. Load it before you change any content.
---

# Content guide of this app

## Curriculum

- **Subject & level:** German as a Foreign Language (`subject: daf`, strand `daf/grammatik`), CEFR **A1–B1** (learning map bands `5-6` through `9-10`, progressing naturally as Peter grows from age 12 in *Klasse 6* at A1 to 13–14 at A2 and 15 at B1).
- **Orientation:** Learning map `https://lernapps.net/apps/map/daf.json` (canonical source `lernapps/apps/map/daf.yaml`, based on ZfA/KMK *Rahmenplan DaF*, Goethe-Institut / ÖSD / telc A1–B1, and CEFR Companion Volume 2020) and build brief `lernapps/apps#875` (part of overview epic `lernapps/apps#887`).
- **Standard variety:** Standard German as used in Germany (*Bundesdeutsch*) only — Austrian and Swiss everyday specialties are excluded so learners build a consistent foundation.
- **Languages:** `languages: [de, en]` (`de` first per `@lernapps/app-templates 0.20.0`, full English UI tree at `/en/`).

## Competencies

### Chapter 1: `genus-plural-negation` — Gender, Plurals and Negation (A1 · 5–6)
- Recap page: `src/genus-plural-negation/vorwissen.yaml` (`recap: [daf/personalpronomen-nominativ, daf/verb-zweitstellung]`) — exercises: `recap-verb-pronomen`.
1. `artikel-genus` (*Ich kann bestimmte (der, die, das) und unbestimmte (ein, eine) Artikel im Nominativ richtig verwenden.*) → `src/genus-plural-negation/artikel-genus.yaml` (`artikel-genus-zuordnen`, `artikel-zimmer-wahl`, `genus-endung-check`, `artikel-ein-luecken`).
2. `pluralbildung` (*Ich kann häufige deutsche Pluralformen bilden und mit dem Pluralartikel die verwenden.*) → `src/genus-plural-negation/pluralbildung.yaml` (`plural-muster-zuordnen`, `plural-schreiben`, `plural-artikel-regel`, `plural-ohne-endung-check`).
3. `negation-nicht-kein` (*Ich kann Nomen mit kein/keine und Verben, Adjektive oder ganze Sätze mit nicht verneinen.*) → `src/genus-plural-negation/negation-nicht-kein.yaml` (`negation-wahl`, `negation-wortstellung`, `negation-satz-ordnen`, `negation-luecken`).

### Chapter 2: `akkusativ-pronomen-possessiv` — Accusative, Pronouns and Possessives (A1 · 5–6)
4. `akkusativ-artikel` (*Ich kann bestimmte, unbestimmte und negative Artikel im Akkusativ für direkte Objekte verwenden.*) → `src/akkusativ-pronomen-possessiv/akkusativ-artikel.yaml` (`akkusativ-artikel-wahl`, `akkusativ-artikel-luecken`, `subjekt-oder-objekt`, `akkusativ-regel-check`).
5. `akkusativ-pronomen` (*Ich kann Personalpronomen im Akkusativ als direkte Objekte verwenden.*) → `src/akkusativ-pronomen-possessiv/akkusativ-pronomen.yaml` (`pronomen-nom-akk-zuordnen`, `akkusativ-pronomen-wahl`, `akkusativ-pronomen-ersetzen`, `akkusativ-sachen-check`).
6. `possessivartikel-nom-akk` (*Ich kann Possessivartikel im Nominativ und Akkusativ richtig verwenden.*) → `src/akkusativ-pronomen-possessiv/possessivartikel-nom-akk.yaml` (`possessiv-besitzer-zuordnen`, `possessiv-nom-akk-wahl`, `possessiv-nom-akk-luecken`, `possessiv-euer-check`).

### Chapter 3: `dativ-verben-reflexiv` — Dative Case, Verbs and Reflexive Pronouns (A2 · 7–8)
7. `dativ-artikel` (*Ich kann bestimmte, unbestimmte und negative Artikel im Dativ einschließlich Dativ Plural -n verwenden.*) → `src/dativ-verben-reflexiv/dativ-artikel.yaml` (`dativ-spalten-zuordnen`, `dativ-artikel-wahl`, `dativ-plural-luecken`, `dativ-plural-s-check`).
8. `dativ-pronomen` (*Ich kann Personalpronomen im Dativ sicher verwenden.*) → `src/dativ-verben-reflexiv/dativ-pronomen.yaml` (`pronomen-nom-dat-zuordnen`, `dativ-vs-akk-pronomen-wahl`, `dativ-pronomen-luecken`, `dativ-ihnen-gross-check`).
9. `verben-mit-dativ` (*Ich kann häufige Dativverben wie helfen, gefallen, gehören, danken, schmecken und passen verwenden.*) → `src/dativ-verben-reflexiv/verben-mit-dativ.yaml` (`dativverben-auswaehlen`, `dativverben-luecken`, `dativverb-erkennen`, `dativverb-satz-ordnen`).
10. `dativ-und-akkusativ` (*Ich kann Sätze mit Empfänger im Dativ und Sache im Akkusativ in der richtigen Reihenfolge bilden.*) → `src/dativ-verben-reflexiv/dativ-und-akkusativ.yaml` (`zwei-objekte-ordnen`, `zwei-pronomen-wahl`, `zwei-objekte-luecken`, `zwei-pronomen-regel-check`).
11. `possessivartikel-dativ` (*Ich kann Possessivartikel im Dativ sicher anwenden.*) → `src/dativ-verben-reflexiv/possessivartikel-dativ.yaml` (`possessiv-dativ-wahl`, `possessiv-dativ-luecken`, `possessiv-dativ-check`, `possessiv-dativ-ordnen`).
12. `reflexive-verben` (*Ich kann häufige reflexive Verben mit Akkusativ- und Dativ-Reflexivpronomen verwenden.*) → `src/dativ-verben-reflexiv/reflexive-verben.yaml` (`reflexiv-verben-zuordnen`, `reflexiv-luecken`, `reflexiv-dativ-erkennen`, `reflexiv-akk-dat-wahl`).
13. `demonstrativ-indefinitpronomen` (*Ich kann dieser, welcher, jeder sowie man, jemand, niemand, etwas und nichts im Kontext verwenden.*) → `src/dativ-verben-reflexiv/demonstrativ-indefinitpronomen.yaml` (`demonstrativ-wahl`, `indefinit-bedeutung-zuordnen`, `indefinit-luecken`, `indefinit-verbform-check`).

### Chapter 4: `genitiv-n-deklination` — Genitive Case and Weak Masculine Nouns (B1 · 9–10)
14. `genitiv-artikel` (*Ich kann den Genitiv für Besitz und nach wegen, trotz, während und statt verwenden.*) → `src/genitiv-n-deklination/genitiv-artikel.yaml` (`genitiv-praepositionen-zuordnen`, `genitiv-luecken`, `genitiv-besitz-check`, `genitiv-praep-wahl`).
15. `n-deklination` (*Ich kann häufige schwache maskuline Nomen außerhalb des Nominativ Singular mit -n/-en beugen.*) → `src/genitiv-n-deklination/n-deklination.yaml` (`n-deklination-wahl`, `n-deklination-luecken`, `n-deklination-unterscheiden`, `n-deklination-merkmale`).

## Content structure

- **Story world (fixed across all pages):** **Peter** moves to **Lindenberg** (central Germany, *Bundesdeutsch*) with his parents for a year, joining *Klasse 6* (age 12 at A1, growing naturally to 13–14 at A2 and 15 at B1) with class teacher **Herr Braun**, classmates **Lukas** (12 at A1) and **Nadia** (12 at A1), and family friends **Familie Weber** (**Frau Weber / Katrin**, **Herr Weber / Thomas**, **Lukas**, **Mina** age 9 at A1). Scenes belong to an age-appropriate everyday world (setting up Peter's room in his parents' apartment, school, backpack, football, bicycle, gifts for Familie Weber, pets, neighborhood party).
- **Recurring visual model:** The growing **4-Case Color Table** (*4-Fälle-Farbtabelle*, adding one row per chapter: Nominative → Accusative → Dative → Genitive), **Stand-in Cards** (*Stellvertreter-Karten*), the **Dative/Accusative Arrow Diagram**, and the **n-Declension Pattern Card**.
- **Page flow (1 competency per page):**
  1. Opening section: concise Lindenberg scene introducing the rule with SVG figure / table / note / vocabulary block (every German noun with its article).
  2. Practice section (`uebung`): **4 varied exercises** progressing from recognition/matching to active gap-fill/ordering/transfer, catching classic English-speaker traps (masculine accusative `den/einen`, gendered thing pronouns `der Rucksack → ihn`, `euer → eure/euren`, dative plural `-n`, `gefallen` subject swap, reflexive `mich/mir`, weak masculine `-n/-en`).
- **Chapter self-assessment:** Each `chapter.yaml` defines `selfAssessment` drawing 1–2 self-contained exercises per competency page (6 + 6 + 7 + 4 = 23 total across 7 steps; recap page `vorwissen` excluded).

## Terminology

- **Address to learners:** Informal *you* in English (`en`) and informal *du* in German (`de`) throughout.
- **Terms used:** Plain-language labels paired with standard German terms (*Nominativ / Wer? Was?*, *Akkusativ / Wen? Was?*, *Dativ / Wem?*, *Genitiv / Wessen?*, *Genus*, *Plural*, *Possessivartikel*, *Reflexivpronomen*, *n-Deklination / schwache maskuline Nomen*). Every German noun is introduced with its article (*der Rucksack, die Gitarre, das Fahrrad*).
- **Standard German (*Bundesdeutsch*):** *Brötchen*, *Fahrrad*, *Regal*, *Rucksack*, *Schreibtisch*, *Hausaufgaben*.
- **Avoided:** Host-family / exchange-student / language-school framing; inline backticks in prose; unexplained linguistic jargon; Austrian/Swiss regionalisms.

## Exercise patterns

- **Pattern 1 — Guided selection (`language-task`, `mode: choice`):** `languages: { source: en, target: de }`, plain English `source`, German `[gap]` with targeted `distractors` testing case/gender contrasts (e.g. `src/genus-plural-negation/artikel-genus.yaml`, `artikel-zimmer-wahl`).
- **Pattern 2 — Active form production (`language-task`, `mode: gap`):** `form: { case: hint, punctuation: ok }`, plain English `source` naming base noun/gender, German `[gap]` target, plus rule-based `mistakes` catching exact learner errors (e.g. `src/akkusativ-pronomen-possessiv/akkusativ-artikel.yaml`, `akkusativ-artikel-luecken`).
- **Pattern 3 — Mapping & pairing (`matching`):** Connect articles, owners, pronouns, reflexive verbs, or genitive prepositions to their matching forms/meanings (e.g. `src/dativ-verben-reflexiv/dativ-pronomen.yaml`, `pronomen-nom-dat-zuordnen`).
- **Pattern 4 — Word-order assembly (`ordering`):** Assemble negated sentences, dative-verb clauses, or two-object sentences (e.g. `src/dativ-verben-reflexiv/dativ-und-akkusativ.yaml`, `zwei-objekte-ordnen`).
- **Pattern 5 — Rule & misconception checks (`single-choice`, `multiple-choice`, `true-false`):** Diagnostic questions where every option carries a rule-based `info` (e.g. `src/genitiv-n-deklination/n-deklination.yaml`, `n-deklination-unterscheiden`).
- Every competency page has **4 varied exercises** (≤ 2 guessable choices, ≥ 2 active tasks).

## Figures

- **Self-drawn inline SVGs (`src/images/*.svg`):** 7 figures (`case-table-ch1.svg`, `case-table-ch2.svg`, `case-table-ch3.svg`, `case-table-ch4.svg`, `standin-pronouns.svg`, `dative-accusative-arrows.svg`, `n-declension-card.svg`).
- **Dimensions & readability:** `viewBox="0 0 340 <h>"` (1:1 crisp legibility at 360 px mobile width), minimum 10.5–13.5 px font sizes, ≥ 28 px empty bottom margin so the runtime's `© CC0-1.0` badge never overlaps text or borders.
- **Color & contrast convention (≥ 4.5:1 in light and dark mode):** Neutral card `#f8fafc` with `#cbd5e1` border and `#0f172a` text; masculine blue (`#dbeafe` / `#1e3a8a`), feminine rose (`#ffe4e6` / `#9f1239`), neuter green (`#dcfce7` / `#14532d`), plural/dative amber (`#fef3c7` / `#78350f`), genitive violet (`#ede9fe` / `#4c1d95`).
- **Origin, licence & pedagogy:** `source: { de: "Eigene Zeichnung", en: "Own drawing" }`, `licence: CC0-1.0`. Every figure illustrates a model pattern and never leaks exercise answers (`dative-accusative-arrows.svg` uses `der Freundin / ein Spiel`; `n-declension-card.svg` uses `der Junge / der Löwe`).

## Sources

- `https://lernapps.net/apps/map/daf.json` (canonical `lernapps/apps/map/daf.yaml`) — verified.
- `lernapps/apps#887` (DaF explainer overview) and `lernapps/apps#875` (build brief for *Nouns, Pronouns and the Four Cases*) — verified.
- Standard CEFR A1–B1 grammar scope per ZfA/KMK *Rahmenplan DaF* and Goethe-Institut / ÖSD / telc A1–B1.
- No private creator material is committed.

## Adding a chapter or round

1. Check `https://lernapps.net/apps/map/daf.json` for competency ids and `requires`.
2. Create `src/<chapter-id>/chapter.yaml` and one YAML file per competency (plus a compact `recap` page first if external prerequisites are needed).
3. Register `<chapter-id>` in `src/app.yaml` (`chapters`).
4. Follow the 4-exercise pattern and `340 px` `CC0-1.0` SVG conventions above; 1 bis 3 ihrer Übungen in `selfAssessment` aufnehmen, wie Skill `lernapps-explainer-self-assessment` sagt.
5. Update this content guide, run `npx vp check --fix`, `npx vp build`, and `npx --no -- lernapps check`, then commit on a feature branch.

## Rules learned from mistakes

- Protagonist is **Peter**, moving to Lindenberg **with his parents** (age 12 in *Klasse 6* at A1, growing to 13–14 at A2 and 15 at B1), with family friends **Familie Weber** — never "Sam", never "Gastfamilie / host family / Gastbruder".
- SVGs must use `viewBox="0 0 340 <h>"` (never `640` wide) with ≥ 28 px empty bottom margin so text stays crisp at 360 px and the `© CC0-1.0` badge never overlaps content.
- Figure metadata must always use `source: { de: "Eigene Zeichnung", en: "Own drawing" }` and `licence: CC0-1.0`.
- Apply n-declension accurately even in surrounding prose and sentences (e.g., *von Herrn Weber*, never *von Herr Weber*).
- Keep figure examples distinct from gap-fill answers (e.g., `der Junge / der Löwe` on `n-declension-card.svg`, `der Freundin / ein Spiel` on `dative-accusative-arrows.svg`) so figures never leak answers.
- Every competency page needs 4+ varied exercises (≤ 2 guessable choices, ≥ 2 active tasks) and every chapter needs a `selfAssessment` block in `chapter.yaml` with self-contained exercises.
