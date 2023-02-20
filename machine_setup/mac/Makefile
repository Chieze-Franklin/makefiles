# SHELL=/bin/bash

default: brew.x chrome.x dbeaver.x docker_desktop.x docker.x fig.x git_alias.x ngrok.x nvm.x postgres.x terraform.x lslack.x vscode.x yarn.x zoom.x

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
	${BREW} "--cask google-chrome"
	${SUCCESS} $@

dbeaver.x:
	${INFO} "Install DBeaver"
	@echo 'Install DBeaver using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/dbeaver-community"
	${BREW} "--cask dbeaver-community"
	${SUCCESS} $@

docker.x:
	${INFO} "Install Docker"
	@echo 'Install Docker using Homebrew'
	${LINK} "https://formulae.brew.sh/formula/docker"
	${BREW} docker
	${SUCCESS} $@

docker_desktop.x:
	${INFO} "Install Docker Desktop"
	@echo 'Install Docker Desktop using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/docker"
	${BREW} "--cask docker"
	${SUCCESS} $@

fig.x:
	${INFO} "Install Fig"
	@echo 'Install Fig using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/fig"
	${BREW} "--cask fig"
	${SUCCESS} $@

git_alias.x:
	${INFO} "Git Alias"
	@echo 'Set up Git Aliases'
	${LINK} "https://git-scm.com/book/en/v2/Git-Basics-Git-Aliases"
	git config --global alias.br branch
	git config --global alias.ch checkout
	git config --global alias.cm "commit -m"
	git config --global alias.st status
	${SUCCESS} $@

ngrok.x:
	${INFO} "Install ngrok"
	@echo 'Install ngrok using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/ngrok"
	${BREW} "--cask ngrok"
	${SUCCESS} $@

nvm.x:
	${INFO} "Install nvm"
	@echo 'Install Node Version Manager using Homebrew'
	${LINK} "https://formulae.brew.sh/formula/nvm"
	${BREW} nvm
	${SUCCESS} $@

postgres.x:
	${INFO} "Install PostgreSQL"
	@echo 'Install PostgreSQL via Homebrew'
	${LINK} "https://wiki.postgresql.org/wiki/Homebrew"
	${BREW} postgresql
	${SUCCESS} $@

terraform.x:
	${INFO} "Install Terraform"
	@echo 'Install Terraform using Homebrew'
	${LINK} "https://formulae.brew.sh/formula/terraform"
	${BREW} terraform
	${SUCCESS} $@

slack.x:
	${INFO} "Install Slack"
	@echo 'Install Slack using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/slack"
	${BREW} "--cask slack"
	${SUCCESS} $@

vscode.x:
	${INFO} "Install VS Code"
	@echo 'Install VS Code using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/visual-studio-code"
	${BREW} "--cask visual-studio-code"
	${SUCCESS} $@

yarn.x:
	${INFO} "Install Yarn"
	@echo 'Install Yarn using Homebrew'
	${LINK} "https://formulae.brew.sh/formula/yarn"
	${BREW} yarn
	${SUCCESS} $@

zoom.x:
	${INFO} "Install Zoom"
	@echo 'Install Zoom using Homebrew'
	${LINK} "https://formulae.brew.sh/cask/zoom"
	${BREW} "--cask zoom"
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
BREW := @bash -c 'brew install $$1' SOME_VALUE
UNINSTALL := @bash -c 'brew uninstall $$1' SOME_VALUE
LINK := @bash -c 'printf "\n"; printf $(BLUE); echo "$$1"; printf "\n"; printf $(NC)' SOME_VALUE
SUCCESS := @bash -c 'printf "\n"; printf $(GREEN); echo "===> $$1"; printf "\n"; printf $(NC); echo "===> successfully run $$1" > $$1' SOME_VALUE
