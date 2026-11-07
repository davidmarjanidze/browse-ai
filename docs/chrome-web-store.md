# Chrome Web Store

Text to paste into the Chrome Web Store developer dashboard. Keep it in line
with [privacy-policy.md](privacy-policy.md) and `public/manifest.json`.

## Listing

**Name:** BrowseAI

**Short description:** Your AI Assistant for Every Page

**Full description:**

```text
Chat with any web page using Chrome's built-in Gemini Nano. Everything runs on your device. No cloud, no tracking, and it works offline.

BrowseAI - AI Help on Any Page

BrowseAI puts Google's Gemini Nano model right in your browser. Ask questions about the page you're on, or just chat without any page context. The model runs on your computer, so it works offline and nothing gets sent anywhere. Your chats, browsing data, and prompts stay on your machine. You can summarize a page, ask follow-up questions, or switch to general chat mode at any time.

⚠️ SYSTEM REQUIREMENTS

You need Google Chrome 151 or newer with built-in AI turned on. The first time you open BrowseAI, click "Download Model" to get Gemini Nano (about 2-4 GB). Make sure you have enough free disk space.

■ FEATURES (TOOLS)

→ Form Filler - Paste in plain text, like your resume, and BrowseAI suggests what to put in each form field on the page.

How to use Form Filler:

1. Open the "Tools" menu and pick "Form Filler".
2. Paste your text, press Enter, and wait while it fills in the form.
3. Check each suggestion and accept or dismiss it, or use "Accept All" or "Dismiss All".

→ Tables Extractor - Finds all the tables on the current page and gets them ready to download.

How to use Tables Extractor:

1. Open the "Tools" menu and pick "Tables Extractor".
2. Press Enter. You can add a prompt if you want, but you don't have to.
3. Use the download menu in the chat box to get CSV, Excel, JSON, or Markdown files in one zip.

■ FEATURES (MIX)

→ AI Bookmarks - Sorts the pages you visit into groups on its own. You can browse, open, and delete them right from the chat panel.

How to use AI Bookmarks:

1. Open Settings and leave "AI Bookmarks" turned on.
2. Browse like normal. BrowseAI sorts pages into groups and saves them on your device.
3. Open the menu at the top of the chat, pick "AI Bookmarks", then open a group to view, open, or delete pages.

→ Multimodal Support (Images & Audio) - Add images or audio files to your question. Ask about diagrams, charts, or pictures, or add a recording to get a transcript or ask about what's said.

→ Capture Visible Area - Take a screenshot of what you can see on the page and add it to your question.

→ Snip & Capture - Drag to select part of the page and add just that part to your question.

→ Selection Highlighting - The text you selected shows up in the chat, so you know what BrowseAI is looking at.

→ Context Mode Toggle - Switch between page mode (BrowseAI reads the whole page) and general mode (plain chat, no page) with one click.

→ Real-time Streaming (Live Responses) - Answers show up word by word as they're written, so you can start reading right away.

→ Context Window Usage - Shows how much of Gemini Nano's memory for the current chat is used up.

→ Themes and Personalization - Pick light, dark or system mode and one of 10 color palettes. Add a nickname and custom instructions so answers fit how you like to work.

■ HOW TO GET STARTED

Install BrowseAI and click the floating BrowseAI button to open the chat. When asked, click "Download Model" to get Gemini Nano. Once it's ready, you're good to go.

Select some text and ask about it, or just ask for a summary of the page. Use the toggle at the bottom of the chat to switch between page mode and general mode.

■ GOOD FOR

Writers who need to summarize research. Students trying to understand hard topics or docs. Developers reading code and API docs. Researchers pulling info from several pages. Anyone who has to get through long reports.

⚠️ IMPORTANT DISCLAIMER

BrowseAI can make mistakes. Its answers and tool results may be wrong, incomplete, misleading, or out of date. Always check the results before you rely on them, especially for legal, money, medical, security, or other important decisions.

Don't use BrowseAI for anything illegal, harmful, or deceptive, or to misuse other people's content or services. The developer is not responsible for misuse of the extension or for problems caused by mistakes in its answers or tool results.
```

**Category:** Productivity. **Language:** English.

### Text for a later listing update

DOM element to component is built into the package but not turned on in the
extension. When it is, add this to the description:

```text
■ DEVELOPER FEATURES

→ DOM element to Component - Pick any element on the page and get component code for it.

How to use DOM element to Component:

1. Open the "Tools" menu and pick "DOM element to component".
2. Pick the framework: Angular, React, Vue.js, or JavaScript.
3. Hover the page to see the highlight, then click the element you want.
4. Press Enter. Add extra requirements if you have any.
```

## Privacy practices

### Single purpose

```text
BrowseAI is an on-device AI assistant that answers questions about the current web page or selected text using Chrome's built-in language model. All processing happens locally on your device. No data is sent to any server.
```

### Permission justifications

**storage**

```text
BrowseAI uses the storage permission to save user-controlled settings in chrome.storage.local on the device: theme and color palette, an optional nickname used to address the user in answers, and optional custom instructions that guide the style of answers. When the user keeps the optional AI Bookmarks feature on, it also stores a list of visited pages (title and URL) grouped by AI-made categories, so the user can open and manage them from the Bookmarks panel. This data stays on the device and is never sent to a server.
```

**activeTab**

```text
BrowseAI uses activeTab only for screenshots the user asks for. When the user picks Capture Visible Area or Snip & Capture, the extension captures the visible part of the current tab and attaches it to the prompt. It is used only at the time of that action and only for the tab the user is on.
```

**Host permission (`<all_urls>`)**

```text
BrowseAI runs on the websites the user visits so it can show its chat button and, when the user opens the chat, read the page text or selected text for page-aware answers. Access to all sites is needed because users can use BrowseAI on any page. Content is processed on the device by Chrome's built-in Prompt API and is not sent to the developer or any third-party server.
```

### Remote code

Select **No, I am not using remote code.** All code is in the package that is
uploaded; the model is Chrome's built-in one.

### Data usage

Leave every data type unchecked. BrowseAI handles page content, prompts and the
bookmarks list only on the device and doesn't collect or transmit them.

### Certifications

Check all three:

- I do not sell or transfer user data to third parties, apart from the approved
  use cases.
- I do not use or transfer user data for purposes that are unrelated to my
  item's single purpose.
- I do not use or transfer user data to determine creditworthiness or for
  lending purposes.

### Privacy policy URL

```text
https://github.com/davidmarjanidze/browse-ai/blob/main/docs/privacy-policy.md
```

The repo must be public and pushed for this link to work.
