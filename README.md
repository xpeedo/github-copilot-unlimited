# github-copilot-unlimited
For those who farm GitHub Copilot Trials and they don't want to break their git configuration.
Note: this topic doesn't cover how to get the gho_<TOKEN> token!

# Motivation
VSCode doesn't really support multiple github accounts at all. One account per VSCode instance (under the same machine). So I decided to look for an approach on how to use GitHub Copilot without messing my configuration. If you mess your GitHub Copilot extension you can reinstall it, no problem.

# How to do that
Go to:
```js
%userprofile%\.vscode\github.copilot-<VERSION>\dist\extension.js
```
and replace:
```js
,new Pc("GitHubLoginFailed")}
```
with =>
```js
,new Pc("GitHubLoginFailed")}n.accessToken="gho_<TOKEN>";
```
