[![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/ahmadalli.vscode-nginx-conf)](https://marketplace.visualstudio.com/items?itemName=ahmadalli.vscode-nginx-conf)

# Nginx config file hint(auto-completion) for VS Code

An **experimental** extension.   
And the hint data generated from [nginx document web page][nginx-doc] by [scripts][doc-script]    
You can report bug or send a feature suggestion in [Github Issues Page][issues].

# Why Fork?

The [upstream repo] seems to be left unmaintained and there was compatibility issue with `raynigon.nginx-formatter` extension because the upstream projects used `NGINX` as language id while the formatter extension uses `nginx` and therefore it's not possible to use both extensions on the same file

## Installation

1. Click `Extension` button in left side of VSCode. (Shortcut: <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd>)
2. Search `nginx.conf hint`. Found this extension and click `Install` button.
3. Reload VSCode.

## Screenshots

![screenshots](https://raw.githubusercontent.com/ahmadalli/vscode-nginx-conf/master/images/screenshots.gif)

## Features

1. provide highlight for Nginx configuration file.
2. auto complete nginx directives and embedded variables
3. hint directive default parameters
4. hint directives syntax 
5. nginx block snippets
6. "Goto Nginx Document" for each directives and variables

## Changelog

### 0.1.0 (2018-07-09)

1. syntax of nginx.conf is provided inside.
	- `original` syntax is from [shanoor/vscode-nginx][shanoor-syntax] (**by default**)
	- `sublime` syntax is from [sublime-nginx][sublime-syntax]
	- you can switch it by configuration: `nginx-conf-hint.syntax`
2. remove dependent extension `shanoor.vscode-nginx`.
3. update Nginx hint data(directives and variables) to latest.

[CHANGELOG.md][changelog]

## Declaration

1. Nginx config syntaxes file from [sublime-nginx][sublime-nginx] repo and [shanoor/vscode-nginx][shanoor-nginx] repo 
2. Icon image of this extension is from extension [nginx.conf][icon-nginx] 
3. This extension is published under the [GPL-3.0 license](LICENSE)

## Contributing to the Extension

- useful nginx.conf snippets 
- report bug via Github issues
- helpful pull request
- give me coffee to make extension better and better via [Paypal][paypal]

[Pull Request][pr] & [Issues][issues]

[CONTRIBUTING.md](CONTRIBUTING.md)

## Author

[LiuYue(hangxingliu)](https://github.com/hangxingliu): Author of the [Original Project][upstream-repo]
[ahmadali shafiee](https://github.com/ahmadalli)

## Contributor

- [@tiansin](https://github.com/tiansin): Contributor of the [Original Project][upstream-repo]



[nginx-doc]: https://nginx.org/en/docs/
[doc-script]: https://github.com/ahmadalli/vscode-nginx-conf/blob/master/utils/download_hint_data.js
[shanoor-syntax]: https://github.com/shanoor/vscode-nginx/blob/master/syntaxes/nginx.tmLanguage
[sublime-syntax]: https://github.com/brandonwamboldt/sublime-nginx/blob/master/Syntaxes/nginx.tmLanguage
[shanoor-nginx]: https://github.com/shanoor/vscode-nginx
[sublime-nginx]: https://github.com/brandonwamboldt/sublime-nginx
[icon-nginx]: https://github.com/shanoor/vscode-nginx/blob/master/nginx_logo.png
[issues]: https://github.com/ahmadalli/vscode-nginx-conf/issues
[pr]: https://github.com/ahmadalli/vscode-nginx-conf/pulls
[changelog]: https://github.com/ahmadalli/vscode-nginx-conf/blob/master/CHANGELOG.md
[upstream-repo]: https://github.com/hangxingliu/vscode-nginx-conf-hint
