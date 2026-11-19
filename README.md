# Humanize

Humanize помогает сделать письмо, пост или сообщение проще и естественнее на русском и английском. Скилл даёт Codex или Claude правила редактуры, чтобы из текста уходили канцелярит и шаблонные фразы, а факты, цитаты и оговорки сохранялись.

## Установка без терминала

Скачайте архив, распакуйте его и переименуйте папку `humanize-main` в `humanize`. Файлы `SKILL.md` и `patterns.md` должны лежать прямо в этой папке. [Скачать ZIP](https://github.com/Da6ka/humanize/archive/refs/heads/main.zip)

### Codex на компьютере или Claude Code

1. Откройте домашнюю папку. На macOS в Finder нажмите `Cmd+Shift+G`, введите `~` и нажмите Enter. Чтобы показать скрытые папки, нажмите `Cmd+Shift+.`. На Windows введите `%USERPROFILE%` в адресной строке Проводника и нажмите Enter.
2. Для Codex откройте `.agents`, для Claude Code откройте `.claude`. Внутри откройте `skills`. Создайте недостающие папки и перенесите всю папку `humanize` в `skills`.
3. В новом чате Codex наберите `$humanize` и выберите скилл из подсказок. В Claude Code введите `/humanize`. Если скилл не появился, перезапустите приложение и проверьте, что `SKILL.md` лежит в `.agents/skills/humanize` для Codex или в `.claude/skills/humanize` для Claude Code. [Документация Codex](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills) · [Документация Claude Code](https://code.claude.com/docs/en/skills#choose-where-skills-load)

### Claude в браузере

1. Нажмите правой кнопкой мыши на переименованную папку `humanize` и создайте ZIP-архив. Внутри нового архива должна быть папка `humanize` с файлами скилла.
2. На Claude.ai откройте **Settings > Capabilities** и включите **Code execution and file creation**. В новом интерфейсе эта настройка может называться **Create and edit files**.
3. Откройте **Customize > Skills**, нажмите **+**, выберите **Create skill > Upload a skill** и загрузите новый ZIP. Убедитесь, что `humanize` включён. Если загрузка недоступна в рабочем аккаунте, проверьте, разрешено ли добавлять свои скиллы. [Инструкция Claude по загрузке скиллов](https://support.claude.com/en/articles/12512180-use-skills-in-claude)

## Как работает Humanize: до и после

Ниже два примера из работы со скиллом в Codex. Имена, компании, ссылки и детали ситуаций убраны или заменены.

Чтобы попробовать, скопируйте любой блок «Запрос». В Codex добавьте его к `$humanize`, в Claude Code поставьте перед ним `/humanize`. В чате на Claude.ai сначала напишите «Используй скилл humanize», затем вставьте запрос в то же сообщение.

### На русском: сократить обратную связь после интервью

**Запрос с исходным черновиком**

```text
Сократи сообщение для мессенджера. Сохрани детали про малые выборки и результат теста для новых пользователей.

Спасибо за время и разговор. К сожалению, не готовы продолжить процесс. Для этой роли важно самостоятельно принимать обоснованные решения по экспериментам. На интервью мне не хватило конкретики по двум вопросам:

- Как ты определяешь нужную выборку и длительность теста и принимаешь решение, если трафика мало.
- В одном из кейсов общий результат теста был неопределённым, а улучшение наблюдалось у новых пользователей. Осталось неясно, как ты проверял надёжность результата в этой группе.

Удачи тебе в поиске!
```

**После редактуры**

> Спасибо за разговор. К сожалению, не готовы продолжить. На интервью мне не хватило конкретики: как ты принимаешь решения при малых выборках и как проверял результат для новых пользователей, когда общий результат теста был неопределённым. Для этой роли важно обосновывать такие решения. Удачи тебе в поиске!

Два длинных пункта уместились в одну фразу. В сообщении по-прежнему понятно, каких примеров не хватило на интервью.

### In English: draft an interview invitation

**Запрос по рабочим заметкам**

```text
Write a short interview invitation. Thank the person for applying for the analyst role. Ask about the A/B test they worked on, especially the test design and their part in the analysis. Suggest a short call.
```

**Готовый черновик**

> Thanks for applying for the analyst role. I'd like to hear more about the test design and your own role in the analysis. Would a short call work?

Кандидат заранее знает, какой пример подготовить к звонку.

Потом подставьте свой черновик. Если важен тон, добавьте пожелание («сохрани обращение на вы») или приложите короткий образец своего текста. Перед отправкой перечитайте результат и сверьте факты с черновиком.

## Установка через Git

Если вы уже пользуетесь Git, можете выполнить одну из команд в терминале macOS или Linux.

**Codex**

```sh
git clone https://github.com/Da6ka/humanize.git ~/.agents/skills/humanize
```

Откройте чат Codex и вызовите `$humanize`.

**Claude Code**

```sh
git clone https://github.com/Da6ka/humanize.git ~/.claude/skills/humanize
```

В Claude Code введите `/humanize` и добавьте черновик.

## Как устроен скилл

Правила редактуры и примеры «до и после» собраны в [каталоге приёмов](patterns.md). В [проверочных примерах](regression-tests.md) показано, какие оговорки, альтернативы и возражения важно сохранить.

Каталог основан на Humanizer от Siqi Chen, который использует материал Wikipedia *Signs of AI writing*. [Оригинальный Humanizer](https://github.com/blader/humanizer) · [Лицензия MIT исходного проекта](LICENSE-humanizer) · [Статья Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
