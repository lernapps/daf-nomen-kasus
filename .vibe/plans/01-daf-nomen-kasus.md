---
# Read by the hooks, the review, the evals. Schema: @lernapps/tooling/guidance/plan-front-matter.v1.schema.json
# Written by `lernapps plan` and the hooks. Never change a key or a value by hand.
# Archetype, null until chosen in Explore. Allowed values: explainer, interactive, quiz.
archetype: explainer
# Current phase. Allowed values: explore, plan, code, commit.
phase: code
# prePushFailures: failed pre-push runs, written by the hook.
prePushFailures: 0
# failedChecks: failed rules and runs, written by lernapps check and the hooks.
failedChecks: { checks-pass: 1 }
---

# Plan: daf-nomen-kasus, first version

<!--
For you, the assistant. The process is in AGENTS.md; this plan holds the method.
- `npx --no -- lernapps plan next` prints the task to do now, `plan done` ticks it and prints the next one.
- You write only below Goal, Key decisions, Notes, Answers, Entry draft, Content method and Retrospective, in the
  creator's language. Delete the comment of a section once the section is filled.
- Work on the branch `work`, locally: push nothing before Commit.
-->

*Started 2026-11-26. Explore, Plan, Code, Commit.*

## Goal

English-speaking learners of German (CEFR A1–B1) follow Peter in Lindenberg as he sets up his room, goes to school, and chooses gifts for family friends Familie Weber, mastering German articles, noun gender, plurals, negation (*nicht/kein*), personal/possessive/reflexive/demonstrative/indefinite pronouns, all four cases (Nominative, Accusative, Dative, Genitive), and weak masculine nouns (n-declension).

## Key decisions

- **Archetype: `explainer` (format 2, `subject: daf`, `strand: daf/grammatik`).** Learners need structured explanations, a growing visual 4-Case Color Table, Stand-in Cards, vocabulary blocks, and 4 progressive exercises per competency page (`language-task`, `matching`, `ordering`, `single-choice`, `multiple-choice`, `true-false`).
- **Premise & variety: Lindenberg (*Bundesdeutsch*), age-appropriate family move.** Protagonist **Peter** moves to Lindenberg with his parents for a year, joining *Klasse 6* (age 12 at A1, growing to 13–14 at A2 and 15 at B1) with teacher **Herr Braun**, classmates **Lukas** and **Nadia**, and family friends **Familie Weber** (Katrin, Thomas, Lukas, Mina 9). No host-family or language-school framing.
- **Languages: `[de, en]` (`de` first, full English tree at `/en/`).** Required by `@lernapps/app-templates 0.20.0`.
- **Self-drawn mobile-first SVGs (`340 px` `viewBox`, `CC0-1.0`).** All 7 figures use `viewBox="0 0 340 <h>"`, ≥ 4.5:1 contrast, ≥ 28 px bottom clearance for the `© CC0-1.0` badge, and non-leaking model examples.
- **Chapter `selfAssessment` included in all 4 chapters.** Each `chapter.yaml` draws 1–2 self-contained exercises per competency page (23 total across 7 steps; recap page `vorwissen` excluded).
- **No `scope` in v1.** All exercises are auto-checked with no private creator material.

## Notes

