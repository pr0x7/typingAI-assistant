# typingAI-assistant
AI powered typing assistant with Ollama

A script that can run in the background and listen to hotkeys, then uses a Large Language Model to fix or paraphrase the text.
## Get Started

### 1. Set up Ollama

Ollama Installation: https://github.com/ollama/ollama

Run `ollama run mistral:7b-instruct-v0.2-q4_K_S`

Mistal 7B Instruct works well for this task, but feel free to try other models, too :)

### 2. Install dependencies
```
pip install pynput pyperclip httpx
```

- pynput: https://pynput.readthedocs.io/en/latest/
- pyperclip: https://github.com/asweigart/pyperclip
- httpx: https://github.com/encode/httpx/

### 3. Run it

Start the assistant:

```
python main.py
```

Hotkeys you can then press:
- F8: Paraphrases the current selection
- F9: Fixes the current line (without having to select the text)
- F10: Fixes the current selection

**Note**: You may get an error the first time saying `This process is not trusted! Input event monitoring will not be possible until it is added to accessibility clients`. On Mac, you need to add the script (IDE/terminal) both on accessibility and input monitoring.

**Note**: The code works on macOS. The underlying shortcuts in the code like Cmd+Shift+Left, Cmd+C, Cmd+V might have to be changed for Linux & Windows (e.g. `Key.cmd` -> `Key.ctrl`).
