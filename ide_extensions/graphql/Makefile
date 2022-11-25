graphql_inline_operation_execution:
	${INFO} "GraphQL: Inline Operation Execution"
	@echo 'Provides standalone support for executing graphql operations inline in your code'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=GraphQL.vscode-graphql-execution"
	${INSTALL} "vscode:extension/GraphQL.vscode-graphql-execution"

graphql_languagee_feature_support:
	${INFO} "GraphQL: Language Feature Support"
	@echo 'Tightly integrates the GraphQL Ecosystem with VSCode for an awesome developer experience'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=GraphQL.vscode-graphql"
	${INSTALL} "vscode:extension/GraphQL.vscode-graphql"

graphql_syntax_highlighting:
	${INFO} "GraphQL: Syntax Highlighting"
	@echo 'Adds full GraphQL syntax highlighting and language support such as bracket matching'
	${LINK} "https://marketplace.visualstudio.com/items?itemName=GraphQL.vscode-graphql-syntax"
	${INSTALL} "vscode:extension/GraphQL.vscode-graphql-syntax"

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
