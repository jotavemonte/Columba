# [Columba](https://marketplace.visualstudio.com/items?itemName=jotavemonte.Columba)

This project is a fork of the [Django-Test-Runner](https://github.com/Pachwenko/VSCode-Django-Test-Runner) and aims to be an user friendly django test runner.

## Features

Default shortcuts:

```
Run Closest Test Method: cmd+d+m        extension.djangoTestRunner.runMethodTests
Run Closest Test Class:  cmd+d+c        extension.djangoTestRunner.runClassTests
Run Current Test File:   cmd+d+f        extension.djangoTestRunner.runFileTests
Run Current App Tests:   cmd+d+a        extension.djangoTestRunner.runAppTests
Run Previous Tests:      cmd+d+p        extension.djangoTestRunner.runPreviousTests
```

VSCodevim keybindings (put these in your settings.json file):

```
"vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": ["leader", "d", "m"],
      "commands": ["python.djangoTestRunner.runMethodTests"]
    },
    {
      "before": ["leader", "d", "c"],
      "commands": ["python.djangoTestRunner.runClassTests"]
    },
    {
      "before": ["leader", "d", "f"],
      "commands": ["python.djangoTestRunner.runFileTests"]
    },
    {
      "before": ["leader", "d", "a"],
      "commands": ["python.djangoTestRunner.runAppTests"]
    },
    {
      "before": ["leader", "d", "p"],
      "commands": ["python.djangoTestRunner.runPreviousTests"]
    }
],
```

## Extension Settings

This extension contributes the following settings:

- `python.djangoTestRunner.djangoNose`: if checked will use django-nose syntax for running class/method tests inside a file, defaults to non-nose testing syntax
- `python.djangoTestRunner.flags`: any flags you wish to run such as --nocapture, also useful for specifying different settings if you use a modified manage&#46;py
- `python.djangoTestRunner.prefixCommand`: any command(s) to be directly before the main test command e.g. "cd ~/Projects/hello-world/src &&" to cd into the directory containing your manage&#46;py
- `python.djangoTestRunner.manageFilePath`: manage.py file path relative to workspace. Also works if you user a custom file e.g manage.sh which receives the test params

## Known Issues

- Default shortcuts may or may not work and require setting them manually

Open a issue/feature request and more at [the github repository](https://github.com/jotavemonte/VSCode-Django-Test-Runner/issues)
