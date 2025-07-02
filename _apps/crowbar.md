---
title: Crowbar
description: Clean interface. Fast search. Smart cleanup. Minimalist Chrome extension for efficient browser navigation and tab management.
icon: /images/crowbar-icon.png
links:
  - text: "GitHub"
    url: "https://github.com/janithkv/crowbar"
    primary: true
  - text: "Install"
    url: "#installation"
tech_stack:
  - "JavaScript"
  - "Chrome Extension API"
  - "HTML/CSS"
  - "Jest"
---

## Overview

Crowbar is a minimalist Chrome extension designed for efficient browser navigation and tab management. Built with a focus on speed and simplicity, it provides two core modes: **Search** and **Cleanup**.

## Features

### 🔍 Search Mode
**Find anything instantly:**
- 📑 Bookmarks • 🕒 History • 📱 Open tabs • 🌐 Search engines

**Usage:**
- **Ctrl+K** (Cmd+K on Mac) to open search
- Type to search → **Space** for search engines → **Tab** to select → **Enter** to open

### 🧹 Cleanup Mode
**Efficient tab management:**
- **Ctrl+L** (Cmd+L on Mac) to open tab manager
- Filter tabs → Select with **Space** or checkboxes → **Enter** to close
- **Shift+Arrows** for range selection • **Ctrl+A/D** (Cmd+A/D on Mac) for select/deselect all

## Installation

```bash
git clone https://github.com/janithkv/crowbar.git
```

**Chrome/Chromium:**
1. Open Chrome → `chrome://extensions/`
2. Enable "Developer mode"
3. Click "Load unpacked" → select Crowbar directory

**Microsoft Edge:**
1. Open Edge → `edge://extensions/`
2. Enable "Developer mode"
3. Click "Load unpacked" → select Crowbar directory

**Note:** Works on Windows, macOS, and Linux

## Design Philosophy

**Minimal UI** • **Keyboard-first** • **Fast search** • **Smart defaults**

The extension follows a clean, distraction-free design that prioritizes functionality over visual complexity. Every interaction is optimized for speed and efficiency.