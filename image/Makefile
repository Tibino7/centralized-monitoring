include INFO

.PHONY: build push release

build:
	docker build $(DOCKER_BUILD_OPTS) -t $(FINAL_IMAGE_NAME) .

run:
	docker run --name $(CONTAINER) $(DOCKER_OPTS) $(FINAL_IMAGE_NAME)
	sleep $(TIMEOUT)

push:
	docker push $(FINAL_IMAGE_NAME)

release: build push

default: build
