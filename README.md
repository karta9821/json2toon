# JSON to TOON Converter

<div align="center">

[![Next.js](https://img.shields.io/badge/Next.js-16-black?style=flat-square&logo=next.js)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=flat-square&logo=typescript)](https://www.typescriptlang.org/)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)

**A privacy-first converter for transforming data between JSON, TOON, TONL, CSV, YAML, TOML, XML and Protobuf, with a free API and MCP server.**

> [!IMPORTANT]
> **This repository serves as the official bug tracker for the [JSON to TOON Service](https://json2toon.co).**
> Please report any issues you encounter with the service here.

[Go to Service](https://json2toon.co) • [Documentation](https://json2toon.co/docs) • [MCP Server](https://json2toon.co/mcp) • [Report Bug](https://github.com/karta9821/jsontotoon/issues/new?template=bug_report.md) • [Changelog](https://json2toon.co/changelog)

</div>

---

## 🎯 What is This?

**JSON to TOON** is a comprehensive data transformation toolkit designed for the AI era. While it handles all standard formats (JSON, YAML, CSV, etc.), its crown jewel is the **TOON (Token-Oriented Object Notation)** format—specifically engineered to optimize data for Large Language Models (LLMs).

### Why TOON?

In the world of LLMs, context window space is precious and expensive. Standard JSON is verbose and token-heavy. TOON solves this by:

- ✅ **Reducing Token Usage**: about **43% fewer tokens** than JSON on average (42.6% in the [official TOON benchmark](https://toonformat.dev/guide/benchmarks)), from ~33% on mixed/nested data to ~59% on flat tables.
- ✅ **Enhancing Readability**: Cleaner syntax that is easier for both humans and models to parse.
- ✅ **Preserving Structure**: Maintains full data fidelity and typing.
- ✅ **Cost Efficiency**: Lower token counts mean cheaper API calls (OpenAI, Anthropic, etc.).

---

## ✨ Features

### 🔄 Universal Conversion & Batch Processing
- **8 Supported Formats**: JSON, TOON, TONL, YAML, TOML, CSV, XML, Protobuf.
- **Bidirectional**: Convert from any format to any format instantly.
- **Batch Mode**: Drag & drop multiple files to convert them all at once.
- **Auto-Detection**: Smart format detection for pasted content.

### 🛠️ Advanced Developer Tools
- **Diff Viewer**: Visual side-by-side comparison of input vs. output.
- **Schema Generator**: Instantly generate JSON Schemas from your data samples.
- **Performance Benchmark**: Run built-in benchmarks to see parsing speed and token savings for your specific data.
- **Format Settings**: Customize indentation (2/4 spaces, tabs) and delimiters.

### 🎨 Premium Editor Experience
- **Monaco Editor**: Full-featured code editor (VS Code engine).
- **Themes**: Choose from System, VS Light/Dark, Dracula, Monokai, and GitHub themes.
- **Font Scaling**: Adjustable font size (10px - 24px) for accessibility.
- **Live Validations**: Syntax error highlighting and line counts.

### 🔒 Privacy-First Architecture
- **Client-Side Processing**: All conversions happen 100% in your browser.
- **Zero Data Leaks**: Your sensitive data never hits our servers (except for the API, see below).
- **Privacy Mode**: Toggle to disable local history storage and analytics events.

### 📊 Analytics & Insights
- **Token Tracker**: Real-time display of input vs. output token counts and savings.
- **Conversion History**: (Optional) Keep track of your recent conversions locally.
- **Shareable Links**: Generate URL-encoded links to share specific data states with colleagues.

### 🌐 Browser Extension
Take the power of JSON to TOON anywhere on the web:
- **Context Menu**: Right-click selected text to convert instantly.
- **Popup Interface**: Quick access to the converter without leaving your tab.
- **Supports**: Chrome, Firefox, Edge, Safari.

---

## 🔌 API Documentation

For developers needing programmatic access, we provide a robust API.

### `POST /api/v1/toon`

Convert content to TOON format.

Free, no API key.

#### Request Body
```json
{
  "content": "{'key': 'value'}",
  "format": "json", 
  "options": {
    "indent": 2
  }
}
```

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| `content` | string | Yes | The raw content string to convert. |
| `format` | string | No | Input format (`json`, `yaml`, `toml`, `xml`). Auto-detected if omitted. |
| `options` | object | No | Configuration options for the converter. |

#### Response
Returns the converted TOON string.
```text
key: value
```

---

## 🤖 MCP Server

json2toon is a remote MCP server (Streamable HTTP, no auth), listed in the [official MCP Registry](https://registry.modelcontextprotocol.io/) as `io.github.karta9821/json2toon`.

- **URL**: `https://json2toon.co/api/mcp`
- **Tools**: `json_to_toon` (JSON → TOON, optional `delimiter`: comma, tab or pipe) and `toon_to_json` (TOON → pretty-printed JSON)
- **Setup guides** for Claude, ChatGPT and Cursor: [json2toon.co/mcp](https://json2toon.co/mcp)

```json
{
  "mcpServers": {
    "json2toon": { "url": "https://json2toon.co/api/mcp" }
  }
}
```

---

## 🚀 Quick Start

### Online (Recommended)
Visit [json2toon.co](https://json2toon.co) — No login required.

---

## 🛠️ Tech Stack

- **Framework**: [Next.js 16](https://nextjs.org/) (React 19)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **UI**: [Tailwind CSS](https://tailwindcss.com/) + [Shadcn UI](https://ui.shadcn.com/)
- **Editor**: [Monaco Editor](https://microsoft.github.io/monaco-editor/)
- **Conversion Engines**:
  - TOON: [@toon-format/toon](https://www.npmjs.com/package/@toon-format/toon)
  - YAML: `js-yaml`
  - TOML: `smol-toml`
  - CSV: `papaparse`
  - XML: `fast-xml-parser`


## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

