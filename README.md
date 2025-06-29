 Overview
ClipMod is a Windows Forms clipboard enhancement tool built with C#. It includes features like clipboard history, global hotkey activation, emoji and GIF integration, and startup customization. You're using Guna UI2 controls for a modern interface.

 Features & Functionality
 Clipboard Monitoring
Tracks text and images copied to clipboard.

Maintains a history list of text (in lstText) and images (in flowImages).

Clicking a text or image re-copies it to clipboard with a confirmation message.

 Global Hotkey
Registers a hotkey (default: F5) to bring the app to the foreground.

Can be changed via btnHotkeySettings.

Hotkey registration uses RegisterHotKey and WndProc to intercept it globally.

 Emoji Loader
Emojis are loaded from the GitHub Gemoji JSON file.

Displayed in webViewEmojis using dynamically generated HTML.

Clicking on an emoji copies it to the clipboard.

Supports search filtering via txtSearch.

 Tenor GIF Integration
Loads GIFs from Tenor API (/v2/search).

Uses async scrolling in flowGifs to load more on scroll.

Clicking a GIF copies its URL.

Includes batching and search via txtSearch.

 Search
txtSearch filters:

Text history.

Image history.

Emojis by description.

GIFs by keyword.

📎 System Tray & Startup
Minimizes to system tray instead of closing.

Tray menu has “Open” and “Exit” options.

Autostart:

Attempts to register app to run at Windows startup via registry key:
HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run

Also has manual shortcut method (placing .lnk in %APPDATA%\Microsoft\Windows\Start Menu\Programs\Startup).

 Drag Window
panel1 acts as a drag surface for the frameless form using mouse events.

 Ads Panel
Loads an embedded WebView page (cuty.io/ads/adsterra.html) refreshed every 15 seconds.

Muted by default.

 Tech Details
UI Framework: Windows Forms + Guna UI2.

JSON Handling: System.Text.Json.

HTTP: HttpClient.

Clipboard: Monitored via AddClipboardFormatListener.

Interop: Global hotkeys registered using user32.dll.

Startup Registration: Via registry or startup folder shortcut.

WebView2: Used for both emoji and ad panels.

 Known Issues (from prior chats)
Emoji loading can fail if WebView2 isn't initialized or JSON changes.

Autostart via registry can silently fail on some systems without admin rights.

WshRuntimeLibrary errors when COM reference is missing.

TextBox/Guna Button UI had styling inconsistencies (white border resolved with FillColor, BorderColor, etc.).


Software It will work on:
As of now i feel it can work on almost any software in the world due to it's dynamic functionality but here are the software tested 

Discord
Roblox
Minecraft
Valorant
Cod
Gta V
War Thunder
Black myth wukong
Default Windows apps
Linux terminal's
Mac Folder icons

--------ETC--------

Releases:

As android and ios have a wide variety of custom emojis and gifs 
ClipMod will focus more on Windows, MacOs, Linux (Ubantu and Arch might kali or sm)

Status:
Windows Released - https://github.com/ANormalFreeModel/Anormalfreemodel

Linux in testing

Mac Still making
