alphabetical_sorter:
	${INFO} "Alphabetical Sorter"
	@echo 'Multi line or single line alphabetical sorter.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=ue.alphabetical-sorter"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=ue.alphabetical-sorter"
	# ${INSTALL} "vscode:extension/ue.alphabetical-sorter"

code_spell_checker:
	${INFO} "Code Spell Checker"
	@echo 'A basic spell checker that works well with camelCase code.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker"
	# ${INSTALL} "vscode:extension/streetsidesoftware.code-spell-checker"

change_case:
	${INFO} "change-case"
	@echo 'Quickly change the case (camelCase, CONSTANT_CASE, snake_case, etc) of the current selection or current word'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=wmaurer.change-case"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=wmaurer.change-case"
	# ${INSTALL} "vscode:extension/wmaurer.change-case"

highlight_whitespace:
	${INFO} "Highlight Trailing White Spaces"
	@echo 'This extension highlight trailing white spaces in red'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=ybaumes.highlight-trailing-white-spaces"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=ybaumes.highlight-trailing-white-spaces"
	# ${INSTALL} "vscode:extension/ybaumes.highlight-trailing-white-spaces"

makefile:
	${INFO} "Makefile Tools"
	@echo 'Provide makefile support in VS Code: C/C++ IntelliSense, build, debug/run'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=ms-vscode.makefile-tools"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=ms-vscode.makefile-tools"
	# ${INSTALL} "vscode:extension/ms-vscode.makefile-tools"

prettier:
	${INFO} "Prettier - Code formatter"
	@echo 'Code formatter using prettier'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode"
	# ${INSTALL} "vscode:extension/esbenp.prettier-vscode"

thunder_client:
	${INFO} "Thunder Client"
	@echo 'Lightweight Rest API Client for VS Code'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=rangav.vscode-thunder-client"
	# ${INSTALL} "vscode:extension/rangav.vscode-thunder-client"

trailing_spaces:
	${INFO} "Trailing Spaces"
	@echo 'Highlight trailing spaces and delete them in a flash!'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces"
	# ${INSTALL} "vscode:extension/shardulm94.trailing-spaces"

vscode_proto3:
	${INFO} "vscode-proto3"
	@echo 'Protobuf 3 support for Visual Studio Code'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=zxh404.vscode-proto3"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=zxh404.vscode-proto3"
	# ${INSTALL} "vscode:extension/zxh404.vscode-proto3"

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
INSTALL := @python3 -m webbrowser -t $$1
# INSTALL2 := ${LINK} https://marketplace.visualstudio.com/items?itemName= $$1 && @python -m webbrowser -t vscode:extension/$$1
LINK := @bash -c 'printf "\n"; printf $(BLUE); echo "$$1"; printf "\n"; printf $(NC)' SOME_VALUE
SUCCESS := @bash -c 'printf "\n"; printf $(GREEN); echo "===> $$1"; printf "\n"; printf $(NC)' SOME_VALUE
