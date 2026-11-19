# Humanize

Humanize is an English and Russian editing skill for drafts that sound formulaic. It helps revise emails, posts, documents and replies while preserving facts, quotations, uncertainty and the writer's voice. You can supply your own style guide or a writing sample.

## Install

### Claude Code

```sh
git clone https://github.com/Da6ka/humanize.git ~/.claude/skills/humanize
```

In Claude Code, type `/humanize` and provide a draft. [Claude Code skills documentation](https://code.claude.com/docs/en/skills#choose-where-skills-load)

### Codex

```sh
git clone https://github.com/Da6ka/humanize.git ~/.agents/skills/humanize
```

In Codex, mention `$humanize` and provide a draft. [Codex skills documentation](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## What it checks

The [pattern catalog](patterns.md) covers 46 patterns, including generic openers, formulaic contrast, repeated context and Russian bureaucratic phrasing. The [regression examples](regression-tests.md) include cases where the right edit is to keep a genuine caveat, a real alternative or an attributed objection.

## Credits

The catalog adapts Siqi Chen's Humanizer under its MIT license. The upstream skill draws on Wikipedia's *Signs of AI writing*. [Original Humanizer](https://github.com/blader/humanizer) · [Upstream license](LICENSE-humanizer) · [Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
