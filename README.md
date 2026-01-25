<div align="center">

# WeChat to NotebookLM

**Automatically sync WeChat Official Account articles to Google NotebookLM for AI-powered analysis, summarization, and content generation**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude_Code-Skill-blue)](https://claude.ai/claude-code)

</div>

## ✨ Features

- 🚀 **One-click sync** - Automatically fetch WeChat articles and add them to NotebookLM
- 📝 **Markdown conversion** - Clean, well-formatted Markdown output
- 🤖 **AI-powered** - Leverage NotebookLM's AI for analysis and content generation
- 🎙️ **Content generation** - Create podcasts, videos, and quizzes from articles
- 💬 **Interactive chat** - Ask questions and get insights from your articles

## 📋 What This Does

This skill automates the entire workflow of getting a WeChat article into NotebookLM:

1. **Fetches** the article content from the URL
2. **Converts** to clean Markdown format
3. **Creates** a NotebookLM notebook
4. **Uploads** the article as a source
5. **Returns** the notebook ID for further interaction

## 🎯 When to Use

Use this skill when you:
- Have a WeChat Official Account article URL (`mp.weixin.qq.com`)
- Want to save the article to NotebookLM for analysis
- Want to create a podcast/video from the article
- Want to chat with the article content using AI
- Want to summarize or extract insights from the article

## 📦 Installation

### Prerequisites

1. **Claude Code** - This skill requires Claude Code CLI
2. **NotebookLM CLI** - Install and authenticate NotebookLM CLI:

```bash
# Install NotebookLM CLI
npm install -g @notebooklm/cli

# Authenticate with Google
notebooklm login

# Verify authentication
notebooklm status
```

### Install the Skill

Clone this repository to your local skills directory:

```bash
# Navigate to your Claude skills directory
cd ~/.claude/skills

# Clone the repository
git clone https://github.com/zstmfhy/wechat-to-notebooklm.git
```

## 🚀 Usage

### Basic Usage

Simply provide a WeChat article URL:

```
Sync this WeChat article to NotebookLM: https://mp.weixin.qq.com/s/xxxxx
```

The skill will:
1. ✅ Fetch the article content
2. ✅ Convert to Markdown
3. ✅ Create a notebook
4. ✅ Upload the article
5. ✅ Return the notebook ID

### Example Workflow

**User**: "Sync this WeChat article to NotebookLM: https://mp.weixin.qq.com/s/xxxxx"

**Agent response**:
```
✅ Fetching article from WeChat...
✅ Converting to Markdown...
✅ Creating notebook "Article Title"...
✅ Uploading to NotebookLM...
✅ Done!

📓 Notebook: Article Title
   ID: abc-123-def

📄 Source: article_title.md
   ID: source-xyz-789

💡 Next steps:
   - Chat: notebooklm ask "Summarize this article"
   - Generate: notebooklm generate audio "Create a podcast"
```

## 🛠️ Advanced Features

### Add to Existing Notebook

```bash
# List existing notebooks
notebooklm list --json

# Add to specific notebook
notebooklm source add /tmp/article.md --notebook <existing_notebook_id> --json
```

### Batch Processing

```bash
# Create a collection notebook
notebooklm create "WeChat Articles Collection" --json

# Add multiple articles to the same notebook
# (The skill will handle this automatically)
```

### Content Generation

After uploading, you can:

**Generate a Podcast:**
```bash
notebooklm generate audio "Create an engaging podcast about this article"
```

**Create a Video:**
```bash
notebooklm generate video "Make an explanatory video"
```

**Generate Quiz:**
```bash
notebooklm generate quiz "Test understanding of key concepts"
```

**Ask Questions:**
```bash
notebooklm ask "What are the key insights?"
notebooklm ask "Summarize in 3 bullet points"
```

## 📚 Command Reference

| Task | Command/Tool |
|------|--------------|
| Fetch article | `mcp__web_reader__webReader` |
| Create notebook | `notebooklm create "Title" --json` |
| Upload file | `notebooklm source add file.md --notebook <id> --json` |
| Check sources | `notebooklm source list --notebook <id> --json` |
| Chat with article | `notebooklm use <id>; notebooklm ask "question"` |
| Generate podcast | `notebooklm generate audio "instructions" --notebook <id>` |

## 🔧 Troubleshooting

### Article URL is invalid or inaccessible
- **Error**: Failed to fetch content
- **Solution**: Verify the URL is correct and accessible
- **Alternative**: Try copying the article content manually

### NotebookLM authentication failed
- **Error**: Auth/cookie error
- **Solution**: Run `notebooklm login` again
- **Check**: `notebooklm status` to verify

### File upload failed
- **Error**: Invalid file or upload error
- **Solution**: Check if Markdown file was created correctly
- **Verify**: File path and permissions

### Notebook creation failed
- **Error**: Rate limiting or API error
- **Solution**: Wait a few minutes and retry
- **Alternative**: Add to existing notebook with `--notebook` flag

## ⚠️ Limitations

- **WeChat articles only**: Optimized for `mp.weixin.qq.com` URLs
- **Text content**: Focuses on text, images are preserved as links
- **Public articles**: Requires publicly accessible articles
- **Rate limits**: NotebookLM has rate limits on uploads

## 💡 Best Practices

1. **Use descriptive notebook titles** - Extract from article title or topic
2. **Keep articles organized** - Use separate notebooks for different topics
3. **Verify uploads** - Check `notebooklm source list` after upload
4. **Clean up temp files** - Remove `/tmp` files after successful upload
5. **Handle rate limits** - If uploads fail, wait 5-10 minutes before retry

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Claude Code](https://claude.ai/claude-code) - The AI CLI tool that powers this skill
- [NotebookLM](https://notebooklm.google.com/) - Google's AI-powered research and note-taking tool
- [WeChat](https://weixin.qq.com/) - The source of amazing content

## 📮 Contact

- GitHub: [@zstmfhy](https://github.com/zstmfhy)
- Issues: [Create an issue](https://github.com/zstmfhy/wechat-to-notebooklm/issues)

---

<div align="center">
Made with ❤️ by the open-source community
</div>
