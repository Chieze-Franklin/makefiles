all:
	${INFO} "Install All"
	@echo 'Install all extensions in this pack'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=fchieze.xpack-container"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=fchieze.xpack-container"
	# ${INSTALL} "vscode:extension/fchieze.xpack-container"

docker:
	${INFO} "Docker"
	@echo 'Makes it easy to create, manage, and debug containerized applications'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-docker"
	# ${INSTALL} "vscode:extension/ms-azuretools.vscode-docker"

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
