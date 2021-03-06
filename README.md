# BetterTwig

![LICENSE](https://img.shields.io/badge/LICENSE-MIT-green?style=for-the-badge)    ![LICENSE](https://img.shields.io/badge/ST-Build%203092+-orange?style=for-the-badge&logo=sublime-text) ![Tag](https://img.shields.io/github/v/tag/Sublime-Instincts/BetterTwig?style=for-the-badge&logo=github&sort=semver)

A Sublime Text package that offers enhanced syntax highlighting, snippets, completions and much more for PHP [Twig](https://twig.symfony.com/) templates. Read more for the full documentation.

## Features

- Indentation for code blocks.
- Snippets for common code blocks.
- Enhanced syntax highlighting for Twig templates.
- Autocompletions for built in tags, filters, functions, tests & loop variables.

## Installation

#### Package Control
The best way is to install it via [Package Control](https://packagecontrol.io/). Once you have Package Control setup in Sublime Text, open the command palette and search for `Package Control: Install Package`. Search for `BetterTwig` and install it. Package Control will take care for of automatically updating the package for you if there are new releases.

You can also use `Package Control: Add Repository`. Copy the github url (without the `.git` at the end) and enter it into the input panel that pops up at the bottom when you select `Package Control: Add Repository`. Now use `Package Control: Install Package` and search for `BetterTwig` and install it.

## Documentation

### Key bindings

- The key bindings are configured so that pressing <kbd>shift + {</kbd> **twice** will automatically add spaces on both sides for the inner brace expression block & place the cursor in the center, like so `{{ | }}`.
- |||ly pressing <kbd>shift + %</kbd> within `{}` will add spaces on both sides of the inner `%` like so `{% | %}`
- Use <kbd>ctrl + /</kbd> or <kbd>ctrl + shift + /</kbd> for Twig comments (`{# This is a Twig comment #}`)

### Auto completions
In order to get the auto completions, go to `Preferences: Settings` from the command palette and paste the following in the `Preferences.sublime-settings -- User` (the right hand window)

```json
"auto_complete_selector": "text.html.twig, meta.tag - punctuation.definition.tag.begin, source - comment - string.quoted.double.block - string.quoted.single.block - string.unquoted.heredoc",
"auto_complete_triggers":
[
	{"characters": "<", "selector": "text.html"},
	{"selector": "text.html.twig, text.html.basic"},
]
```

If you already have these in your user settings, then just copy the Twig related portions into them.

### Snippets

| **Tab Trigger** |          **Twig Code Block**          |
|-----------------|---------------------------------------|
| `tapply`        | `{% apply %}{% endapply %}`           |
| `tautoescape`   | `{% autoescape %}{% endautoescape %}` |
| `tblock`        | `{% block %}{% endblock %}`           |
| `tdeprecated`   | `{% deprecated %}`                    |
| `tembed`        | `{% embed %}{% endembed %}`           |
| `textends`      | `{% extends %}`                       |
| `tfor`          | `{% for %}{% endfor %}`               |
| `tforelse`      | `{% for %}{% else %}{% endfor %}`     |
| `tmacro`        | `{% macro %}{% endmacro %}`           |
| `tsandbox`      | `{% sandbox %}{% endsandbox %}`       |
| `tset`          | `{% set %}`                           |
| `tverbatim`     | `{% verbatim %}{% endverbatim %}`     |
| `twith`         | `{% with %}{% endwith %}`             |

## Issues & Feature requests.

There is always scope for improvements so please do report any bug(s) that you encounter or request for feature(s) that this package should support.

Please follow the issue & feature request templates that have been setup while reporting any bug(s) or requesting for feature(s) (So as to stay as organised as possible).

Use the [Twig playground](https://twigfiddle.com/) if you want to share a particular snippet of template while creating a specific issue.

## License
The MIT License (MIT)

Copyright 2020 &copy; Ashwin Shenoy

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.