# alfred-workflows

## 1Password Copy
Simple, hacky AppleScript to search and copy a password to the clipboard.
```osascript
tell application "System Events"
	set frontmostApplicationName to name of 1st process whose frontmost is true
	open location "onepassword://extension/search/{query}"
	set frontmost of process "1Password 7" to true
	key code 48
	key code 124
	key code 125
	key code 36
	set frontmost of process frontmostApplicationName to true
end tell
```