- **Subject & strand:** `subject: daf`, `strand: daf/grammatik` (`lernapps/apps#875`, part of `lernapps/apps#887`).
- **Sources verified:** `https://lernapps.net/apps/map/daf.json` (canonical `lernapps/apps/map/daf.yaml`), `lernapps/apps#875`, `lernapps/apps#887`.
- **Chapters & competencies (15 competencies + 1 recap page):**
  - **Chapter 1 `genus-plural-negation` (A1 · 5–6):** `vorwissen` (`recap: [daf/personalpronomen-nominativ, daf/verb-zweitstellung]`), `artikel-genus` (der/die/das, ein/eine, gender clues; catches English article omission & ending confusion), `pluralbildung` (5 plural patterns + always *die*; catches *-s* overgeneralization & missing umlauts), `negation-nicht-kein` (*kein* vs. *nicht* & word order; catches *kein* before definite articles/adjectives).
  - **Chapter 2 `akkusativ-pronomen-possessiv` (A1 · 5–6):** `akkusativ-artikel` (only masculine changes `der/ein/kein → den/einen/keinen`; catches forgetting `-n` on masculine objects & relying on word order over case), `akkusativ-pronomen` (Stand-in Cards; catches using *es* for masculine/feminine things), `possessivartikel-nom-akk` (2-step owner + noun ending; catches `eueren` instead of `euren`).
  - **Chapter 3 `dativ-verben-reflexiv` (A2 · 7–8):** `dativ-artikel` (M-R-M-N + dative plural `-n`; catches missing `-n` on *Freunden/Kindern* and over-adding `-n` to *Fotos*), `dativ-pronomen` (Stand-in Cards Dativ; catches `mich/mir`, `sie/ihr`, lowercase `ihnen` vs. formal `Ihnen`), `verben-mit-dativ` (*helfen, gefallen, gehören, danken, schmecken, passen*; catches `gefallen` subject swap & accusative after `helfen`), `dativ-und-akkusativ` (Arrow Diagram 3 word-order rules; catches `ihr es` instead of `es ihr`), `possessivartikel-dativ` (`-em/-er/-en`; catches `seinen` instead of `seinem` & missing plural `-n`), `reflexive-verben` (`mich/mir`, `dich/dir` with 2nd object; catches accusative with body parts), `demonstrativ-indefinitpronomen` (`dieser/welcher/jeder` + `man/jemand/niemand/etwas/nichts`; catches `Mann` for `man` & plural verb with `man`).
  - **Chapter 4 `genitiv-n-deklination` (B1 · 9–10):** `genitiv-artikel` (`des/eines + -(e)s`, `der/einer`, `wegen/trotz/während/statt`; catches missing `-(e)s` on masculine/neuter & adding `-s` to feminine), `n-deklination` (weak masculine nouns `-n/-en` outside Nom. Sg.; catches omitting `-n` in Akk/Dat/Gen & over-applying to regular nouns like `der Lehrer`).
- **Scope:** In: all 15 competencies of `#875` across 4 chapters + 1 recap page, 7 mobile-first `340 px` SVGs, 4 varied exercises per competency page, chapter self-assessments, `languages: [de, en]`. Out: adjective declension (`#876`), verb tenses/conjugation (`#874`).
- **Gold-standard upgrade fixes applied:** Removed all host-family (`Gastfamilie`, `Gastbruder`, `Gast`) and old `sams-zimmer` references; fixed `von Herrn Weber` grammar in `n-deklination.yaml`; refactored all 7 SVGs from `640 px` to `340 px` with `CC0-1.0` & ≥ 28 px bottom clearance; expanded all 15 competency pages from 2 to 4 varied exercises; added `selfAssessment` to all 4 chapters.


## Explore

<!--
- Find out what the app teaches, for whom, how much and how it looks. Ask; write no code, run no `create`.
- An answer counts only in the creator's words under "Answers". At most 2 questions per message, one topic each.
-->

### Tasks

- [ ] Check the start: the folder `.agents/skills/lernapps-app` exists (else stop and tell the creator that the folder
      was not started with `init`), and `git branch --show-current` prints `work` (else `git switch -c work`).
- [ ] Load skill `lernapps-app`. Tell the creator in two sentences what a lernapps app is and where it will live: at
      their own address, free and public, and once listed as a copy on lernapps.net. Say that the technical part
      (GitHub) comes at the end and that you do it.
- [ ] Interview: ask the topics "Goal" and "Learners" of "Answers".
- [ ] Load skill `lernapps-map-assignment` and read the learning map of the subject as it says. The creator brings
      the content themselves (material, a word list, the pages): note under "Notes" which competencies of the map it
      covers. Else write the skill's assignment, with its story; the creator's yes answers the topics Content and
      Amount. A subject without a map: skip this task and say so.
- [ ] Load skill `lernapps-exercise-patterns` and read its reference for the subject. Note under "Notes" how learners
      will practise what the goal names.
- [ ] Choose the archetype as skill `lernapps-app` says: read the README of each archetype in question, then tell the
      creator in plain words what the chosen one can and cannot do. Write the archetype and its reason under "Key
      decisions".
- [ ] Run `npx --no -- lernapps skills --archetype <name>` with the chosen archetype. It installs the archetype's
      skills and adds the archetype's tasks to this plan.
- [ ] Load skill `lernapps-explainer-design`. An explainer has the look of the runtime: write "fixed by the
      archetype" under the topic "Look and feel" of "Answers".
- [ ] Interview: ask every other topic of "Answers", in order. Leave out only a topic that an answer of the creator
      already covers, and note which answer. A topic nobody answered is asked once before you write an assumption
      with "(guess)".
- [ ] Load skill `lernapps-content-research` and research as it says. Write under "Notes": the strand or subject, the
      competencies by chapter with their ids, the sources you opened.
- [ ] Write under "Notes" which competency goes on which page and which pages form a chapter, as "Map the content" of
      skill `lernapps-explainer-design` says. Per page, name the prerequisites the app does not practise.
