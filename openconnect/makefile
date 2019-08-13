GIT_COMMIT := $(shell git describe --tags --dirty=-unsupported --always || echo pre-commit)

build:
	docker build -t drewwells/openconnect:`cat VERSION`-$(GIT_COMMIT) .

push: build
	docker push drewwells/openconnect:`cat VERSION`-$(GIT_COMMIT)
