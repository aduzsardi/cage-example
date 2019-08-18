PROJECT_NAME=cage-example
CAGE_VERSION=v0.2.7
OS=osx
dep: ## Install dependencies, like cage
	curl -L https://github.com/faradayio/cage/releases/download/${CAGE_VERSION}/cage-${CAGE_VERSION}-${OS}.zip -o cage.zip
	unzip cage.zip
	rm cage.zip

refresh: ## Refresh cage cache for tut
	rm -rf .cage

build_dummy: # Necessary so you have a test/image somewhere...
	docker build src/ -t test/image

help: ## Display this help screen
	@grep -h -E '^[a-zA-Z_-]+:.*?## .*$$' $(MAKEFILE_LIST) | awk 'BEGIN {FS = ":.*?## "}; {printf "\033[36m%-30s\033[0m %s\n", $$1, $$2}'
