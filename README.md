# Humanize

Humanize is a Claude skill for editing emails, posts, and messages in English and Russian. It cuts jargon and stock phrases while preserving facts, quotations, and caveats. It also works with Codex.

## Install in Claude on the web

1. Download and unzip the archive. Rename the extracted folder from `humanize-main` to `humanize`. It contains `SKILL.md` and `patterns.md`. [Download the ZIP](https://github.com/Da6ka/humanize/archive/refs/heads/main.zip)
2. Right-click the `humanize` folder and compress it into a new ZIP. Open the new ZIP to check that it contains the `humanize` folder with the skill files inside.
3. On Claude.ai, open **Settings > Capabilities** and turn on **Code execution and file creation**. This setting may be called **Create and edit files**.
4. Open **Customize > Skills**, click **+**, and choose **Create skill > Upload a skill**. Upload the new ZIP and make sure `humanize` is enabled. If you use a work account and the upload option is missing, ask your administrator whether custom skills are allowed. [Claude's guide to uploading skills](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

## Use Humanize in Claude

Start a new chat and type `Use the humanize skill.` In the same message, paste a draft and say what you want changed. You can try it with either prompt below.

## Examples from real use

Both examples are adapted from real uses of the skill. Identifying details have been removed or changed.

### Shorten interview feedback in Russian

**Prompt with the original draft**

```text
Сократи сообщение для мессенджера. Сохрани детали про малые выборки и результат теста для новых пользователей.

Спасибо за время и разговор. К сожалению, не готовы продолжить процесс. Для этой роли важно самостоятельно принимать обоснованные решения по экспериментам. На интервью мне не хватило конкретики по двум вопросам:

- Как ты определяешь нужную выборку и длительность теста и принимаешь решение, если трафика мало.
- В одном из кейсов общий результат теста был неопределённым, а улучшение наблюдалось у новых пользователей. Осталось неясно, как ты проверял надёжность результата в этой группе.

Удачи тебе в поиске!
```

**Edited message**

> Спасибо за разговор. К сожалению, не готовы продолжить. На интервью мне не хватило конкретики: как ты принимаешь решения при малых выборках и как проверял результат для новых пользователей, когда общий результат теста был неопределённым. Для этой роли важно обосновывать такие решения. Удачи тебе в поиске!

The rewrite turns two long bullets into one sentence while keeping both questions about decisions with small samples and the test result for new users.

### Draft an interview invitation in English

**Prompt based on notes**

```text
Write a short interview invitation. Thank the person for applying for the analyst role. Ask about the A/B test they worked on, especially the test design and their part in the analysis. Suggest a short call.
```

**Draft invitation**

> Thanks for applying for the analyst role. I'd like to hear more about the test design and your own role in the analysis. Would a short call work?

The candidate knows which example to prepare for the call.

For your own draft, specify the tone you want, such as `Keep the tone formal`, or include a short sample of your writing. Check the facts against your original draft before sending the result.

## Install in Claude Code

Move the extracted `humanize` folder into `.claude/skills` in your home folder. Create `.claude` and `skills` if needed. The full path to the skill file should be `~/.claude/skills/humanize/SKILL.md`. In Claude Code, type `/humanize` and add a draft or one of the prompts above. [Claude Code skills documentation](https://code.claude.com/docs/en/skills#choose-where-skills-load)

If you use Git, you can install the skill from a macOS or Linux terminal with this command.

```sh
git clone https://github.com/Da6ka/humanize.git ~/.claude/skills/humanize
```

## Editing rules and credits

The pattern catalog contains the editing rules and before-and-after examples. The test cases show how the skill handles caveats, alternatives, and objections that matter to the meaning of the draft. [Pattern catalog](patterns.md) · [Test cases](regression-tests.md)

The catalog adapts Siqi Chen's Humanizer, which draws on Wikipedia's *Signs of AI writing*. [Original Humanizer](https://github.com/blader/humanizer) · [Upstream MIT license](LICENSE-humanizer) · [Wikipedia article](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
