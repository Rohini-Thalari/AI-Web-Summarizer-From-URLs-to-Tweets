# 🐦 AI Web Summarizer — From URLs to Tweets

> Paste any URL. Get an AI-powered summary + ready-to-post tweet variants in seconds.

---

## 📌 Overview

**AI Web Summarizer** is an AI-powered web tool that takes any public article or webpage URL and automatically:
- Fetches and reads the page content
- Generates a concise 2–3 sentence summary
- Produces multiple tweet variants in your chosen tone — all under 280 characters

Built using the **Anthropic Claude API** with web search capabilities, this tool bridges the gap between long-form content and social media-ready output.

---

## ✨ Features

- 🔗 **URL-based input** — paste any public webpage URL
- 🧠 **AI-powered summarization** — Claude reads and understands the article
- 🐦 **Tweet generation** — 1 to 4 tweet variants per request
- 🎭 **Tone selection** — choose from Insightful, Casual, Thread Starter, Bold, or Educational
- 📋 **One-click copy** — instantly copy any tweet variant to clipboard
- 📊 **Character counter** — live 280-character limit indicator per tweet
- ⚡ **Real-time web search** — Claude fetches the latest content from the URL at runtime

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML / CSS / JavaScript | Frontend UI |
| Anthropic Claude API (`claude-sonnet-4`) | Summarization & tweet generation |
| Claude Web Search Tool (`web_search_20250305`) | Fetching live URL content |
| Fetch API | API communication |

---

## 🚀 Getting Started

### Prerequisites

- An [Anthropic API key](https://console.anthropic.com/)
- A modern web browser

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Rohini-Thalari/AI-Web-Summarizer-From-URLs-to-Tweets-.git
   cd AI-Web-Summarizer-From-URLs-to-Tweets-
   ```

2. **Open the project**
   - Simply open `index.html` in your browser, or serve it locally:
   ```bash
   npx serve .
   ```

3. **Configure your API key**
   - The app uses the Anthropic API directly from the browser.
   - Make sure your API key is configured in the relevant config or environment file.

---

## 🧪 How to Use

1. Paste a public article or webpage URL into the input field
2. Select your preferred **tweet tone** (Insightful, Casual, Thread Starter, Bold, Educational)
3. Choose the **number of tweet variants** (1–4) using the slider
4. Click **"Summarize & Generate Tweets"**
5. View the AI-generated summary and tweet variants
6. Click **Copy** on any tweet to copy it to your clipboard

---

## 📸 Demo

```
URL Input:  https://example.com/article-about-ai

Summary:
  AI is transforming industries by automating repetitive tasks and enabling 
  smarter decision-making. Recent breakthroughs in large language models have 
  accelerated adoption across healthcare, finance, and education.

Tweet Variants:
  [Insightful] AI isn't just automation — it's redefining how we make decisions 
  across healthcare, finance & education. The LLM era is just getting started. 
  #AI #FutureOfWork

  [Bold] Hot take: The next decade belongs to whoever builds AI-first workflows. 
  Late adopters will be left behind. #AIStrategy #Innovation
```

---

## 🎨 Tone Options

| Tone | Description |
|---|---|
| **Insightful** | Thought-provoking, data-driven angle |
| **Casual** | Conversational and easy to read |
| **Thread Starter** | Hooks the reader to continue reading |
| **Bold** | Strong opinion or contrarian take |
| **Educational** | Informative and clear explanation |

---

## 📁 Project Structure

```
AI-Web-Summarizer-From-URLs-to-Tweets-/
├── index.html          # Main application file
├── style.css           # Styling (if separate)
├── app.js              # Core JavaScript logic
└── README.md           # Project documentation
```

---

## 🔐 API Usage

This project uses the Anthropic Messages API with the built-in web search tool:

```javascript
const response = await fetch("https://api.anthropic.com/v1/messages", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({
    model: "claude-sonnet-4-20250514",
    max_tokens: 1000,
    tools: [{ type: "web_search_20250305", name: "web_search" }],
    messages: [{ role: "user", content: prompt }]
  })
});
```

---

## ⚠️ Limitations

- Only works with **publicly accessible** URLs (no login-gated content)
- Tweet generation depends on the quality and length of the source article
- API rate limits apply based on your Anthropic plan

---

## 🤝 Contributing

Contributions are welcome! To get started:

1. Fork the repository
2. Create a new branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit: `git commit -m "Add your feature"`
4. Push to the branch: `git push origin feature/your-feature-name`
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👩‍💻 Author

**Rohini Thalari**
- GitHub: [@Rohini-Thalari](https://github.com/Rohini-Thalari)

---

> Made with ❤️ using Claude AI
