---
layout: post
title: Text Editors - Customizations/Plugins/Hacks for Sublime, VS Code and Vim
categories: notes
last_modified_at: 2020-07-14 11:16:39
---

If you love coding text editors are your sharp tools. Customizing them to your needs will help you save time and increase productivity.

## Sublime Text

### How to use Python script with Key Bindings

We will create a sample package that will display time on status bar when we press keys `ctrl+shift+c`, just for demonstrating.

- Create a new python file inside Users Package Library. On Mac with Sublime Text 3 it can be created at: `Users/yourname/Library/Application Support/Sublime Text 3/Packages/User/any_name.py`

- In the python file add following content:

```py
import sublime
import sublime_plugin
import time

class MyCustomMessageCommand(sublime_plugin.WindowCommand):
    
    # Command shows message on Status Bar
    def run(self):
        now = time.strftime("%c")
        message = "The time is " + now
        sublime.status_message(message)
```

- Add the key bindings:

```py
[
  {
    "keys" : ["ctrl+shift+c"], 
    "command" : "my_custom_message" 
  }
]
```

As you can see that the python class name becomes the command name with _ added.

Now on pressing `ctrl+shift+c` you can execute this python file which displays the time on status bar in this case.

You can use this feature to unlimited possibilities. I used it to add timestamp to file whenever it was saved.

References:

- <https://forum.sublimetext.com/t/automatically-updated-timestamp/7156/7>

### Extending Sublime Text for Markdown Support

If you want more syntax highlighting and better preview of what you write then you can extend Sublime Text by installing  package, follow steps below:

- Type: ``Cmd + Shift + P`` to open package manager.
- Then type ``install package`` and hit enter. This will provide you list of available packages from packagecontrol.io
- Next when you get dropdown type ``Markdown`` and this will list you all markdown related packages.
- You can select ``Markdown Editing`` to install the package. This provides much better highlighting and preview.

I, personally, didn't like it much and was a bit distracting for me. So I removed this package. But you may like it.

Removing a package from Sublime Text:

- press ``Cmd + Shift + P`` and
- then type ``remove package``. This will give you list of packages installed and
- next select ``Markdown Editing`` to remove it.


## VS Code

Recently VS Code turned out to be best editor for Markdown however it is bit heavy. Also 'Markdown Preview' extension on Chrome makes it handy to preview markdown files. VS Code can be logged in using GitHub to start sync.

- Extensions can be disabled when not in use.
- open `~/.config/Code/User/settings.json` to add extension configurations
- add below codes within the curly braces

Markdownlint disable rules:

```json
  "markdownlint.config": {
    "default": true,
    "MD007": { "indent": 4 }
}
```

cSpell disable code check in Markdown code blocks:

```json
    "cSpell.languageSettings": [
        {
            // use with Markdown files
            "languageId": "markdown",
            // Exclude code inline and multiline both
            "ignoreRegExpList": [
                "^\\s*```[\\s\\S]*?^\\s*```",
                "\\s`[\\s\\S]*?\\s*`",
            ]
        }
    ],
```
