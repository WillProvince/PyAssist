# PyAssist: Personalized AI Assistant Implementation

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

PyAssist is an advanced Python implementation for creating personalized AI assistants through OpenAI's API. This script enables local execution of intelligent agents capable of program execution ,file management, web interactions, and contextual conversations, with persistent memory that evolves through continued use.

## Key Features

- **Cognitive Progression System**
  - Develops persistent memory across sessions
  - Improves interaction quality through usage patterns
- **Multi-Modal Capabilities**
  - **File Operations**: Create, modify, and open local files
  - **Web Integration**: Real-time search and data retrieval
  - **Voice & Text**: Dual interaction channels with TTS/STT
- **Contextual Awareness**
  - Maintains conversation history
  - Adaptive response generation
- **Enterprise-Grade Tooling**
  - Automated logging system
  - Thread-based conversation management
  - API extensions (Google, ScaleSERP, Tomorrow.IO)

## Getting Started

### Prerequisites
- Python 3.8+
- OpenAI API Key (Required)
- Google API Key (Optional, for voice features)
- ScaleSERP API Key (Optional, for web search)
- Tomorrow.IO API Key (Optional, for weather)

### Installation
1. Clone repository
   ```bash
   git clone https://github.com/yourusername/PyAssist.git
   cd PyAssist
2. Install dependencies
  ```bash
  pip install -r requirements.txt
  ```

### Configuration
1. Rename RenameThisFile.env to .env
2. Populate API keys in .env:

```ini
OPENAI_APIKEY = "OpenAI API Key Here"
WEATHERAPI = "Tomorrow.IO API Key Here"
GOOGLE_API = "Google API Key Here"
SERPAPI = "ScaleSERP API Key Here"
```
Customize assistant parameters:
```ini
MODEL = "gpt-4o"
INSTRUCTIONS = "You are a helpful AI assistant..."
NAME = "Companion"
TOOL_LIST = "func.txt"
```
## Usage
### Launching the Application
```bash
python main.py
```
### Interaction Modes
| Mode | Description | Features |
| --- | --- | --- |
| Text-Based | Traditional chat interface | Command palette, File uploads |
| Voice | Speech-enabled interactions | TTS responses, STT processing |

### Command Reference
| Command | Description | Usage Example |
| --- | --- | --- |
| help | Display command help | help |
| clear | Create new conversation thread | clear |
| retrieve | Resume existing thread | retrieve thread_abc123 |
| upload | Submit file with query | upload data.csv |
| speech | Toggle TTS responses | speech |
| ids | Show API resource identifiers | ids |
| exit | Terminate application | exit |

### Conversation Logging
PyAssist maintains detailed logs in ```thread_logs/``` with:
- Full message history
- Tool call details
- System operations
- File attachments
### Sample log structure:
```
User: Can you tell me the time?
------------------------------------------------
Assistant: 
------------------------------------------------
TOOL CALL
Tool Name: "get_time"
Parsed Arguments:{'time_zone': 'America/New_York', 'format': '12hr'}
------------------------------------------------
Assistant: The current time in New York City, NY is 10:14 AM. How can I help you further?
```
## Support & Contribution
For issues or feature requests, please open an issue.

## License
Distributed under MIT License. See LICENSE for details.
