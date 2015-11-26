SHELL = bash

build:
	packer \
		build \
			-var-file Variables/Production.json \
			Template.json
	mkdir ../../Artifacts/Debian_amd64/
	mv -f -v output-debian-amd64-*/* ../../Artifacts/Debian_amd64/

debug-build:
	PACKER_LOG=1 PACKER_LOG_PATH=Packer.log packer \
		build \
			-debug \
			-var-file Variables/Development.json \
			Template.json

clean:
	rm -rf packer_cache
	rm -rf output-debian-amd64-*
	rm Packer.log

.PHONY: build debug-build clean
