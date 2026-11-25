# Evidence Tests

**Find out how much your evidence actually proves.**

A Claude skill for researchers and writers in the humanities and social sciences. It takes the causal claims your argument rests on, sorts each piece of evidence by what it can and cannot show, and checks that every claim is stated at the strength its evidence supports.

Built on Stephen Van Evera's four process-tracing tests, as developed by David Collier, James Mahoney, Sherry Zaks, and Andrew Bennett and Jeffrey Checkel.

<img width="750" alt="Evidence Tests" src="assets/evidence-tests.jpg" />

[Download `evidence-tests.zip`](https://github.com/Halfofthesky/evidence-tests/releases/latest/download/evidence-tests.zip) · [View `SKILL.md`](evidence-tests/SKILL.md)

---

## When you need it

- You argue that something **caused** something: a reform, a war, a decline, a turn in someone's thinking.
- You claim an **influence**: that A read B, or that an idea reached the people who acted on it.
- You write "**shows**", "**proves**" or "**clearly**", and want to know whether your evidence earns those words.
- A reviewer says you **ignored an alternative explanation**, or that your evidence "is also consistent with" something else.
- Your argument leans on **what the record doesn't contain**.
- You're **planning research** and want to know which evidence would actually settle the question.

## Why you need it

Most evidence fits more than one story, and not all evidence weighs the same. Van Evera's point is that you can tell how much a piece of evidence weighs by asking two questions:

- **Would it have to be there if you're right?** If so, its absence hurts you.
- **Could anything else have put it there?** If not, its presence helps you.

The answers sort every piece of evidence into one of four tests:

| Test | Must it be there? | Could something else explain it? | If it's there | If it isn't |
|---|---|---|---|---|
| **Straw in the wind** | No | Yes | Slight support | Slight doubt |
| **Hoop** | Yes | Yes | Keeps the claim alive | Rules the claim out |
| **Smoking gun** | No | No | Confirms the claim | Some doubt |
| **Doubly decisive** | Yes | No | Confirms the claim, rules out rivals | Rules the claim out |

The accused was in town that day: a hoop. A smoking gun in his hand: a smoking gun. A bank camera that filmed the robbers' faces: doubly decisive, and rare. Most real evidence is straw in the wind.

The usual mistakes follow from this. Writers treat hoops as proof. They count evidence for their claim as evidence against a rival, when both could be true. They read silence in the record as proof that something didn't happen. This skill catches those moves and tells you what evidence would fix them.

## What it does

It reads your text and produces:

1. **A claim map**: each causal, existence or influence claim, quoted with its location, with the confidence the text asserts and the links in its causal chain.
2. **A rival table**: the alternative explanations, from your text and from the field (labelled), and how each relates to your claim: excludes it, coexists with it, or supports it.
3. **An evidence ledger**: every piece of evidence, with its source and possible bias, whether it must be there, what else could explain it, its test type, the general rule the test relies on, and the result.
4. **Absences**: evidence your claim predicts but you don't report, with the questions that decide whether that silence counts.
5. **A balance** for each claim: what your wording asserts against what your tests support.
6. **Flags**, each with its location in the text:

| Flag | What it catches |
|---|---|
| E1 Overclaim | The wording is stronger than the tests allow |
| E2 Hoop as proof | Evidence that only keeps a claim alive is treated as confirming it |
| E3 Shared prediction | "Consistent with" evidence that the rivals predict just as well |
| E4 Assumed exclusivity | Support for your claim counted against a rival that could also be true |
| E5 Missing rival | An explanation the field would expect goes unaddressed |
| E6 Unequal toughness | Rivals held to a higher standard than your own explanation |
| E7 Absence misread | Silence read as proof, or a real absence explained away |
| E8 Weak generalisation | The rule that makes the test strong is unstated or only probable |
| E9 Untested link | A step in the causal chain carries no evidence of its own |
| E10 Dependent evidence | One finding counted twice, or many findings that all bear on one rival |
| E11 Source bias | A source's motives or selection go unweighed |
| E12 Tautological prediction | The "prediction" just restates the claim |
| E13 Ad hoc repair | The explanation is bent to fit each anomaly, with no new test |
| E14 Ambiguous test type | Two readings of the evidence, with both given |

7. **Moves**: what evidence would turn a weak test into a strong one, which rival to test next, and how to word each claim at the strength its evidence supports.

It **doesn't rewrite your text**, score your argument, or invent probabilities.

## How to use it

Give Claude your text (or a section of it) and say what you want. Three modes:

- **Audit**: your own draft. *"Run evidence tests on the main claim of this chapter."*
- **Read**: someone else's text. *"Evidence-test this article: how strong is its case, and against which rivals?"*
- **Plan**: research you haven't done yet. *"I want to argue that A's reading of B shaped his later work. What evidence would settle it?"*

If you don't name the claims, it picks the ones your argument rests on and tells you which. It works in any language. It is not meant for interpretive claims about meaning ("the poem is ironic"), and says so if you give it one.

**Tip:** name the rival explanations you're worried about. Uniqueness is always measured against a rival, so the findings get sharper when the rivals are explicit.

## Install

**Claude (web and desktop):**
1. Download [`evidence-tests.zip`](https://github.com/Halfofthesky/evidence-tests/releases/latest/download/evidence-tests.zip).
2. Go to **Customize → Skills → + → Create skill → Upload a skill**.
3. Choose the zip. Code execution must be on in **Settings → Capabilities**.

**Claude Code:** copy the `evidence-tests/` folder into `~/.claude/skills/`.

**ChatGPT, Gemini or any other model:** the skill is a single plain Markdown file with no scripts. Download [`SKILL.md`](https://github.com/Halfofthesky/evidence-tests/releases/latest/download/SKILL.md) and paste it into a custom GPT's instructions, a Gem, a project's instructions, or the start of a chat.

## Downloads

From the [latest release](https://github.com/Halfofthesky/evidence-tests/releases/latest):

| File | For |
|---|---|
| [`evidence-tests.zip`](https://github.com/Halfofthesky/evidence-tests/releases/latest/download/evidence-tests.zip) | Uploading to Claude |
| [`evidence-tests.skill`](https://github.com/Halfofthesky/evidence-tests/releases/latest/download/evidence-tests.skill) | The same archive, `.skill` extension |
| [`SKILL.md`](https://github.com/Halfofthesky/evidence-tests/releases/latest/download/SKILL.md) | Any other model, as plain text |

## Sources

- Stephen Van Evera, *Guide to Methods for Students of Political Science* (Cornell University Press, 1997), 30–35.
- David Collier, "Understanding Process Tracing," *PS: Political Science & Politics* 44.4 (2011): 823–830.
- James Mahoney, "The Logic of Process Tracing Tests in the Social Sciences," *Sociological Methods & Research* 41.4 (2012): 570–597.
- Sherry Zaks, "Relationships Among Rivals (RAR): A Framework for Analyzing Contending Hypotheses in Process Tracing," *Political Analysis* 25.3 (2017): 344–362.
- Andrew Bennett and Jeffrey T. Checkel, eds., *Process Tracing: From Metaphor to Analytic Tool* (Cambridge University Press, 2015).

The skill marks which source each rule comes from. Applying the tests to causal claims left implicit in historical narrative is my own extension. The skill is not affiliated with the authors.

## See also

- [BEAM](https://github.com/Halfofthesky/beam): maps what each source does in your text.
- [Concept Check](https://github.com/Halfofthesky/concept-check): tests whether a concept earns its place.
- [Stasis](https://github.com/Halfofthesky/stasis): finds where a disagreement sits and whether the text meets it there.
- [Logic & Reasoning Skills](https://github.com/Halfofthesky/logic-reasoning-skills): reconstructs arguments, spots fallacies, solves formal logic.
- [Adversarial Editorial Review](https://github.com/Halfofthesky/adversarial-editorial-review): three reviewers and an editorial synthesis for humanities manuscripts.

## License

MIT
