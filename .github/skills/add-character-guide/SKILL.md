---
name: add-character-guide
description: Adds the folder and markdown files for a fighting game character's entry
disable-model-invocation: true
---

When this skill is invoked, the user will provide a game name and character name as parameters. If no character name is provided, stop and ask the user to supply a character name before proceeding.

1. Check if the provided game exists as a subfolder in `content/docs`. If the game does not exist, inform the user and stop execution.
2. For the provided game, check if a subfolder for the provided character exists in `content/docs/<game>/characters`. If it does, stop and notify the user instead of overwriting it.
3. If no subfolder exists, add a new subfolder to `content/docs/<game>/characters` called `<character-name>`.
4. In that character's folder, add 5 markdown files:
  - `_index.md`
  - `about.md`
  - `combos.md`
  - `educational-content.md`
  - `oki.md`
5. Add the following frontmatter to the newly created `_index.md`:
```
---
title: "<character-name>"
description: ""
icon: "article"
toc: true
---
```
6. Add the following frontmatter to the newly created `about.md`:
```
---
title: "About <character-name>"
description: ""
icon: "article"
toc: true
---
```
7. Add the following frontmatter to the newly created `combos.md`:
```
---
title: "Combos"
description: ""
icon: "article"
toc: true
---
```
8. Add the following frontmatter to the newly created `educational-content.md`:
```
---
title: "Educational Content"
description: ""
icon: "article"
toc: true
---
```
9. Add the following frontmatter to the newly created `oki.md`:
```
---
title: "Oki"
description: ""
icon: "article"
toc: true
---
```

## Guidelines for handling character names

Some characters will have names with special characters, such as `E. Honda` and `A.K.I`. When creating a markdown file for that character, remove all punctuation, special characters, and spaces from the filename. For example, `E. Honda` would be `ehonda.md`, `A.K.I.` would be `aki.md`, `Ryu` would be `ryu.md`, and both `Chun Li` and `Chun-Li` would be `chun-li.md`.

Regardless if a character's name contains special characters, preserve the character name as it was provided for the `title` field in their markdown file's frontmatter. That value is what end users will see in the documentation.