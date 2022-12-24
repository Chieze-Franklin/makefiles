# SHELL=/bin/bash

default: git.x nvm.x yarn.x snap_vscode.x xclip.x snap_slack.x snap_docker.x root_docker.x docker_compose.x enable_startup_docker psql.x snap_dbeaver.x

clean:
	@rm -f $(wildcard *.x)

enable_startup_docker:
	${INFO} "Enable Startup for Docker"
	@echo 'Start Docker when machine boots'
	${LINK} "https://docs.docker.com/engine/install/linux-postinstall/#configure-docker-to-start-on-boot-with-systemd"
	sudo systemctl enable docker.service
	sudo systemctl enable containerd.service

disable_startup_docker:
	${INFO} "Disable Startup for Docker"
	@echo 'Do not start Docker when machine boots'
	${LINK} "https://docs.docker.com/engine/install/linux-postinstall/#configure-docker-to-start-on-boot-with-systemd"
	sudo systemctl disable docker.service
	sudo systemctl disable containerd.service

git.x:
	${INFO} "Install Git"
	@echo 'Install Git commands'
	${LINK} "https://git-scm.com/"
	${INSTALL} "git-all"
	git config --global alias.br branch
	git config --global alias.ch checkout
	git config --global alias.cm "commit -m"
	git config --global alias.st status
	${SUCCESS} $@

docker.x: docker_0.x docker_1.x docker_2.x

docker_0.x:
	${INFO} "Uninstall Old Docker"
	@echo 'Remove old Docker version'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${UNINSTALL} "docker docker-engine docker.io containerd runc"
	${SUCCESS} $@

docker_1.x: docker_0.x
	${INFO} "Setup Docker"
	@echo 'Set up Docker repository'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${INSTALL} "ca-certificates curl gnupg lsb-release"
	sudo mkdir -p /etc/apt/keyrings
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
	@echo 'deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable' | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
	${SUCCESS} $@

docker_2.x: docker_1.x
	${INFO} "Install Docker"
	@echo 'Install Docker engine'
	${LINK} "https://docs.docker.com/engine/install/ubuntu"
	${INSTALL} "docker-ce docker-ce-cli containerd.io docker-compose-plugin"
	${SUCCESS} $@

docker_compose.x:
	${INFO} "Install docker-compose"
	@echo 'Install docker-compose (as a separate tool from Docker)'
	${LINK} "https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-compose-on-ubuntu-20-04"
	sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
	sudo chmod +x /usr/local/bin/docker-compose
	${SUCCESS} $@

nvm.x:
	${INFO} "Install nvm"
	@echo 'Install Node Version Manager'
	${LINK} "https://github.com/nvm-sh/nvm"
	curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.2/install.sh | bash
	export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")" [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
	${SUCCESS} $@

psql.x:
	${INFO} "Install PSQL"
	@echo 'Install PSQL (Postgres Client)'
	${LINK} "https://www.postgresql.org/docs/current/app-psql.html"
	# sudo apt install postgresql-client-common
	${INSTALL} "postgresql-client-common"
	${INSTALL} "postgresql-client"
	${SUCCESS} $@

root_docker.x:
	${INFO} "Root Docker"
	@echo 'Run Docker as root user (without sudo)'
	${LINK} "https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user"
	sudo groupadd docker
	sudo usermod -aG docker $USER
	newgrp docker
	${SUCCESS} $@

snap_dbeaver.x:
	${INFO} "Install DBeaver"
	@echo 'Install DBeaver using Snap'
	${LINK} "https://snapcraft.io/dbeaver-ce"
	${SNAP} "dbeaver-ce"
	${SUCCESS} $@

snap_docker.x:
	${INFO} "Install Docker"
	@echo 'Install Docker using Snap'
	${LINK} "https://snapcraft.io/docker"
	${SNAP} "docker"
	${SUCCESS} $@

snap_slack.x:
	${INFO} "Install Slack"
	@echo 'Install Slack using Snap'
	${LINK} "hhttps://snapcraft.io/slack"
	${SNAP} "slack"
	${SUCCESS} $@

snap_vscode.x:
	${INFO} "Install VS Code"
	@echo 'Install VS Code using Snap'
	${LINK} "https://snapcraft.io/code"
	${SNAP} "code --classic"
	${SUCCESS} $@

xclip.x:
	${INFO} "Install XClip"
	@echo 'Install XClip in order for VS Code extension, CodeSnap, to work'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=adpyke.codesnap"
	sudo apt install xclip
	${SUCCESS} $@

yarn.x:
	${INFO} "Install Yarn"
	@echo 'Install Yarn'
	${LINK} "https://yarnpkg.com/getting-started/install"
	@NODE_VER="$$(echo $$(node -v) | cut -c 2-3)"; NODE_VER_16="16"; echo $$NODE_VER; if [ $$NODE_VER -lt $$NODE_VER_16 ]; then npm i -g corepack; fi
	corepack enable
	corepack prepare yarn@stable --activate
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
SNAP := @bash -c 'sudo snap install $$1' SOME_VALUE
# INSTALL2 := ${LINK} https://marketplace.visualstudio.com/items?itemName= $$1 && @python -m webbrowser -t vscode:extension/$$1
UNINSTALL := @bash -c 'sudo apt-get remove $$1' SOME_VALUE
LINK := @bash -c 'printf "\n"; printf $(BLUE); echo "$$1"; printf "\n"; printf $(NC)' SOME_VALUE
SUCCESS := @bash -c 'printf "\n"; printf $(GREEN); echo "===> $$1"; printf "\n"; printf $(NC); echo "===> successfully run $$1" > $$1' SOME_VALUE
