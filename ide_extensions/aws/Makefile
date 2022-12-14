aws_toolkit:
	${INFO} "AWS Toolkit"
	@echo 'Amazon Web Services toolkit for browsing and updating cloud resources'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.aws-toolkit-vscode"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=AmazonWebServices.aws-toolkit-vscode"
	# ${INSTALL} "vscode:extension/AmazonWebServices.aws-toolkit-vscode"

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
