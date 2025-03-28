+++
title = 'VsCodeSetting配置'
date = 2024-11-12T21:31:17+08:00





categories = ["设置"] 

tags = ["setting" ]

+++



> 我的 `vscode` 的设置`.json`文件

# 最新 

# 2024.12.26



```json
{
    "editor.fontSize": 16,
    "cph.general.autoShowJudge": false,
    "editor.formatOnSave": true,
    "editor.formatOnType": true,
    "files.autoSave": "afterDelay",
    "git.confirmSync": false,
    "chat.editor.fontSize": 18,
    "window.zoomLevel": 1,
    "editor.mouseWheelZoom": true,
    "editor.wordWrap": "on",
    "debug.onTaskErrors": "debugAnyway",
    "explorer.confirmDelete": false,
    "extensions.experimental.affinity": {
        "asvetliakov.vscode-neovim": 1
    },
    "workbench.settings.applyToAllProfiles": [
        "editor.fontSize"
    ],
    "go.delveConfig": {},
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[markdown]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[prisma]": {
        "editor.defaultFormatter": "Prisma.prisma"
    },
    "[typescript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[typescriptreact]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "editor.codeActionsOnSave": {
        "source.addMissingImports": "explicit",
        "source.organizeImports": "explicit"
    },
    "editor.cursorSmoothCaretAnimation": "on",
    "editor.cursorSurroundingLines": 5,
    "editor.fontFamily": "CaskaydiaCove Nerd Font ",
    "editor.fontLigatures": true,
    "python.analysis.completeFunctionParens": true,
    "editor.fontSize": 18,
    "editor.fontWeight": "300",
    "editor.formatOnSave": true,
    "editor.inlineSuggest.enabled": true,
    "editor.lineNumbers": "relative",
    "editor.linkedEditing": true,
    "editor.smoothScrolling": true,
    "editor.stickyScroll.enabled": true,
    "editor.suggest.insertMode": "replace",
    "editor.suggestFontSize": 14,
    "editor.wordWrap": "on",
    "errorLens.fontStyleItalic": true,
    "everforest.italicKeywords": true,
    "explorer.confirmDelete": false,
    "explorer.confirmDragAndDrop": false,
    "extensions.autoUpdate": "onlyEnabledExtensions",
    "extensions.ignoreRecommendations": false,
    "files.exclude": {
        "**/node_modules": true
    },

    "typescript.preferences.importModuleSpecifier": "relative",
    "typescript.updateImportsOnFileMove.enabled": "always",
    "vim.foldfix": true,
    "vim.highlightedyank.color": "rgba(230, 97, 89, 0.7)",
    "vim.highlightedyank.enable": true,
    "vim.highlightedyank.textColor": "white",
    "vim.hlsearch": true,
    "vim.leader": "<space>",
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "leader",
                "r"
            ],
            "commands": [
                "editor.action.rename"
            ]
        },
        {
            "before": [
                "leader",
                "w"
            ],
            "commands": [
                ":w!"
            ]
        },
        {
            "before": [
                "leader",
                "q"
            ],
            "commands": [
                ":q!"
            ]
        },
        {
            "before": [
                "leader",
                "x"
            ],
            "commands": [
                ":x!"
            ]
        },
        {
            "after": [
                "g",
                "g",
                "V",
                "G"
            ],
            "before": [
                "<c-a>"
            ]
        },
        {
            "before": [
                "<leader>",
                "k"
            ],
            "commands": [
                "editor.action.showHover"
            ]
        },
        {
            "before": [
                "[",
                "d"
            ],
            "commands": [
                "editor.action.marker.prev"
            ]
        },
        {
            "before": [
                "]",
                "d"
            ],
            "commands": [
                "editor.action.marker.next"
            ]
        },
        {
            "before": [
                "<leader>",
                "c",
                "a"
            ],
            "commands": [
                "editor.action.quickFix"
            ]
        },
        {
            "after": [
                "^"
            ],
            "before": [
                "H"
            ]
        },
        {
            "after": [
                "$"
            ],
            "before": [
                "L"
            ]
        },
        {
            "before": [
                "leader",
                "i"
            ],
            "commands": [
                "extension.toggleBool"
            ]
        }
    ],
    "vim.useSystemClipboard": true,
    "window.zoomLevel": 1,
    "workbench.iconTheme": "vscode-great-icons",
    "workbench.settings.editor": "json",
    "workbench.startupEditor": "readme",
    "zenMode.hideLineNumbers": false,
    "[jsonc]": {
        "editor.quickSuggestions": {
            "strings": true
        },
        "editor.suggest.insertMode": "replace"
    },
    "terminal.integrated.defaultProfile.windows": "Windows PowerShell",
    "terminal.explorerKind": "external",
    "security.workspace.trust.enabled": false,
    "typescript.disableAutomaticTypeAcquisition": true,
    "git.enableSmartCommit": true,
    "git.openRepositoryInParentFolders": "always",
    "files.autoGuessEncoding": true,
    "code-runner.languageIdToFileExtensionMap": {
        "bat": ".bat",
        "powershell": ".ps1",
        "typescript": ".ts"
    },
    "vim.easymotion": true,
    "vim.easymotion": true,
    "vim.incsearch": true,
    "vim.useSystemClipboard": true,
    "vim.useCtrlKeys": true,
    "vim.hlsearch": true,
    "vim.insertModeKeyBindings": [
        {
            "before": [
                "j",
                "j"
            ],
            "after": [
                "<Esc>"
            ]
        }
    ],
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "<leader>",
                "d"
            ],
            "after": [
                "d",
                "d"
            ]
        },
        {
            "before": [
                "<C-n>"
            ],
            "commands": [
                ":nohl"
            ]
        },
        {
            "before": [
                "K"
            ],
            "commands": [
                "lineBreakInsert"
            ],
            "silent": true
        },
        {
            "before": [
                "<BS>"
            ],
            "after": [
                "-"
            ]
        }
    ],
    "vim.leader": "<space>",
    "vim.handleKeys": {
        "<C-a>": false,
        "<C-f>": false,
        "<C-c>": false,
        "<C-y>": false,
        "<C-x>": false,
    },
    "extensions.experimental.affinity": {
        "vscodevim.vim": 1
    },
    "go.formatTool": "gofmt",
    "[go]": {
        "editor.insertSpaces": true,
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": "explicit"
        },
        "editor.suggest.snippetsPreventQuickSuggestions": false
    },
    "animations.Install-Method": "Custom CSS and JS",
    // "apc.imports": [
    //     "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.3/dist/updateHandler.js"
    // ],
    "animations.CursorAnimationOptions": {
        "Color": "#ffb6c1",
        "TrailLength": 8
    },
    "vscode_custom_css.imports": [
        "file:///C:/Users/zhang/.vscode//extensions/jithurjacob.nbpreviewer-1.2.2/static/custom.css",
        "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.4/dist/updateHandler.js"
    ],
    "backgroundCover.imagePath": "e:\\Desktop\\图集\\black_image.png",
    "backgroundCover.opacity": 0.8,
    "backgroundCover.randomImageFolder": "e:\\Desktop\\图集",
    "animations.CursorAnimation": true,
    "animations.Command-Palette": "Slide",
    "animations.Auto-Install": true,
    "update.enableWindowsBackgroundUpdates": false,
    "update.mode": "manual"
}
```



