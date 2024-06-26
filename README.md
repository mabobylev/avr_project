# AVR project template

- Using VSCode

## VSCode properties

- _c_cpp_properties.json_

```json
{
  "configurations": [
    {
      "name": "AVR",
      "includePath": ["${workspaceFolder}/**", "/usr/avr/include"],
      "browse": {
        "path": []
      },
      "defines": ["F_CPU 8000000UL", "__AVR_ATmega8A__"],
      "compilerPath": "/usr/bin/avr-gcc",
      "compilerArgs": [],
      "cStandard": "c11",
      "cppStandard": "gnu++11",
      "intelliSenseMode": "linux-gcc-arm",
      "configurationProvider": "ms-vscode.cmake-tools"
    }
  ],
  "version": 4
}
```

- _tasks.json_

```json
{
// See https://go.microsoft.com/fwlink/?LinkId=733558
// for the documentation about the tasks.json format
"version": "2.0.0",
"tasks": [
    {
        "label": "Build",
        "type": "shell",
        "command": "make",
        "args": [],
        "group": "build",
        "detail": "Build project",
        "presentation": {
            "reveal": "silent"
        },
        "problemMatcher": [
            "$gcc"
        ]
    },
    {
        "label": "Clean",
        "type": "shell",
        "command": "make",
        "args": ["clean"],
        "group": "build",
        "detail": "Clean project",
        "presentation": {
            "reveal": "silent"
        },
        "problemMatcher": [
            "$gcc"
        ]
    }
    ]
}
```
