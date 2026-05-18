# Think Backwards — categories

Downloadable category packs for **[Think Backwards](https://www.thinkbackwards.app/)**, an offline-first gameshow-style hot-seat trivia game.

The app ships with a built-in set of categories. This repo hosts extra packs you can pull into the app on demand — animal trivia, art history, mythology, more being added over time.

---

## Currently available

| File | Category | Questions |
|---|---|---|
| [`animals.json`](animals.json) | Animals | 25+ |
| [`art.json`](art.json) | Art | 25+ |
| [`geography.json`](geography.json) | Geography | 25+ |
| [`history.json`](history.json) | History | 25+ |
| [`literature.json`](literature.json) | Literature | 25+ |
| [`mythology.json`](mythology.json) | Mythology | 25+ |
| [`science.json`](science.json) | Science | 25+ |
| [`technology.json`](technology.json) | Technology | 25+ |

Each pack covers all five gameshow-style difficulty tiers ($100–$1000 equivalent).

---

## How to use these in the app

1. Open Think Backwards at [thinkbackwards.app](https://www.thinkbackwards.app/) (or your installed version).
2. Go to **Settings → Categories → Available** tab.
3. The list pulls from this repo automatically. Pick a pack and tap **Install**.
4. Picked packs appear in the **Installed** tab and are usable in any game setup.

To point the app at a fork of this repo (your own custom packs), use **Settings → Categories → Remote source** and enter your `user/repo` slug.

---

## File format

Each `.json` file in this repo is a single category pack. The shape:

```json
{
  "id": "animals",
  "name": "Animals",
  "description": "Critters of every kind — feathered, finned, furred, and frankly weird.",
  "version": 2,
  "questions": [
    {
      "id": "animals-1-1",
      "difficulty": 1,
      "question": "The fastest land animal.",
      "answer": "Cheetah"
    }
  ]
}
```

### Field rules

| Field | Type | Rule |
|---|---|---|
| `id` | string | kebab-case (`a-z`, `0-9`, `-`). Must be unique across packs. |
| `name` | string | Display name shown in-app. |
| `description` | string | Optional one-line blurb. |
| `version` | integer | Bump to push updates to installed users. The app re-fetches packs whose `version` is higher than the one cached. |
| `questions[]` | array | At least **25** questions; at least **1** per difficulty tier (1–5). |
| `questions[].id` | string | Convention: `<category-id>-<difficulty>-<slot>`. Must be unique within the pack. |
| `questions[].difficulty` | integer | 1–5, mapping to the five gameshow-style value tiers. |
| `questions[].question` | string | The clue. Declarative form preferred (the app's tone). |
| `questions[].answer` | string | The canonical answer. |
| `questions[].acceptedAnswers` | string[] | Optional. Extra accepted answers for grading flexibility (e.g. `"USA"` for `"United States"`). |

The app validates every download against this schema; malformed packs are rejected with a readable error.

---

## Contributing

PRs welcome — especially new categories. Quick guide:

1. Fork this repo.
2. Add or edit a `<category>.json` file at the repo root.
3. Match the format above. **Avoid true/false questions** and **prefer declarative wording** (e.g. *"The fastest land animal."* rather than *"What's the fastest land animal?"*).
4. Bump the pack's `version` field if you're editing an existing pack so installed users get the update.
5. Open a PR. Once merged, the pack is live for anyone who opens the **Available** tab.

If you're not sure about a question's wording or difficulty, open an issue first and we'll sort it.

---

## Reporting issues with question content

Open an [issue](../../issues) describing:
- The pack and question id (e.g. `animals-3-2`).
- What's wrong (incorrect answer, outdated, ambiguous wording, etc.).
- The corrected version if you have one.

For app bugs (not question content), file those at the [main installers repo](https://github.com/SenalKaranda/ThinkBackwardsPWA) or email **catdadstudios@gmail.com**.

---

## License

Question content is contributed by volunteers and is intended for use within Think Backwards. If you want to reuse this content elsewhere, please check the source of any specific question — many are common knowledge but some may have come from copyrighted material and would need attribution.