# 2024.11.12 设置



```json
{
  "editor.fontSize": 16,
  "cph.general.autoShowJudge": false,
  "editor.formatOnSave": true,
  "editor.formatOnType": true,
  "files.autoSave": "afterDelay",
  "git.confirmSync": false,
  "chat.editor.fontSize": 18,
  "window.zoomLevel": 1,
  "editor.mouseWheelZoom": true,
  "editor.wordWrap": "on",
  "debug.onTaskErrors": "debugAnyway",
  "explorer.confirmDelete": false,
  "extensions.experimental.affinity": {
    "asvetliakov.vscode-neovim": 1
  },
  "workbench.settings.applyToAllProfiles": [
    "editor.fontSize"
  ],
  "go.delveConfig": {},
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[markdown]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[prisma]": {
    "editor.defaultFormatter": "Prisma.prisma"
  },
  "[typescript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.codeActionsOnSave": {
    "source.addMissingImports": "explicit",
    "source.organizeImports": "explicit"
  },
  "editor.cursorSmoothCaretAnimation": "on",
  "editor.cursorSurroundingLines": 5,
  "editor.fontFamily": "CaskaydiaCove Nerd Font",
  "editor.fontLigatures": true,
  "python.analysis.completeFunctionParens": true,
  "editor.fontSize": 18,
  "editor.fontWeight": "300",
  "editor.formatOnSave": true,
  "editor.inlineSuggest.enabled": true,
  "editor.lineNumbers": "relative",
  "editor.linkedEditing": true,
  "editor.smoothScrolling": true,
  "editor.stickyScroll.enabled": true,
  "editor.suggest.insertMode": "replace",
  "editor.suggestFontSize": 14,
  "editor.wordWrap": "on",
  "errorLens.fontStyleItalic": true,
  "everforest.italicKeywords": true,
  "explorer.confirmDelete": false,
  "explorer.confirmDragAndDrop": false,
  "extensions.autoUpdate": "onlyEnabledExtensions",
  "extensions.ignoreRecommendations": false,
  "files.exclude": {
    "**/node_modules": true
  },
  "prettier.semi": false,
  "prettier.singleAttributePerLine": true,
  "prettier.singleQuote": true,
  "prettier.trailingComma": "all",
  "projectManager.git.baseFolders": [
    "$home/workspace"
  ],
  "projectManager.sortList": "Recent",
  "sortJSON.orderOverride": [
    "name",
    "version",
    "main",
    "module",
    "types",
    "typings",
    "files",
    "publishConfig",
    "repository",
    "scripts",
    "prefix",
    "description",
    "body"
  ],
  "sortJSON.orderUnderride": [
    "resolutions",
    "dependencies",
    "devDependencies",
    "peerDependencies",
    "cSpell.userWords"
  ],
  "typescript.preferences.importModuleSpecifier": "relative",
  "typescript.updateImportsOnFileMove.enabled": "always",
  "update.showReleaseNotes": false,
  "vim.foldfix": true,
  "vim.highlightedyank.color": "rgba(230, 97, 89, 0.7)",
  "vim.highlightedyank.enable": true,
  "vim.highlightedyank.textColor": "white",
  "vim.hlsearch": true,
  "vim.leader": "<space>",
  "vim.normalModeKeyBindingsNonRecursive": [
    {
      "before": [
        "leader",
        "r"
      ],
      "commands": [
        "editor.action.rename"
      ]
    },
    {
      "before": [
        "leader",
        "w"
      ],
      "commands": [
        ":w!"
      ]
    },
    {
      "before": [
        "leader",
        "q"
      ],
      "commands": [
        ":q!"
      ]
    },
    {
      "before": [
        "leader",
        "x"
      ],
      "commands": [
        ":x!"
      ]
    },
    {
      "after": [
        "g",
        "g",
        "V",
        "G"
      ],
      "before": [
        "<c-a>"
      ]
    },
    {
      "before": [
        "<leader>",
        "k"
      ],
      "commands": [
        "editor.action.showHover"
      ]
    },
    {
      "before": [
        "[",
        "d"
      ],
      "commands": [
        "editor.action.marker.prev"
      ]
    },
    {
      "before": [
        "]",
        "d"
      ],
      "commands": [
        "editor.action.marker.next"
      ]
    },
    {
      "before": [
        "<leader>",
        "c",
        "a"
      ],
      "commands": [
        "editor.action.quickFix"
      ]
    },
    {
      "after": [
        "^"
      ],
      "before": [
        "H"
      ]
    },
    {
      "after": [
        "$"
      ],
      "before": [
        "L"
      ]
    },
    {
      "before": [
        "leader",
        "i"
      ],
      "commands": [
        "extension.toggleBool"
      ]
    }
  ],
  "vim.useSystemClipboard": true,
  "window.zoomLevel": 1,
  "workbench.iconTheme": "Monokai Pro Icons",
  "workbench.settings.editor": "json",
  "workbench.startupEditor": "readme",
  "zenMode.hideLineNumbers": false,
  "vsicons.dontShowNewVersionMessage": true,
  "[jsonc]": {
    "editor.quickSuggestions": {
      "strings": true
    },
    "editor.suggest.insertMode": "replace"
  },
  "terminal.integrated.defaultProfile.windows": "Command Prompt",
  "terminal.explorerKind": "external",
  "security.workspace.trust.enabled": false,
  "typescript.disableAutomaticTypeAcquisition": true,
  "git.enableSmartCommit": true,
  "git.openRepositoryInParentFolders": "always",
  "files.autoGuessEncoding": true,
  "code-runner.languageIdToFileExtensionMap": {
    "bat": ".bat",
    "powershell": ".ps1",
    "typescript": ".ts"
  },
  "vim.easymotion": true,
  // "editor.formatOnType": true,
  // "editor.formatOnSave": true,
  "go.formatTool": "gofmt",
  "[go]": {
    "editor.insertSpaces": true,
    "editor.formatOnSave": true,
    "editor.codeActionsOnSave": {
      "source.organizeImports": "explicit"
    },
    "editor.suggest.snippetsPreventQuickSuggestions": false
  },
  "animations.Install-Method": "Custom CSS and JS",
  "apc.imports": [
    "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.3/dist/updateHandler.js"
  ],
  "animations.CursorAnimation": true,
  "animations.CursorAnimationOptions": {
    "Color": "#ffb6c1",
    "TrailLength": 8
  },
  "animations.Smooth-Mode": false,
  "marscode.codeCompletionPro": {
    "enableCodeCompletionPro": true
  },
  "marscode.enableCodelens": {
    "enableInlineUnitTest": false,
    "enableInlineDocumentation": false
  },
  "vscode_custom_css.imports": [
    "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.4/dist/updateHandler.js"
  ]
}
```





