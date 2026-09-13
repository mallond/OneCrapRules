
# The Last Lantern â€” A Dice Dungeon

**Seven chambers. Three stolen seals. One dwindling lantern.**

A solo browser adventure played with a physical set of polyhedral dice. You make the choices and enter your rolls; the game handles combat, supplies, treasure, and the expedition journal.

[**Play The Last Lantern**](https://mallond.github.io/OneCrapRules/dnd/TheLastLantern/)

*One adventurer. About 15â€“25 minutes. One very questionable map.*

## The story

Every morning, the village gets darker. Someone has hidden the dawn beneath the old well. Tonight, you go looking.

Descend through seven chambers, recover the three dawn seals, and defeat the Keeper of Borrowed Dawn. Along the way, youâ€™ll find creatures, traps, treasure, healing springs, and lantern shrines.

The dice do not care that you have a plan.

## What you need

- A modern browser on a computer, tablet, or phone.
- A standard seven-piece dice set: d4, d6, d8, d10, d12, d20, and a percentile tens die.
- A willingness to occasionally blame small plastic objects for your decisions.

No account, installation, game master, or D&D rulebook is required. The interface asks for manually entered results; it does not roll virtual dice for you.

## Quick start

1. Open the game and select **Enter the well**.
2. Roll the die requested on screen.
3. Enter the result and select **Submit roll**, or press **Enter**.
4. When offered a choice, choose a bold or careful approach.
5. Resolve the encounter, then descend to the next chamber. Drink your potion between chambers when needed.
6. Recover the seals in chambers **2, 4, and 6**, then face the Keeper in chamber **7**.

Select **How to play** for the full in-game rules. The journal records rolls, outcomes, and discoveries as you go.

## Your expedition

| Resource | Starting amount | What it does |
|---|---:|---|
| Vitality | 20 | Your health. At 0, the expedition ends. Maximum 20. |
| Lantern fuel | 10 | Each descent costs 1. At 0, the expedition ends. Maximum 10. |
| Healing potion | 1 | Heals a d12 between chambers, up to maximum vitality. |
| Dawn seals | 0 | Earn one when you resolve chamber 2, 4, or 6. |
| Gold | 0 | Treasure and a contribution to your final score. |

Choosing to drink consumes the potion before its healing roll. It is unavailable at full vitality. There is no shop or gold-spending mechanic.

## The dice

| Die | Job in this game | Personality |
|---|---|---|
| **d4** | Damage you suffer after a failed check | The dungeonâ€™s smallest complaint form. Surprisingly sharp. |
| **d6** | Encounter type; fuel restored at a shrine | Chooses between hospitality and teeth. |
| **d8** | Damage you deal on a successful attack | Your swordâ€™s performance review. |
| **d10** | Treasure found after combat or in a cache | Loose change with dramatic lighting. |
| **d12** | Healing from a spring or potion | Finally invited to the party. Brought medicine. |
| **d20** | Attack and trap checks | Decides whether your plan was â€œbrilliantâ€ or â€œa learning experience.â€ |
| **d100** | Final relic and its gold reward | The victory gift shop. |

For a percentile roll, roll the tens die and ordinary d10 together. **40 + 7 = 47**, **00 + 7 = 7**, and **00 + 0 = 100**. Enter the combined result from **1â€“100**.

## Encounters

In chambers 1â€“6, roll a d6 to discover what waits:

| d6 | Encounter | Resolution |
|---|---|---|
| 1â€“2 | Creature | Choose your approach, then fight. Victory leads to treasure. |
| 3 | Trap | Choose your approach, then make one check. A failure costs d4 vitality; surviving clears the trap. |
| 4 | Cache | Gain d10 + twice the chamber number in gold. |
| 5 | Spring | Recover d12 vitality, up to 20. |
| 6 | Lantern shrine | Recover d6 fuel, up to 10. |

The seventh chamber always contains the Keeper, with **18 vitality**.

### Bold or careful?

- **Go bold:** Spend no extra fuel. Survive and complete the encounter for **5 bonus gold**.
- **Go carefully:** Spend **1 fuel** for **+3 to every d20 check in that encounter**. Requires at least 2 fuel when chosen.

Careful costs fuel once per encounter, not once per roll. Leave enough fuel for the remaining descents: reaching zero ends the expedition immediately.

### Combat and traps

The target is **9 + the chamber number**.

- Roll **d20 + your approach bonus**. Meet or exceed the target to succeed.
- A **natural 1 always fails**, regardless of bonuses.
- A **natural 20 always succeeds**. In combat, it also doubles your next d8 damage roll.
- On an attack hit, roll **d8 damage**. Repeat attacks until the creature reaches 0 vitality.
- On a missed attack, roll **d4 damage against yourself**. The creature only retaliates after a miss.
- A trap requires one check. On failure, suffer d4 damage; if you survive, the chamber is still completed.

Ordinary creatures have **4 + the chamber number** in vitality. Defeating one earns a treasure roll.

## Victory and defeat

Recover all three seals and defeat the Keeper to reach the final percentile roll. That roll reveals your relic and adds its value in gold.

Your victory score is:

```text
Gold + (25 Ã— seals) + remaining vitality + (5 Ã— remaining fuel)
```

If vitality or lantern fuel reaches zero, the expedition ends. You can begin another with **New expedition** or the ending screenâ€™s replay button.

**Progress lasts only while the page stays open.** Refreshing or reopening the page starts over. There is no saved game, persistent leaderboard, or journal export.

## Run locally

The complete game lives in **`index.html`**, including its CSS and JavaScript.

1. Download `index.html` from this folder.
2. Open it directly in a modern browser.
3. Play offline.

No npm packages, build step, server, API keys, or external assets are required.

To host your own copy, serve `index.html` through a static host such as GitHub Pages. Put this README alongside the HTML file in the gameâ€™s folder.

## Inside the code

The app uses plain HTML, CSS, and JavaScript, with responsive layouts and labeled controls.

| Function or value | Purpose |
|---|---|
| `s` | Current expedition state: health, fuel, chamber, inventory, and journal. |
| `fresh()` | Start a new expedition. |
| `act(action)` | Process choices such as descending, drinking, or selecting an approach. |
| `dieSize()` | Return the die required by the current phase. |
| `submit(value)` | Validate and resolve a roll. |
| `complete()` | Finish an ordinary encounter and award applicable seals and bonuses. |
| `dead()` | Check whether vitality or fuel has run out. |
| `render()` | Update the interface from the game state. |

The page also conditionally registers two WebMCP tools when `document.modelContext.registerTool` is available: `read_expedition` and `submit_physical_roll`. Normal browser play does not require WebMCP support.

This is a client-side, honor-system solo game. Enter your actual rollsâ€”or experiment with the code. There is no server validating the results.

## About

Created through a collaboration between David Mallon and ChatGPT: a small experiment in turning a handful of dice into a complete adventure.

The Last Lantern is an original game using familiar polyhedral dice. It is not an official Dungeons & Dragons product and does not implement the D&D ruleset.

*Writing the dungeon does not qualify you to survive it.* ðŸŽ²
