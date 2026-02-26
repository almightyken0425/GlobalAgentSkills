# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 專案概述

此 repo 用於存放自訂的 Claude Code Agent Skills，供其他專案透過各自的 `.agent/skills/` 目錄引用。每個 skill 是一個獨立資料夾，內含描述 skill 行為規範的主文件。

---

## 目前 Skills

- **tutorial_writing** — 技術知識文件的撰寫哲學與認知架構建構方法論，規範如何從底層協議到應用層逐步堆疊知識
- **universal_writing_linter** — Markdown 與程式碼註解的通用寫作規範，包含禁令清單、命名規範、格式標準，並要求執行驗證腳本

---

## Skill 結構規範

每個 skill 資料夾的標準結構：

```
.agent/skills/<skill-name>/
  SKILL.md          # skill 的主要規範文件，開頭須有 YAML front matter
  scripts/          # 若 skill 需要自動化驗證，腳本放此
  *.md              # 其他政策文件，由主文件引用
```

YAML front matter 必填欄位為 `name` 與 `description`。

---

## 新增 Skill 的方式

在 `.agent/skills/` 下建立新資料夾，至少包含一個主規範文件，front matter 格式如下：

```yaml
---
name: skill-name
description: 一句話描述此 skill 的用途
---
```
