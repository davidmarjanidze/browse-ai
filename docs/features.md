# Features

All features come from the `browse-ai-core` package. This page lists what a
BrowseAI user gets with the extension's config. The package docs describe each
feature and option in full.

## Extension config

`src/content/extension-config.ts`:

| Option       | Value                 | Effect                                                                |
| ------------ | --------------------- | --------------------------------------------------------------------- |
| `mode`       | `drawer`              | Round button in a corner; the chat opens as a full-height side panel. |
| `position`   | `bottom-right`        | Corner of the button and side of the panel.                           |
| `palette`    | `forest`              | Default colors. Users can pick another in settings.                   |
| `theme`      | `system`              | Follows the OS light or dark mode by default.                         |
| `storageKey` | `_browseAIV2`         | Key in `chrome.storage.local`.                                        |
| `features`   | `{ bookmarks: true }` | Turns on AI bookmarks. All other features keep the package defaults.  |

## What the user gets

**Chat**

- Chat with Gemini Nano on the device. Answers stream in as they're written and
  are shown as Markdown. Each answer can be copied. A running answer can be
  stopped.
- A download button and progress when the model isn't on the device yet.
- **Page / General** switch. In page mode the prompt includes the page title,
  URL and main text. If the page is too long for the model, the text is cut and
  the chat says how much was cut. In general mode no page context is sent. In
  page mode the switch shows the site's host name.
- Text selected on the page is shown above the input and sent with the next
  prompt.
- A chat memory badge in the header shows how much of the model's context is
  used. **New chat** starts over.
- A moving glow behind the header and messages while the model is thinking.

**Attachments**

- Upload an image or an audio file and ask about it.
- **Capture visible area**: screenshot of the visible part of the tab.
- **Snip and capture**: drag a rectangle on the page; only that part is
  attached.

**Tools** (picked from the Tools select under the input)

- **Form filler**: reads the labelled fields of the form on the page and
  suggests values from the user's message. Each suggestion appears next to its
  field with Accept and Dismiss, plus Accept all and Dismiss all in the chat.
- **Tables extractor**: finds the HTML tables on the page and offers them for
  download as CSV, Excel, JSON or Markdown, in one zip.

**AI bookmarks** (on in the extension)

- While on, every page the user opens is put into a category picked by the model
  and saved in `chrome.storage.local`.
- The **AI Bookmarks** panel (header menu) lists the categories. Users can open
  pages, delete a page, delete a category or clear everything.
- The model also merges similar categories as the list grows.

**Settings** (header menu)

- Theme: light, dark or system. Palette: one of 10.
- Personalization: a nickname and custom instructions that are added to every
  conversation.
- A switch to turn AI bookmarks on or off.

## Not turned on in the extension

- **DOM element to component**: pick an element on the page and get component
  code for Angular, React, Vue or plain JavaScript. It's off by default in the
  package and the extension doesn't turn it on. Set
  `features.domToComponent: true` in the extension config to add it to the Tools
  select.

## Toolbar popup

Clicking the toolbar icon opens `popup.html`, a static page that tells the user
to click the round button in the bottom right corner of any page.
