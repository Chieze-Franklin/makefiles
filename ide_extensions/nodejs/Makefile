# https://github.com/andela/engineering-playbook/tree/master/4.%20Laptop%20Setup # Regex Preview and Editor

eslint:
	${INFO} "ESLint"
	@echo 'Integrates ESLint JavaScript into VS Code.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint"
	${INSTALL} "vscode:extension/dbaeumer.vscode-eslint"
import_cost:
	${INFO} "Import Cost"
	@echo 'Display import/require package size in the editor'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost"
	${INSTALL} "vscode:extension/wix.vscode-import-cost"

modules_intellisense:
	${INFO} "Node.js Modules Intellisense"
	@echo 'Autocompletes Node.js modules in import statements'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=leizongmin.node-module-intellisense"
	${INSTALL} "vscode:extension/leizongmin.node-module-intellisense"

path_intellisense:
	${INFO} "Path Intellisense"
	@echo 'Visual Studio Code plugin that autocompletes filenames'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense"
	${INSTALL} "vscode:extension/christian-kohler.path-intellisense"

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
