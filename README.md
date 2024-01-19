# github-copilot-unlimited
For those who farm GitHub Copilot Trials and they don't want to break their git configuration.
Note: this repo doesn't cover how to get the `gho_<TOKEN>` token!

# Motivation
VSCode doesn't really support multiple github accounts at all. One account per VSCode instance (under the same machine). So I decided to look for an approach on how to use GitHub Copilot without messing my configuration. If you mess your GitHub Copilot extension you can reinstall it, no problem.

# How to do that (Windows)
Go to:
```js
%userprofile%\.vscode\github.copilot-<VERSION>\dist\extension.js
```
and replace:
```js
"GitHubLoginFailed")}
```
with =>
```js
"GitHubLoginFailed")}n.accessToken="gho_<TOKEN>";
```

For GitHub Copilot Chat you have to do this:
```js
%userprofile%\.vscode\extensions\github.copilot-chat-<VERSION>\dist\extension.js
```
and replace:
```js
{token:r.accessToken});return
```
with =>
```js
{token:"gho_<TOKEN>"});return
```

For different OS, like Linux and MacOS should be similar.

When the GitHub Copilot trials expires or GitHub Copilot VSCode extension gets updated, you have to repeat this process (kinda).

# Disclaimer
If you use this day by day you might buy GitHub Copilot license instead. If you can't afford it, just use this method.
