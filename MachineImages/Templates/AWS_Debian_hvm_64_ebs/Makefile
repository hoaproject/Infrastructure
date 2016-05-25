SHELL = bash

build:
	AWS_PROFILE=infra-packer packer \
		build \
			-var-file Variables/Production.json \
			Template.json

debug-build:
	AWS_PROFILE=infra-packer PACKER_LOG=1 PACKER_LOG_PATH=Packer.log packer \
		build \
			-debug \
			-var-file Variables/Development.json \
			Template.json

clean:
	rm -rf output-debian-amd64-*
	rm Packer.log

purge:
	rm -rf packer_cache
	make clean

.PHONY: build debug-build clean purge
