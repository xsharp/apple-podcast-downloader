# Apple Podcast Downloader - Claude Skill

A comprehensive Claude Code skill for searching, browsing, and downloading podcast episodes from Apple Podcasts.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Claude Code](https://img.shields.io/badge/Claude-Code-blue.svg)](https://claude.ai/code)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

## ✨ Features

- 🔍 **Smart Search** - Find podcasts by keyword, author, or topic across Apple Podcasts
- 📋 **Episode Browser** - Browse episodes with rich metadata (title, date, duration, description)
- 📥 **Audio Download** - Download episodes as MP3 files with progress tracking
- 🌏 **Unicode Support** - Full support for Chinese, Japanese, Korean, and other languages
- 📊 **Rich Metadata** - Access RSS feeds, artwork, ratings, and detailed information
- ⚡ **Zero Dependencies** - Uses only Python 3 standard library
- 🔐 **No Auth Required** - Free Apple iTunes API with no authentication needed

## 🚀 Quick Start

### Installation

1. **Install as Claude Code Skill**:
   ```bash
   # Clone this repository to your Claude skills directory
   cd ~/.claude/skills/
   git clone https://github.com/BurnWang/apple-podcast-downloader.git

   # Or for project-specific installation
   cd your-project/.claude/skills/
   git clone https://github.com/BurnWang/apple-podcast-downloader.git
   ```

2. **That's it!** No additional dependencies required.

### Basic Usage

Simply ask Claude natural questions:

```
"Find podcasts about Python programming"
"Download the latest episode of The Daily"
"Show me the 5 most recent Talk Python To Me episodes"
"Search for 绿皮火车 podcast"  (Chinese search works!)
```

### Manual Usage

You can also use the helper script directly:

```bash
# Search for podcasts
python3 scripts/itunes_api.py search "keyword" 10

# Get episodes from a podcast
python3 scripts/itunes_api.py episodes 1200361736 5

# Download an episode
python3 scripts/itunes_api.py download 1200361736 0 downloads/
```

## 📚 Documentation

- **[SKILL.md](SKILL.md)** - Main skill definition for Claude
- **[examples.md](examples.md)** - 8 detailed usage examples
- **[reference.md](reference.md)** - Complete API reference

## 🎯 Use Cases

### 1. Quick Download
User: "Download the latest episode of Python Bytes"
Claude: Searches → Displays episode → Downloads automatically

### 2. Browse and Choose
User: "Show me recent episodes of The Daily"
Claude: Lists 10 latest episodes → User picks → Downloads

### 3. Batch Operations
User: "Download episodes 1, 3, and 5 from Talk Python"
Claude: Fetches list → Downloads selected episodes

### 4. International Podcasts
User: "搜索绿皮火车播客"
Claude: Works seamlessly with Chinese characters!

## 🛠️ Technical Details

### Architecture

```
apple-podcast-downloader/
├── SKILL.md              # Claude skill definition
├── README.md             # This file
├── examples.md           # Usage examples
├── reference.md          # API documentation
├── LICENSE               # MIT License
└── scripts/
    └── itunes_api.py     # Python helper script
```

### How It Works

1. **Search**: Uses iTunes Search API to find podcasts
2. **Browse**: Fetches episode metadata using podcast ID
3. **Download**: Streams audio files directly from CDN with progress tracking

### API Information

- **Provider**: Apple iTunes Search API
- **Authentication**: None required
- **Rate Limits**: ~20 requests/second (unofficial)
- **Cost**: Free

## 🔧 Advanced Features

### Supported Formats
- Audio: MP3, M4A (auto-downloaded)
- Metadata: JSON output for programmatic access

### Error Handling
- Network errors with retry suggestions
- Invalid IDs with helpful messages
- Unicode encoding for international content

### Performance
- Streaming downloads for large files
- Progress indicators for downloads >10MB
- Efficient JSON parsing

## 🤝 Contributing

Contributions are welcome! Here's how:

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Built for [Claude Code](https://claude.ai/code)
- Uses [Apple iTunes Search API](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/iTuneSearchAPI/)
- Created as a teaching example for NotebookLM tutorial

## 🎓 Educational Value

This skill is an excellent example for learning:
- Claude Code skill development
- REST API integration
- File download with progress tracking
- Unicode handling in Python
- Error handling and user experience

Perfect for tutorials and workshops on building Claude skills!

---

**Made with ❤️ by BurnWang**
