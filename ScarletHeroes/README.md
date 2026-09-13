# Scarlet Heroes â€” Play Tutor

**Learn the game by watching the Player and Game Master play it outâ€”one readable step at a time.**

[Open the Play Tutor](https://mallond.github.io/OneCrapRules/ScarletHeroes/)

An unofficial, player-focused training app for **Scarlet Heroes**, inspired by the **â€œPlaying the Gameâ€** chapter. Instead of asking you to memorize rules before playing, the tutor shows an intention, a GM ruling, a dice roll, and the resulting consequence.

Familiar dice. Unfamiliar damage rules. Fewer confused adventurers.

## Whatâ€™s inside

- **7 lessons with 3 variations each:** 21 scripted practice sequences.
- **Readable play logs** separating Player, Game Master, Dice & Result, and Rule Explained entries.
- **Visible arithmetic:** see which dice and modifiers apply, and how the result changes the scene.
- **Step-by-step or automatic playback**, with adjustable speed and pause controls.
- **Character status and HP** updated as the example unfolds.
- **A searchable glossary** with 64 entries covering acronyms, dice notation, and game terminology.
- **Clickable HD and AC** in scene descriptions for quick definitions.
- **Six character presets**, custom hero names, and a â€œSurprise meâ€ option.
- **A review question** at the end of each sequence.
- **Downloadable text logs** for rereading away from the app.
- **Printed book page references** alongside rule explanations.

## Lessons and variations

| Lesson | Variation 1 | Variation 2 | Variation 3 |
| --- | --- | --- | --- |
| Checks & exploration | Intent before dice | The sealed archive | The hidden sentry |
| Combat & the Fray die | A round, one beat at a time | The bridge ambush | Hold the floodgate |
| Saves & Defying Death | Danger, then a saving throw | The falling portcullis | The last ledge |
| Damage & healing | Each die tells its own story | Shards in the vault | Old wounds, fresh burns |
| Turning undead | The priest and the restless dead | The cemetery gate | The distant crypt guardian |
| Travel & encumbrance | The road has a cost | The road to the signal tower | The mountain rescue |
| Opposed checks at sea | A chase between captains | Escape under moonlight | Rain across the harbor |

The variations change situations, example rolls, consequences, and review questions. They demonstrate different applications of the same lessonâ€™s rules.

## How to use it

1. **Choose a lesson** from the navigation.
2. Select a **Practice variation**, or use **Try another variation** to cycle through its three examples.
3. Read the scene and character information. The first log entry appears automatically.
4. Press **Next step** to advance one entry, or **Auto-play** to watch at your chosen pace.
5. Follow the playerâ€™s intent, the GMâ€™s decision, the arithmetic, and the consequence.
6. Answer the review question when the sequence finishes.
7. Use **Save play log** to download the entries revealed so far.

**Restart** repeats the current variation. Changing variations resets that lessonâ€™s log and HP. Each sequence is a separate teaching example; injuries and adventure progress do not carry between lessons.

Uncheck **Follow newest entry** if you want to scroll back through the log without playback pulling you toward the latest entry.

### Looking up terms

Open **Glossary Â· Aâ€“Z** and search for a term such as `HD`, `AC`, `Fray`, or `saving throw`. You can also click **HD** or **AC** in the scene description.

Opening the glossary pauses auto-play. Close it with the Close button or **Escape**, then resume playback when you are ready.

### Choosing a character

Use **New character** to select a preset, enter a custom hero name, or choose **Surprise me**. Starting the session restarts the current lesson and updates names throughout its narration and exported logs.

Characters change identity and background; they **do not randomize stats or dice outcomes**. The fighter training build stays consistent so its worked equations remain accurate. The Turning Undead lesson uses the selected heroâ€™s cleric companion.

Character and variation selections are kept in memory for the current page session. Reloading the page resets them.

## How the simulations work

Both the Player and GM are **scripted locally in JavaScript**. Rolls are deliberately chosen teaching examples, not random rolls or live AI responses.

This makes it possible to replay the same event, inspect its arithmetic, and understand why it succeeded or failed. A selected variation follows its written sequence; the review questions provide feedback but do not branch the adventure.

The tutor covers selected aspects of the chapter, not the complete game. It does not include full character creation, an open-ended campaign engine, or every class ability and special rule. Consult the book for complete rules and use GM judgment where appropriate.

## Run locally

Download `index.html` and open it in a modern web browser.

Thatâ€™s it. The HTML, CSS, JavaScript, glossary, and scenarios are contained in **one file**. There are no packages to install, no build step, no API keys, and no backend. Once downloaded, the tutor runs offline.

## Publish with GitHub Pages

For this repository, the app belongs at:

```text
OneCrapRules/
â””â”€â”€ ScarletHeroes/
    â”œâ”€â”€ index.html
    â””â”€â”€ README.md
```

1. Place the latest app file at `ScarletHeroes/index.html`.
2. Commit and push it to the branch used by GitHub Pages.
3. Wait for the Pages deployment to finish.
4. Open the published page and refresh it.

If the download is named `scarlet-heroes-21-scenarios.html`, rename it to **`index.html`** before replacing the app file.

### Not seeing the variation controls?

The updated edition has **â€œ21 SCENARIOS Â· VARIATIONS EDITIONâ€** in its header. The **Practice variation** picker and **Try another variation** button appear below the lesson introduction, above the scene description.

Open your downloaded file directly first. If the controls appear locally but not online, confirm that you replaced the correct repository file and that GitHub Pages deployed the new commit. Then try a hard refresh: **Ctrl+F5** on Windows.

## Editing the tutor

Everything lives in `index.html`:

- The `<style>` section defines the appearance and responsive layout.
- `lessons` contains the seven original teaching sequences.
- `addedVariations` supplies two additional sequences per lesson.
- `lessonVariants` combines the originals and additions.
- `glossaryTerms` contains the searchable definitions.
- `characterPresets` contains the practice hero identities.

When changing a scenario, keep its narration, dice arithmetic, HP changes, review answer, and page references consistent. Avoid changing a heroâ€™s stats without also updating every example that depends on those stats.

## Credits and scope

**Scarlet Heroes** is by **Kevin Crawford / Sine Nomine Publishing**. Rule references in this tutor point to the bookâ€™s printed page numbers, primarily â€œPlaying the Game,â€ pp. 16â€“23.

This is an independent, unofficial learning aid, not an official product or a replacement for the rulebook. The tutorial scenes and dialogue are original teaching examples. The rulebook PDF is not bundled with the app.

Built collaboratively by **David Mallon and ChatGPT**, through questions, examples, and a healthy appreciation for dice.

*Describe what you want to do. Learn what to roll. See what happens next.*