# 11月28日

```json
{
    "editor.fontSize": 16,
    "cph.general.autoShowJudge": false,
    "editor.formatOnSave": true,
    "editor.formatOnType": true,
    "files.autoSave": "afterDelay",
    "git.confirmSync": false,
    "chat.editor.fontSize": 18,
    "window.zoomLevel": 1,
    "editor.mouseWheelZoom": true,
    "editor.wordWrap": "on",
    "debug.onTaskErrors": "debugAnyway",
    "explorer.confirmDelete": false,
    "extensions.experimental.affinity": {
        "asvetliakov.vscode-neovim": 1
    },
    "workbench.settings.applyToAllProfiles": [
        "editor.fontSize"
    ],
    "go.delveConfig": {},
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[markdown]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[prisma]": {
        "editor.defaultFormatter": "Prisma.prisma"
    },
    "[typescript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[typescriptreact]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "editor.codeActionsOnSave": {
        "source.addMissingImports": "explicit",
        "source.organizeImports": "explicit"
    },
    "editor.cursorSmoothCaretAnimation": "on",
    "editor.cursorSurroundingLines": 5,
    "editor.fontFamily": "CaskaydiaCove Nerd Font",
    "editor.fontLigatures": true,
    "python.analysis.completeFunctionParens": true,
    "editor.fontSize": 18,
    "editor.fontWeight": "300",
    "editor.formatOnSave": true,
    "editor.inlineSuggest.enabled": true,
    "editor.lineNumbers": "relative",
    "editor.linkedEditing": true,
    "editor.smoothScrolling": true,
    "editor.stickyScroll.enabled": true,
    "editor.suggest.insertMode": "replace",
    "editor.suggestFontSize": 14,
    "editor.wordWrap": "on",
    "errorLens.fontStyleItalic": true,
    "everforest.italicKeywords": true,
    "explorer.confirmDelete": false,
    "explorer.confirmDragAndDrop": false,
    "extensions.autoUpdate": "onlyEnabledExtensions",
    "extensions.ignoreRecommendations": false,
    "files.exclude": {
        "**/node_modules": true
    },
    "prettier.semi": false,
    "prettier.singleAttributePerLine": true,
    "prettier.singleQuote": true,
    "prettier.trailingComma": "all",
    "projectManager.git.baseFolders": [
        "$home/workspace"
    ],
    "projectManager.sortList": "Recent",
    "sortJSON.orderOverride": [
        "name",
        "version",
        "main",
        "module",
        "types",
        "typings",
        "files",
        "publishConfig",
        "repository",
        "scripts",
        "prefix",
        "description",
        "body"
    ],
    "sortJSON.orderUnderride": [
        "resolutions",
        "dependencies",
        "devDependencies",
        "peerDependencies",
        "cSpell.userWords"
    ],
    "typescript.preferences.importModuleSpecifier": "relative",
    "typescript.updateImportsOnFileMove.enabled": "always",
    "update.showReleaseNotes": false,
    "vim.foldfix": true,
    "vim.highlightedyank.color": "rgba(230, 97, 89, 0.7)",
    "vim.highlightedyank.enable": true,
    "vim.highlightedyank.textColor": "white",
    "vim.hlsearch": true,
    "vim.leader": "<space>",
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "leader",
                "r"
            ],
            "commands": [
                "editor.action.rename"
            ]
        },
        {
            "before": [
                "leader",
                "w"
            ],
            "commands": [
                ":w!"
            ]
        },
        {
            "before": [
                "leader",
                "q"
            ],
            "commands": [
                ":q!"
            ]
        },
        {
            "before": [
                "leader",
                "x"
            ],
            "commands": [
                ":x!"
            ]
        },
        {
            "after": [
                "g",
                "g",
                "V",
                "G"
            ],
            "before": [
                "<c-a>"
            ]
        },
        {
            "before": [
                "<leader>",
                "k"
            ],
            "commands": [
                "editor.action.showHover"
            ]
        },
        {
            "before": [
                "[",
                "d"
            ],
            "commands": [
                "editor.action.marker.prev"
            ]
        },
        {
            "before": [
                "]",
                "d"
            ],
            "commands": [
                "editor.action.marker.next"
            ]
        },
        {
            "before": [
                "<leader>",
                "c",
                "a"
            ],
            "commands": [
                "editor.action.quickFix"
            ]
        },
        {
            "after": [
                "^"
            ],
            "before": [
                "H"
            ]
        },
        {
            "after": [
                "$"
            ],
            "before": [
                "L"
            ]
        },
        {
            "before": [
                "leader",
                "i"
            ],
            "commands": [
                "extension.toggleBool"
            ]
        }
    ],
    "vim.useSystemClipboard": true,
    "window.zoomLevel": 1,
    "workbench.iconTheme": "Monokai Pro Icons",
    "workbench.settings.editor": "json",
    "workbench.startupEditor": "readme",
    "zenMode.hideLineNumbers": false,
    "vsicons.dontShowNewVersionMessage": true,
    "[jsonc]": {
        "editor.quickSuggestions": {
            "strings": true
        },
        "editor.suggest.insertMode": "replace"
    },
    "terminal.integrated.defaultProfile.windows": "Command Prompt",
    "terminal.explorerKind": "external",
    "security.workspace.trust.enabled": false,
    "typescript.disableAutomaticTypeAcquisition": true,
    "git.enableSmartCommit": true,
    "git.openRepositoryInParentFolders": "always",
    "files.autoGuessEncoding": true,
    "code-runner.languageIdToFileExtensionMap": {
        "bat": ".bat",
        "powershell": ".ps1",
        "typescript": ".ts"
    },
    "vim.easymotion": true,
    "vim.easymotion": true,
    "vim.incsearch": true,
    "vim.useSystemClipboard": true,
    "vim.useCtrlKeys": true,
    "vim.hlsearch": true,
    "vim.insertModeKeyBindings": [
        {
            "before": [
                "j",
                "j"
            ],
            "after": [
                "<Esc>"
            ]
        }
    ],
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "<leader>",
                "d"
            ],
            "after": [
                "d",
                "d"
            ]
        },
        {
            "before": [
                "<C-n>"
            ],
            "commands": [
                ":nohl"
            ]
        },
        {
            "before": [
                "K"
            ],
            "commands": [
                "lineBreakInsert"
            ],
            "silent": true
        }
    ],
    "vim.leader": "<space>",
    "vim.handleKeys": {
        "<C-a>": false,
        "<C-f>": false,
        "<C-c>": false,
        "<C-y>": false,
    },
    "extensions.experimental.affinity": {
        "vscodevim.vim": 1
    },
    "go.formatTool": "gofmt",
    "[go]": {
        "editor.insertSpaces": true,
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": "explicit"
        },
        "editor.suggest.snippetsPreventQuickSuggestions": false
    },
    "animations.Install-Method": "Custom CSS and JS",
    "apc.imports": [
        "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.3/dist/updateHandler.js"
    ],
    "animations.CursorAnimation": true,
    "animations.CursorAnimationOptions": {
        "Color": "#ffb6c1",
        "TrailLength": 8
    },
    "animations.Smooth-Mode": false,
    "marscode.codeCompletionPro": {
        "enableCodeCompletionPro": true
    },
    "marscode.enableCodelens": {
        "enableInlineUnitTest": false,
        "enableInlineDocumentation": false
    },
    "vscode_custom_css.imports": [
        "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.4/dist/updateHandler.js"
    ],
    "database-client.autoSync": true
}
```



