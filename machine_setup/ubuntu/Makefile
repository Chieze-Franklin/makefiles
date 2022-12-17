git:
	${INFO} "Install Git"
	@echo 'Install Git commands'
	${LINK} "https://git-scm.com/"
	${INSTALL} "git-all"

docker_0:
	${INFO} "Uninstall Old Docker"
	@echo 'Remove old Docker version'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${UNINSTALL} "docker docker-engine docker.io containerd runc"

docker_1:
	${INFO} "Setup Docker"
	@echo 'Set up Docker repository'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${INSTALL} "ca-certificates curl gnupg lsb-release"
	sudo mkdir -p /etc/apt/keyrings
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
	@echo 'deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable' | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

docker_2:
	${INFO} "Install Docker"
	@echo 'Install Docker engine'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${INSTALL} "docker-ce docker-ce-cli containerd.io docker-compose-plugin"

docker_compose:
	${INFO} "Install docker-compose"
	@echo 'Install docker-compose (as a separate tool from Docker)'
	${LINK} "https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04"
	sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
	sudo chmod +x /usr/local/bin/docker-compose

nvm:
	${INFO} "Install nvm"
	@echo 'Install Node Version Manager'
	${LINK} "https://github.com/nvm-sh/nvm"
	curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
	export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")" [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm

xclip:
	${INFO} "Install XClip"
	@echo 'Install XClip in order for VS Code extension, CodeSnap, to work'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=adpyke.codesnap"
	sudo apt install xclip

snap_docker:
	${INFO} "Install Docker"
	@echo 'Install Docker using Snap'
	${LINK} "https://snapcraft.io/docker"
	${SNAP} "docker"

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