- [ ] Write under "Notes", one line per competency: how learners get there (they derive it, they do not only read it
      off), and which misconception the feedback catches.
- [ ] Write under "Notes" the scope: what is in, what is out and why, the data range (for example "all main-group
      elements", never a silent "1–20"), the languages.
- [ ] **Checkpoint:** research. Show in plain words: the strand or why none, the competencies by chapter, the didactic
      approach, the scope, every "(guess)", the sources and what is unchecked, the archetype and its reason. Stop and
      wait. Changes: change them, then ask again.

### Answers

- Goal: Master German articles, gender, plurals, negation, pronouns, all four cases, and weak masculine nouns (n-declension) across CEFR A1–B1 (`lernapps/apps#875`).
- Learners: English-speaking learners of German as a Foreign Language (`subject: daf`), starting at age 12 (*Klasse 6*, A1) and progressing through A2–B1; builds on nominative personal pronouns and verb-second word order (`#874`).
- Model and focus: Modeled on `daf-hallo-lindenberg` and `daf-verben-grundlagen`; focus on clear visual models (growing 4-Case Color Table, Stand-in Cards) and 4 varied auto-checked exercises per competency page.
- Hurdles: English speakers drop articles, use *es* for gendered things, miss masculine accusative `-n`, forget dative plural `-n`, swap subject/object with *gefallen*, confuse reflexive `mich/mir`, and omit `-n/-en` on weak masculine nouns.
- Content: Written from verified learning map `map/daf.yaml` and issue brief `lernapps/apps#875`.
- Amount: Complete v1 covering all 15 competencies across 4 chapters + 1 recap page + 4 chapter self-assessments.
- Languages: German and English (`languages: [de, en]`).
- Look and feel: Fixed by the archetype (`explainer`, light and dark mode).
- Terms: Standard German grammar terms paired with plain-language explanations (*Nominativ / Wer?*, *Akkusativ / Wen?*, *Dativ / Wem?*, *Genitiv / Wessen?*, *4-Fälle-Farbtabelle*, *Stellvertreter-Karten*).
- Finding the app: German cases, der die das, accusative dative genitive, German pronouns, DaF Grammatik Nomen Kasus.

## Plan

<!--
- Map the confirmed content onto the archetype. No new content questions: a gap in the content goes back to Explore.
- The creator confirms the plan in one read. After the yes you work on your own.
-->

### Tasks

- [ ] Map the content as "Map the content" of skill `lernapps-explainer-design` says, and write the result under
      "Content method".
- [ ] Choose a pattern per competency as skill `lernapps-exercise-patterns` says, and add it to "Content method".
- [ ] Add to "Content method" one line per page, as "Engagement" of skill `lernapps-explainer-design` says: the
      opening task, the change of activity, the reward, the story.
- [ ] Add the tasks of Code, each one a piece of work that ends in a commit. First the pattern: one complete page or
      screen, `npx --no -- lernapps plan add --at pattern "<task>"`. Then the others, one call each:
      `npx --no -- lernapps plan add --at pages "<task>"`. Each task says what it builds and what it shows.
- [ ] Draw a sketch of each screen, component or interactive exercise: a static SVG or image, or the steps with what
      learners see after each. Keep the files in `.vibe/sketches/`.
- [ ] Show the creator, short: goal, competencies by chapter, the Code tasks, the sketches, and the content method in
      plain words (what learners see and do, what the app cannot do). At most 2 questions.
- [ ] **Checkpoint:** confirm the plan and the content method. Stop and wait for an explicit yes. Changes: change
      them, then ask again.

### Content method

- **Patterns:** Every competency page combines 4 varied exercises from `language-task` (`choice` & `gap` with targeted `mistakes`), `matching`, `ordering`, `single-choice`, `multiple-choice`, and `true-false` (≤ 2 guessable choices, ≥ 2 active tasks).
- **Figures & learning action:** All 7 SVGs (`340 px`, `CC0-1.0`) anchor visual memory without leaking answers: `case-table-ch1..4.svg` grow the 4-Case Color Table row by row so learners see exactly which cells change in each case; `standin-pronouns.svg` contrasts accusative (blue) vs. dative (amber) pronouns side by side; `dative-accusative-arrows.svg` visualizes recipient vs. thing roles and the 3 word-order rules; `n-declension-card.svg` contrasts base nominative singular against `-n/-en` in all other cases using `der Junge` / `der Löwe`.
- **Prerequisites & recap:** External prerequisites `daf/personalpronomen-nominativ` and `daf/verb-zweitstellung` (from `#874`) are consolidated on the compact opening recap page `src/genus-plural-negation/vorwissen.yaml`.
- **Adding a chapter:** Register in `src/app.yaml`, create `chapter.yaml` + competency pages following the 4-exercise and `340 px` SVG conventions, add `selfAssessment`, update `.agents/skills/app-content/SKILL.md`, and verify with `lernapps check`.

## Code

<!--
- Build the app, locally on `work`, on your own. After each task: `plan done`, then one commit with the work and this
  plan. The hooks check each commit; a failing check is fixed from its message, as skill `lernapps-cli` says.
- What you cannot decide: choose, write it under "Key decisions" with "(guess)", go on.
- The creator asks for a change: say your reading in one sentence first, then change every place it holds for
  (`feedback-applied-everywhere`).
-->

### Tasks

- [ ] Load skill `lernapps-cli`. Create the app as its section "Create" says:
      `npx --no -- lernapps create --archetype explainer`.
- [ ] Fill the content guide `.agents/skills/app-content/SKILL.md` from "Notes" and "Content method": every heading,
      no "FILL IN" left. Commit it before any content.
- [ ] Load skill `lernapps-explainer`.
- [ ] Load skill `lernapps-content-questions`. Read whole, with your file tool:
      `.agents/skills/lernapps-explainer/references/blocks.md` and
      `.agents/skills/lernapps-explainer/references/exercises.md`. A foreign language: also
      `references/language-tasks.md` in the same folder. A component in the plan: also `references/components.md`.
- [ ] Decide whether the app needs `scope`, as "`scope`" in
      `.agents/skills/lernapps-explainer/references/structure.md` says. Write the choice under "Key decisions".
<!-- tasks: pattern: the one page or screen that is the pattern for the others -->
- [ ] **Checkpoint:** the pattern page. Load skill `lernapps-learner-check` and do its learner check on the page. Fix
      what it finds. Then show the creator the page and ask whether the others may follow it. Stop and wait. A
      change: change the pattern first.
<!-- tasks: pages: the other pages or screens, after the pattern -->
- [ ] Update the content guide so that it describes the app as built (`app-content-matches`).
- [ ] Run `npx --no -- lernapps check` until it passes.
- [ ] Look at every screen and state, at 360 px and on a desktop, as "Look at the app" of skill `lernapps-cli` says.
      Compare each with its sketch.
- [ ] Do the whole-app check of skill `lernapps-learner-check`. Fix what it finds and write under "Notes" what you
      fixed.

## Commit

<!--
- Put the app on GitHub, publish it with the creator's yes, then list it. A push to `main` publishes.
- Open the pull requests (to `main`, to the catalog) without asking: they publish nothing.
- The creator asked to stop before publishing (a trial): stop here and say so.
-->

### Tasks

- [ ] Load skill `lernapps-explainer-self-assessment`. Add the self-assessment as it says, or write under "Key
      decisions" why the app has none. Commit.
- [ ] Load skill `lernapps-github`. Set up the repository and Pages as it says. Ask for the repository's name and
      every click only the creator can make, in one message.
- [ ] Push `work`, open the preview pull request and see its checks to green, as skill `lernapps-github` says.
- [ ] **Checkpoint:** publish. Show what the app does and the preview link from the comment "Vorschau der App". Ask
      whether it may go online. Stop and wait for the yes.
- [ ] Load skill `lernapps-commit`. Publish as skill `lernapps-github` says: `work` into `main` as one squash commit,
      the run of `Pages` watched to its end.
- [ ] Open the address the job `deploy` printed and confirm that the app shows. Never use a derived address.
- [ ] Load skill `lernapps-listing`. Write the entry under "Entry draft" as it says, with the creator's answer to
      "Finding the app".
- [ ] Fill the retrospective.
- [ ] Commit this plan on `main` and push it: the listing check and the review read it there.
- [ ] **Checkpoint:** list. Open the listing pull request as skill `lernapps-listing` says, without asking first: the
      pull request is the review. See it to "bestanden", then show the creator the pull request and its result.
- [ ] If the plan changed since its last push, commit it on `main` and push again.

### Entry draft

<!-- YAML valid against the entry schema the listing skill names. Only known values, never invented. -->

```yaml
```

## Retrospective

<!-- At the end of Commit, before the listing pull request. Facts, short, no names. Read by review and evals. -->

### Phases reached

<!-- Last phase completed, checkpoints passed. E.g. "commit; confirmed, published". -->

### Creator turns after the plan

<!-- Number of creator messages after the confirmation, topic of each. Target: at most 3. -->

### Where I had to guess

<!-- Each gap in plan, skills, messages or answers, and your choice. "None" if none. -->
