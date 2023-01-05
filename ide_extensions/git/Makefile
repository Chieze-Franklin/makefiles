all:
	${INFO} "Install All"
	@echo 'Install all extensions in this pack'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=fchieze.xpack-git"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=fchieze.xpack-git"
	# ${INSTALL} "vscode:extension/fchieze.xpack-git"


git_blame:
	${INFO} "Git Blame"
	@echo 'See git blame information in the status bar.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=waderyan.gitblame"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=waderyan.gitblame"
	# ${INSTALL} "vscode:extension/waderyan.gitblame"

git_history:
	${INFO} "Git History"
	@echo 'View git log, file history, compare branches or commits'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory"
	# ${INSTALL} "vscode:extension/donjayamanne.githistory"

git_lens:
	${INFO} "Git Lens"
	@echo 'GitLens supercharges Git inside VS Code and unlocks untapped knowledge within each repository.'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens"
	${INSTALL} "https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens"
	# ${INSTALL} "vscode:extension/eamodio.gitlens"

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