# vscode 字体 : CaskaydiaCove Nerd Font 



# 24 . 12 .07 

```json
{
    "editor.fontSize": 16,
    "cph.general.autoShowJudge": false,
    "editor.formatOnSave": true,
    "editor.formatOnType": true,
    "files.autoSave": "afterDelay",
    "git.confirmSync": false,
    "chat.editor.fontSize": 18,
    "window.zoomLevel": 1,
    "editor.mouseWheelZoom": true,
    "editor.wordWrap": "on",
    "debug.onTaskErrors": "debugAnyway",
    "explorer.confirmDelete": false,
    "extensions.experimental.affinity": {
        "asvetliakov.vscode-neovim": 1
    },
    "workbench.settings.applyToAllProfiles": [
        "editor.fontSize"
    ],
    "go.delveConfig": {},
    "[javascript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[markdown]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[prisma]": {
        "editor.defaultFormatter": "Prisma.prisma"
    },
    "[typescript]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[typescriptreact]": {
        "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "editor.codeActionsOnSave": {
        "source.addMissingImports": "explicit",
        "source.organizeImports": "explicit"
    },
    "editor.cursorSmoothCaretAnimation": "on",
    "editor.cursorSurroundingLines": 5,
    "editor.fontFamily": "CaskaydiaCove Nerd Font ",
    "editor.fontLigatures": true,
    "python.analysis.completeFunctionParens": true,
    "editor.fontSize": 18,
    "editor.fontWeight": "300",
    "editor.formatOnSave": true,
    "editor.inlineSuggest.enabled": true,
    "editor.lineNumbers": "relative",
    "editor.linkedEditing": true,
    "editor.smoothScrolling": true,
    "editor.stickyScroll.enabled": true,
    "editor.suggest.insertMode": "replace",
    "editor.suggestFontSize": 14,
    "editor.wordWrap": "on",
    "errorLens.fontStyleItalic": true,
    "everforest.italicKeywords": true,
    "explorer.confirmDelete": false,
    "explorer.confirmDragAndDrop": false,
    "extensions.autoUpdate": "onlyEnabledExtensions",
    "extensions.ignoreRecommendations": false,
    "files.exclude": {
        "**/node_modules": true
    },
    "prettier.semi": false,
    "prettier.singleAttributePerLine": true,
    "prettier.singleQuote": true,
    "prettier.trailingComma": "all",
    "projectManager.git.baseFolders": [
        "$home/workspace"
    ],
    "projectManager.sortList": "Recent",
    "sortJSON.orderOverride": [
        "name",
        "version",
        "main",
        "module",
        "types",
        "typings",
        "files",
        "publishConfig",
        "repository",
        "scripts",
        "prefix",
        "description",
        "body"
    ],
    "sortJSON.orderUnderride": [
        "resolutions",
        "dependencies",
        "devDependencies",
        "peerDependencies",
        "cSpell.userWords"
    ],
    "typescript.preferences.importModuleSpecifier": "relative",
    "typescript.updateImportsOnFileMove.enabled": "always",
    "update.showReleaseNotes": false,
    "vim.foldfix": true,
    "vim.highlightedyank.color": "rgba(230, 97, 89, 0.7)",
    "vim.highlightedyank.enable": true,
    "vim.highlightedyank.textColor": "white",
    "vim.hlsearch": true,
    "vim.leader": "<space>",
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "leader",
                "r"
            ],
            "commands": [
                "editor.action.rename"
            ]
        },
        {
            "before": [
                "leader",
                "w"
            ],
            "commands": [
                ":w!"
            ]
        },
        {
            "before": [
                "leader",
                "q"
            ],
            "commands": [
                ":q!"
            ]
        },
        {
            "before": [
                "leader",
                "x"
            ],
            "commands": [
                ":x!"
            ]
        },
        {
            "after": [
                "g",
                "g",
                "V",
                "G"
            ],
            "before": [
                "<c-a>"
            ]
        },
        {
            "before": [
                "<leader>",
                "k"
            ],
            "commands": [
                "editor.action.showHover"
            ]
        },
        {
            "before": [
                "[",
                "d"
            ],
            "commands": [
                "editor.action.marker.prev"
            ]
        },
        {
            "before": [
                "]",
                "d"
            ],
            "commands": [
                "editor.action.marker.next"
            ]
        },
        {
            "before": [
                "<leader>",
                "c",
                "a"
            ],
            "commands": [
                "editor.action.quickFix"
            ]
        },
        {
            "after": [
                "^"
            ],
            "before": [
                "H"
            ]
        },
        {
            "after": [
                "$"
            ],
            "before": [
                "L"
            ]
        },
        {
            "before": [
                "leader",
                "i"
            ],
            "commands": [
                "extension.toggleBool"
            ]
        }
    ],
    "vim.useSystemClipboard": true,
    "window.zoomLevel": 1,
    "workbench.iconTheme": "Monokai Pro Icons",
    "workbench.settings.editor": "json",
    "workbench.startupEditor": "readme",
    "zenMode.hideLineNumbers": false,
    "vsicons.dontShowNewVersionMessage": true,
    "[jsonc]": {
        "editor.quickSuggestions": {
            "strings": true
        },
        "editor.suggest.insertMode": "replace"
    },
    "terminal.integrated.defaultProfile.windows": "Command Prompt",
    "terminal.explorerKind": "external",
    "security.workspace.trust.enabled": false,
    "typescript.disableAutomaticTypeAcquisition": true,
    "git.enableSmartCommit": true,
    "git.openRepositoryInParentFolders": "always",
    "files.autoGuessEncoding": true,
    "code-runner.languageIdToFileExtensionMap": {
        "bat": ".bat",
        "powershell": ".ps1",
        "typescript": ".ts"
    },
    "vim.easymotion": true,
    "vim.easymotion": true,
    "vim.incsearch": true,
    "vim.useSystemClipboard": true,
    "vim.useCtrlKeys": true,
    "vim.hlsearch": true,
    "vim.insertModeKeyBindings": [
        {
            "before": [
                "j",
                "j"
            ],
            "after": [
                "<Esc>"
            ]
        }
    ],
    "vim.normalModeKeyBindingsNonRecursive": [
        {
            "before": [
                "<leader>",
                "d"
            ],
            "after": [
                "d",
                "d"
            ]
        },
        {
            "before": [
                "<C-n>"
            ],
            "commands": [
                ":nohl"
            ]
        },
        {
            "before": [
                "K"
            ],
            "commands": [
                "lineBreakInsert"
            ],
            "silent": true
        },
        {
            "before": [
                "<BS>"
            ],
            "after": [
                "-"
            ]
        }
    ],
    "vim.leader": "<space>",
    "vim.handleKeys": {
        "<C-a>": false,
        "<C-f>": false,
        "<C-c>": false,
        "<C-y>": false,
        "<C-x>": false,
    },
    "extensions.experimental.affinity": {
        "vscodevim.vim": 1
    },
    "go.formatTool": "gofmt",
    "[go]": {
        "editor.insertSpaces": true,
        "editor.formatOnSave": true,
        "editor.codeActionsOnSave": {
            "source.organizeImports": "explicit"
        },
        "editor.suggest.snippetsPreventQuickSuggestions": false
    },
    "animations.Install-Method": "Custom CSS and JS",
    "apc.imports": [
        "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.3/dist/updateHandler.js"
    ],
    "animations.CursorAnimation": true,
    "animations.CursorAnimationOptions": {
        "Color": "#ffb6c1",
        "TrailLength": 8
    },
    "animations.Smooth-Mode": false,
    "marscode.codeCompletionPro": {
        "enableCodeCompletionPro": true
    },
    "marscode.enableCodelens": {
        "enableInlineUnitTest": false,
        "enableInlineDocumentation": false
    },
    "vscode_custom_css.imports": [
        "file:///c:/Users/zhang/.vscode/extensions/brandonkirbyson.vscode-animations-2.0.4/dist/updateHandler.js"
    ],
    "database-client.autoSync": true,
    "background.editor": {
        "useFront": true,
        "style": {
            "background-position": "100% 100%",
            "background-size": "auto",
            "opacity": 0.6
        },
        "styles": [
            {},
            {},
            {}
        ],
        "images": [],
        "interval": 0,
        "random": false
    },
    "backgroundCover.imagePath": "e:\\Desktop\\图集\\black_image.png",
    "backgroundCover.opacity": 0.8,
    "backgroundCover.randomImageFolder": "e:\\Desktop\\图集"
}
```

