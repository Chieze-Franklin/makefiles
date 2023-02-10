# SHELL=/bin/bash

default: brew.x chrome.x

clean:
	@rm -f $(wildcard *.x)

brew.x:
	${INFO} "Install Homebrew"
	@echo 'Install Homebrew'
	${LINK} "https://brew.sh"
	/bin/bash -c "$$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
	${SUCCESS} $@

chrome.x:
	${INFO} "Install Google Chrome"
	@echo 'Install Google Chrome using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/google-chrome"
	${BREW} google-chrome
	${SUCCESS} $@

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
INSTALL := @bash -c 'sudo apt-get update; sudo apt-get install $$1' SOME_VALUE
BREW := @bash -c 'brew install --cask $$1' SOME_VALUE
# INSTALL2 := ${LINK} https://marketplace.visualstudio.com/items?itemName= $$1 && @python -m webbrowser -t vscode:extension/$$1
UNINSTALL := @bash -c 'sudo apt-get remove $$1' SOME_VALUE
LINK := @bash -c 'printf "\n"; printf $(BLUE); echo "$$1"; printf "\n"; printf $(NC)' SOME_VALUE
SUCCESS := @bash -c 'printf "\n"; printf $(GREEN); echo "===> $$1"; printf "\n"; printf $(NC); echo "===> successfully run $$1" > $$1' SOME_VALUE
