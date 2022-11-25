alphabetical_sorter:
	${INFO} "Alphabetical Sorter"
	@echo 'Multi line or single line alphabetical sorter.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=ue.alphabetical-sorter"
	${INSTALL} "vscode:extension/ue.alphabetical-sorter"

auto_close_tag:
	${INFO} "Auto Close Tag"
	@echo 'Automatically add HTML/XML close tag, same as Visual Studio IDE or Sublime Text'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag"
	${INSTALL} "vscode:extension/formulahendry.auto-close-tag"

auto_rename_tag:
	${INFO} "Auto Rename Tag"
	@echo 'Automatically rename paired HTML/XML tag, same as Visual Studio IDE does.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=formulahendry.auto-rename-tag"
	${INSTALL} "vscode:extension/formulahendry.auto-rename-tag"

code_spell_checker:
	${INFO} "Code Spell Checker"
	@echo 'A basic spell checker that works well with camelCase code.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker"
	${INSTALL} "vscode:extension/streetsidesoftware.code-spell-checker"

change_case:
	${INFO} "change-case"
	@echo 'Quickly change the case (camelCase, CONSTANT_CASE, snake_case, etc) of the current selection or current word'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=wmaurer.change-case"
	${INSTALL} "vscode:extension/wmaurer.change-case"

highlight_whitespace:
	${INFO} "Highlight Trailing White Spaces"
	@echo 'This extension highlight trailing white spaces in red'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=ybaumes.highlight-trailing-white-spaces"
	${INSTALL} "vscode:extension/ybaumes.highlight-trailing-white-spaces"

markdownlint:
	${INFO} "markdownlint"
	@echo 'Markdown linting and style checking for Visual Studio Code'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint"
	${INSTALL} "vscode:extension/DavidAnson.vscode-markdownlint"

trailing_spaces:
	${INFO} "Trailing Spaces"
	@echo 'Highlight trailing spaces and delete them in a flash!'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces"
	${INSTALL} "vscode:extension/shardulm94.trailing-spaces"

vscode_proto3:
	${INFO} "vscode-proto3"
	@echo 'Protobuf 3 support for Visual Studio Code'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=zxh404.vscode-proto3"
	${INSTALL} "vscode:extension/zxh404.vscode-proto3"

# COLORS # https://linux.101hacks.com/ps1-examples/prompt-color-using-tput/
BLACK  := $(shell tput -Txterm setaf 0)
RED  := $(shell tput -Txterm setaf 1)
GREEN  := $(shell tput -Txterm setaf 2)
YELLOW := $(shell tput -Txterm setaf 3)
BLUE  := $(shell tput -Txterm setaf 4)
MEGENTA  := $(shell tput -Txterm setaf 5)
CYAN  := $(shell tput -Txterm setaf 6)
WHITE  := $(shell tput -Txterm setaf 7)
NC := "\e[0m"
RESET  := $(shell tput -Txterm sgr0)
# Shell Functions
INFO := @bash -c 'printf "\n"; printf $(GREEN); echo "=== $$1 ==="; printf "\n"; printf $(NC)' SOME_VALUE
INSTALL := @python -m webbrowser -t $$1
# INSTALL2 := ${LINK} https://marketplace.visualstudio.com/items?itemName= $$1 && @python -m webbrowser -t vscode:extension/$$1
LINK := @bash -c 'printf "\n"; printf $(BLUE); echo "$$1"; printf "\n"; printf $(NC)' SOME_VALUE
SUCCESS := @bash -c 'printf "\n"; printf $(GREEN); echo "===> $$1"; printf "\n"; printf $(NC)' SOME_VALUE
