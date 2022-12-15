install_git:
	${INFO} "Install Git"
	@echo 'Install Git commands'
	${LINK} "https://git-scm.com/"
	${INSTALL} "git-all"

install_docker_0:
	${INFO} "Uninstall Old Docker"
	@echo 'Remove old Docker version'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${UNINSTALL} "docker docker-engine docker.io containerd runc"

install_docker_1:
	${INFO} "Setup Docker"
	@echo 'Set up Docker repository'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${INSTALL} "ca-certificates curl gnupg lsb-release"
	sudo mkdir -p /etc/apt/keyrings
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
	@echo 'deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable' | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

install_docker_2:
	${INFO} "Install Docker"
	@echo 'Install Docker engine'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${INSTALL} "docker-ce docker-ce-cli containerd.io docker-compose-plugin"

snap_slack:
	${INFO} "Install Slack"
	@echo 'Install Slack using Snap'
	${LINK} "hhttps://snapcraft.io/slack"
	${SNAP} "slack"

snap_vscode:
	${INFO} "Install VS Code"
	@echo 'Install VS Code using Snap'
	${LINK} "https://snapcraft.io/code"
	${SNAP} "code --classic"
	
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
SNAP := @bash -c 'sudo snap install $$1' SOME_VALUE
# INSTALL2 := ${LINK} https://marketplace.visualstudio.com/items?itemName= $$1 && @python -m webbrowser -t vscode:extension/$$1
UNINSTALL := @bash -c 'sudo apt-get remove $$1' SOME_VALUE
LINK := @bash -c 'printf "\n"; printf $(BLUE); echo "$$1"; printf "\n"; printf $(NC)' SOME_VALUE
SUCCESS := @bash -c 'printf "\n"; printf $(GREEN); echo "===> $$1"; printf "\n"; printf $(NC)' SOME_VALUE
