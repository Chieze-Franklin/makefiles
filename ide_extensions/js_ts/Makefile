all:
	${INFO} "Install All"
	@echo 'Install all extensions in this pack'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=fchieze.xpack-jsts"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=fchieze.xpack-jsts"
	# ${INSTALL} "vscode:extension/fchieze.xpack-jsts"

codemetrics:
	${INFO} "CodeMetrics"
	@echo 'Computes complexity in TypeScript / JavaScript files.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-codemetrics"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-codemetrics"
	# ${INSTALL} "vscode:extension/kisstkondoros.vscode-codemetrics"

eslint:
	${INFO} "ESLint"
	@echo 'Integrates ESLint JavaScript into VS Code.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint"
	# ${INSTALL} "vscode:extension/dbaeumer.vscode-eslint"

import_cost:
	${INFO} "Import Cost"
	@echo 'Display import/require package size in the editor'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost"
	# ${INSTALL} "vscode:extension/wix.vscode-import-cost"
	
jest:
	${INFO} "Jest"
	@echo 'Supports full jest features in vscode environment'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest"
	# ${INSTALL} "vscode:extension/Orta.vscode-jest"

jest_runner:
	${INFO} "Jest Runner"
	@echo 'Simple way to run or debug a single (or multiple) tests from context-menu'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=firsttris.vscode-jest-runner"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=firsttris.vscode-jest-runner"
	# ${INSTALL} "vscode:extension/firsttris.vscode-jest-runner"

modules_intellisense:
	${INFO} "Node.js Modules Intellisense"
	@echo 'Autocompletes Node.js modules in import statements'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=leizongmin.node-module-intellisense"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=leizongmin.node-module-intellisense"
	# ${INSTALL} "vscode:extension/leizongmin.node-module-intellisense"

path_intellisense:
	${INFO} "Path Intellisense"
	@echo 'Visual Studio Code plugin that autocompletes filenames'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense"
	# ${INSTALL} "vscode:extension/christian-kohler.path-intellisense"

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
