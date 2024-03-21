[![Visual Studio Marketplace Downloads](https://img.shields.io/visual-studio-marketplace/d/ahmadalli.vscode-nginx-conf)](https://marketplace.visualstudio.com/items?itemName=ahmadalli.vscode-nginx-conf)

# Nginx config file hint(auto-completion) for VS Code

[![.github/workflows/ci.yaml](https://github.com/ahmadalli/vscode-nginx-conf-hint/actions/workflows/ci.yaml/badge.svg)](https://github.com/ahmadalli/vscode-nginx-conf-hint/actions/workflows/ci.yaml)


A Visual Studio Code extension that helps you write Nginx configuration files. 
Many features in it include syntax highlight, auto-complete, in-editor documents, embedded Lua block, and more.


# Why Fork?

The [upstream repo] seems to be left unmaintained and there was compatibility issue with `raynigon.nginx-formatter` extension because the upstream projects used `NGINX` as language id while the formatter extension uses `nginx` and therefore it's not possible to use both extensions on the same file

## Installation

1. Click `Extension` button in left side of VSCode. (Shortcut: <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd> or <kbd>Command</kbd>+<kbd>Shift</kbd>+<kbd>X</kbd>)
2. Search for `ahmadalli.vscode-nginx-conf-hint` and click the `Install` button.

## Screenshots

![screenshots](https://raw.githubusercontent.com/ahmadalli/vscode-nginx-conf/master/images/screenshots.gif)

## Features

1. Syntax highlight for Nginx configuration file
2. Support syntax of Lua block in Nginx configuration file
3. Autocomplete directives, variables, location, media types, path, and more
4. Hint directive arguments and usage
5. Provide Nginx snippets
6. Provide directives and snippets from [OpenResty](https://github.com/openresty/)
7. Menu item "Goto Nginx Document" for display related Nginx document in the editor 

## Changelog

### 0.3.1 (2024-02-29)

1. Update hint data to Dec 5th, 2023. @AdrianDsg
	- Nginx directives
	- Lua Resty directives
	- HTTP headers
	- MIME types
2. Add completion for HTTP headers
3. Add two file extension names `.conf.default` and `.conf.template`. @halilim
4. Fix syntax for constant values, language keywords
	- <https://github.com/hangxingliu/vscode-nginx-conf-hint/commit/49159c02fd09dce264ded7802c9499a0f09646f5>
5. Update Nginx beautifier

### 0.3.0 (2021-11-20)

:mega: There are a lot of updates in this version:

1. The syntax of the Nginx configuration file is updated completely
	- Because the syntax from sublime extension and shanoor's repo are long time no updates. So I write a syntax generator for better highlight
	- New syntax is generated from codes. You can find them in [generate-tmLanguage.ts](src/syntax/generate-tmLanguage.ts)
	- New syntax supports embedded Lua block
	- New syntax supports the directive statement in multiple lines
	- And extension configuration `nginx-conf-hint.syntax` is removed
2. Optimize hint data loader and document loader. They use less memory now and load data on demand
3. This extension can run as a web extension. So you can use this extension on <https://vscode.dev/> now
4. The coverage of auto-completion is more, and auto-completion is smarter
	1. Auto completion is based on the context and grammar of the configuration now
	2. Fix some wrong auto-completion items
	3. Autocomplete named location
	4. Autocomplete directive's named argument
	5. Autocomplete media types 
5. Add editor definition support for `location` directive
6. Add new extension configuration `nginx-conf-hint.externalModules` for controlling enabled of external modules hint data
7. The source code is rewritten by using Typescript

[CHANGELOG.md](docs/CHANGELOG.md)   
[更新日志](docs/CHANGELOG.zh-Hans.md)

## Declaration

1. Icon image of this extension is from extension [nginx.conf][icon-nginx] 
2. This project uses the file [src/libs/nginxbeautifier.js](src/libs/nginxbeautifier.js) from <https://github.com/vasilevich/nginxbeautifier>
3. This extension is published under the [GPL-3.0 license](LICENSE)

## Building & Contributing

Please check out the document [CONTRIBUTING.md](docs/CONTRIBUTING.md) for information 
about building/contributing this project

[Pull Request][pr] & [Issues][issues]

## Author

[LiuYue(hangxingliu)](https://github.com/hangxingliu): Author of the [Original Project][upstream-repo]

[ahmadali shafiee](https://github.com/ahmadalli)

## Contributors

- [Adrian Dischinger](https://github.com/AdrianDsg): Contributor of the [Original Project][upstream-repo]
- [Halil Özgür](https://github.com/halilim): Contributor of the [Original Project][upstream-repo]
- [@tiansin](https://github.com/tiansin): Contributor of the [Original Project][upstream-repo]
- [@latipun7](https://github.com/latipun7): Contributor of the [Original Project][upstream-repo]


[nginx-doc]: https://nginx.org/en/docs/
[doc-script]: https://github.com/ahmadalli/vscode-nginx-conf-hint/blob/master/utils/download_hint_data.js
[icon-nginx]: https://github.com/shanoor/vscode-nginx/blob/master/nginx_logo.png
[issues]: https://github.com/ahmadalli/vscode-nginx-conf/issues
[pr]: https://github.com/ahmadalli/vscode-nginx-conf/pulls
[changelog]: https://github.com/ahmadalli/vscode-nginx-conf/blob/master/docs/CHANGELOG.md
[upstream-repo]: https://github.com/hangxingliu/vscode-nginx-conf-hint
