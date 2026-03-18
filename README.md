# LIL SSO Builder

A lightweight browser tool for generating authenticated **LinkedIn Learning SSO links**.

No installation. No login. No data collection.

You can use it **directly in your browser** via GitHub Pages or **download it and run it locally, both behave exactly the same.

**Live tool:**
https://thejobot.github.io/LIL-SSO-Builder

---

## What This Tool Does

LinkedIn Learning often provides generic share links that route learners to a standard email login screen.

**LIL SSO Builder** generates a properly structured Single Sign-On (SSO) URL so learners are routed through their organization’s SSO login and land directly on the intended LinkedIn Learning content.

Paste two URLs. Get one clean, authenticated SSO link.

---

## What You Need

### 1. Your SSO URL

This is the JIT or share SSO URL associated with your LinkedIn Learning account. It contains your account ID and looks similar to:

```
https://www.linkedin.com/learning-login/jit?account=XXXXXXXXX&channelType=JIT_INVITATION...
```

If you do not have this URL, your LinkedIn Learning administrator or Customer Success Manager can provide it.

Short or redirected URLs are supported — the tool will guide you through expanding them.

---

### 2. A LinkedIn Learning Content URL

The tool supports all major LinkedIn Learning content types, including learner-created content.

Supported types:

- Courses
- Topic browse pages (e.g. `browse/technology`)
- Showcase pages (e.g. `showcase/artificial-intelligence`)
- Learning paths
- Individual videos
- Role play scenarios
- User-generated collections (shared collections)

---

## How to Use

### Step 1 — Paste your SSO URL

Paste your **full JIT or share SSO URL** into Step 1 and select **Extract Account ID**.

If the tool detects a **short or redirected URL**, it will:
- Display clear expansion instructions
- Provide an **Open in New Tab to Expand** button

Once redirected, copy the full URL from your browser’s address bar and paste it back into the tool.

---

### Step 2 — Paste a content URL

Paste any LinkedIn Learning content URL into Step 2.

The tool automatically detects the content type and preserves the correct path, including:
- Role play scenario URNs
- Numeric collection IDs for shared collections

---

### Step 3 — Build and copy

Select **Build SSO URL**.

Your authenticated SSO link appears immediately. Select **Copy to Clipboard** and share it.

---

## Supported URL Examples

| Content Type | Example |
|---|---|
| Course | `linkedin.com/learning/course-name` |
| Topic Browse | `linkedin.com/learning/browse/technology` |
| Showcase | `linkedin.com/learning/showcase/artificial-intelligence` |
| Learning Path | `linkedin.com/learning/paths/path-name` |
| Video | `linkedin.com/learning/videos/video-name` |
| Role Play | `linkedin.com/learning/role-play/scenarios/...` |
| Collection | `linkedin.com/learning/collections/1234567890` |

---

## How It Works

The tool extracts your account ID from the SSO URL and wraps the content URL using LinkedIn Learning’s enterprise login pattern:

```
https://www.linkedin.com/checkpoint/enterprise/login/[ACCOUNT_ID]
?pathWildcard=[ACCOUNT_ID]
&application=learning
&redirect=[ENCODED_CONTENT_URL]
```

This triggers your organization’s SSO configuration and routes learners through the branded login experience before landing on the selected content.

---

## Privacy

Using this tool on **GitHub Pages is no different than downloading and running it locally**.

The HTML file is loaded once by your browser. After that, **all processing happens entirely in your browser**.

- URLs you paste are never transmitted
- No data is logged or stored
- No analytics or tracking
- No network requests after page load

GitHub cannot see what you paste or what the tool generates.

---

## Running Locally

If you prefer to run it on your own machine:

1. Select **Code → Download ZIP**
2. Unzip the folder
3. Open `index.html` in any browser

No setup required.

---

## Requirements

Any modern browser (Chrome, Safari, Firefox, Edge). Works on macOS, Windows, and mobile.

---

## Questions or Issues

Open an issue in this repository and include:
- The type of URL you used
- The output you received

---

**LIL SSO Builder** is a community utility and is not an official LinkedIn product.
