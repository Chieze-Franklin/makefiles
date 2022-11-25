jest:
	${INFO} "Jest"
	@echo 'Supports full jest features in vscode environment'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest"
	${INSTALL} "vscode:extension/Orta.vscode-jest"

jest_runner:
	${INFO} "Jest Runner"
	@echo 'Simple way to run or debug a single (or multiple) tests from context-menu'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=firsttris.vscode-jest-runner"
	${INSTALL} "vscode:extension/firsttris.vscode-jest-runner"

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
