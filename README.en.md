<!-- 语言切换 / Language -->
[简体中文](README.md) | **English**

<div align="center">

# Multi_AI_Conversation · 多AI对话

A DeepSeek Harness (DSH) desktop plugin that lets multiple large-language-model
AIs take turns talking on one page — collaborating, discussing, and iterating on
your project autonomously.

</div>

---

## 👤 Author

- Author: **恕染** (English name: **shuran**)
- GitHub: [@shuran10086](https://github.com/shuran10086)
- Repository: <https://github.com/shuran10086/Multi_AI_Conversation>

---

## ✨ Features

**Multi_AI_Conversation** adds a top-level entry "多AI对话 / Multi-AI Chat" to the
DeepSeek Harness left navigation bar; clicking it opens the plugin's own page.
Core capabilities:

- **Multi-model management**: configure **up to 6** AI models in the plugin page,
  each with its own **API base URL, key, model name, persona/role, and
  temperature**. Independent of DSH's built-in model settings.
- **Two modes**: a **Work Mode** and a **Game Mode**, each configured and saved
  independently.
- **Work Mode (core)**:
  - After you send a **project goal**, multiple AIs **take turns discussing**
    autonomously — brainstorming and iterating on the plan;
  - AIs speak in **strict turns** (the next starts only after the current one
    finishes), and every AI can see what the others said;
  - **Timeout auto-skip**: an AI that does not answer in time is skipped to the
    next one; after several consecutive skips it is dropped for the rest of the
    round;
  - **Interjection anytime**: either "send after the current AI finishes" or
    "pause everything immediately and send";
  - **Auto / manual turn order**: let the system rotate automatically, or pick
    the next speaker yourself;
  - After you issue the **"Start" (开工)** command, the AIs move from discussion
    to **step-by-step delivery**, continuously **compiling the result into a
    single Markdown "final plan" file**;
  - **Multiple discussion histories** can be reviewed and resumed.
- **Game Mode (planned)**: let AIs autonomously play Werewolf, with customizable
  items/effects and customizable role (werewolf/villager/…) counts and
  abilities. *(For now only the foundation and placeholder UI are reserved; game
  logic is not yet implemented.)*
- **Native experience**: fully uses DSH theme tokens, localization, and layout
  conventions; **compatible with dark/light themes and window scaling**; the UI
  is **bilingual (Chinese/English)** and follows the DSH language setting.

---

## 🚀 Usage

> ⚠️ This project is developed **in stages** and is currently being built
> incrementally. The following is the standard workflow once the plugin is
> complete.

### 1. Get the project

```bash
git clone https://github.com/shuran10086/Multi_AI_Conversation.git
```

The plugin source lives in `插件本体/Multi_AI_Conversation/` (an installable DSH
bundle).

### 2. Install into DeepSeek Harness

This plugin is a standard DSH bundle (with `package.json` and
`cordis.patch.yml`). Install it through DSH's plugin management using the
**absolute path** of `插件本体/Multi_AI_Conversation/` as the target. After a
successful install, a "多AI对话" entry appears in the left navigation bar.

### 3. Configure AI models

1. Click "多AI对话" on the left to open the plugin page;
2. In the configuration area, **add AIs** (up to 6). For each AI fill in: a
   nickname, API base URL (OpenAI-compatible), key, and model name; optionally a
   persona, temperature, and color;
3. In "Output Settings", pick the **output folder** for the final plan file.

### 4. Use Work Mode

1. Switch to "Work Mode" and start a new discussion;
2. Enter your **project goal** and send it;
3. The AIs begin **taking turns discussing**. You can interject at any time and
   tune the rules (timeout, turn order, interjection mode, etc.);
4. When the discussion is mature, click **"Start" (开工)**. The AIs move to
   step-by-step delivery and continuously write the plan into a Markdown file in
   your chosen folder;
5. Every discussion is saved to the history list and can be reviewed or resumed.

---

## 📄 License

This project uses the **Multi_AI_Conversation Non-Commercial Open Source
License**. See [LICENSE](LICENSE).

- ✅ Anyone may copy, use, modify, and redistribute it;
- 📌 Redistribution / derivatives must: publish the complete source code, retain
  the original author, project URL and original license, state the changes and
  their dates, and keep using this same license;
- 🚫 **All commercial use is prohibited** (selling, paid SaaS/hosting/API,
  advertising/marketing, enterprise for-profit use, etc.);
- ✍️ Commercial use requires prior written authorization from the copyright
  holder **恕染 (shuran)**.
