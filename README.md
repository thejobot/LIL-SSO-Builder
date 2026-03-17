# LIL SSO Builder

A free browser tool that generates authenticated SSO course links for LinkedIn Learning. No installation, no login, no data sent anywhere. Use it live in your browser or download it and run it locally — both work exactly the same way.

Use it now!
https://thejobot.github.io/LIL-SSO-Builder/index.html

---

## What This Tool Does

LinkedIn Learning often generates generic course links that send learners to a standard email login screen. **LIL SSO Builder** creates a properly structured Single Sign‑On (SSO) URL so learners are routed through their organization’s SSO login and land directly on the intended content.

You paste two URLs. The tool generates one clean, authenticated SSO link.

---

## What You Need

### 1. Your SSO URL

This is the JIT or share SSO URL for your LinkedIn Learning account. It contains your account ID and looks similar to:

```
https://www.linkedin.com/learning-login/jit?account=XXXXXXXXX&channelType=JIT_INVITATION...
```

If you don’t have this, your LinkedIn Learning admin or customer success manager can provide it.

### 2. A LinkedIn Learning Content URL

The tool supports:

- Courses
- Topic browse pages (for example: browse/technology)
- Showcase pages (for example: showcase/artificial-intelligence)
- Learning paths
- Individual videos

---

## How to Use

### Step 1 – Paste Your SSO URL

Paste your full JIT or share SSO URL into Step 1 and click **Extract Account ID**.

If the tool detects a short or redirected URL, it will show instructions and an **Open in New Tab** button so you can expand the link in your browser and paste the full URL back in.

### Step 2 – Paste a Content URL

Paste any LinkedIn Learning course, browse, showcase, path, or video URL into Step 2. The content type is detected automatically.

### Step 3 – Build and Copy

Click **Build SSO URL**. Your authenticated link appears instantly. Click **Copy to Clipboard** and share it.

---

## Supported URL Types

| Content Type | Example |
|------------|--------|
| Course | linkedin.com/learning/course-name |
| Topic Browse | linkedin.com/learning/browse/technology |
| Showcase | linkedin.com/learning/showcase/artificial-intelligence |
| Learning Path | linkedin.com/learning/paths/path-name |
| Video | linkedin.com/learning/videos/video-name |

---

## How It Works

The tool extracts your account ID from the SSO URL and wraps the content URL using LinkedIn Learning’s enterprise login pattern:

```
https://www.linkedin.com/checkpoint/enterprise/login/[ACCOUNT_ID]
?pathWildcard=[ACCOUNT_ID]
&application=learning
&redirect=[ENCODED_CONTENT_URL]
```

This triggers your organization’s SSO configuration and routes learners through the branded login before landing them on the content.

---

## Privacy

Using this tool on GitHub Pages is **no different** than downloading and running it locally.

The HTML file is loaded once by your browser. After that, all processing happens entirely on your device. When you paste URLs into the tool, nothing is transmitted, logged, or sent anywhere.

GitHub cannot see what you paste or what the tool generates. There are no analytics, no tracking, and no network requests after the page loads.

---

## Running Locally

1. Click **Code → Download ZIP**
2. Unzip the folder
3. Open `index.html` in any browser

No setup required.

---

## Requirements

Any modern browser (Chrome, Safari, Firefox, Edge). Works on macOS, Windows, and mobile.

## Questions or Issues

Open an issue in this repository and include the URL type you used and the output you received.
