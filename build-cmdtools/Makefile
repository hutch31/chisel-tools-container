VERSION=0.1
CONTAINER_NAME=hutch31/chisel-cmdline-container

target:
	docker build -t ${CONTAINER_NAME}:${VERSION} .

push:
	docker tag ${CONTAINER_NAME}:${VERSION} ${CONTAINER_NAME}:latest
	docker push ${CONTAINER_NAME}:${VERSION}

