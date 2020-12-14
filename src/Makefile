build-img:
	docker build -t fc-cpp-runtime  -f build-image/Dockerfile build-image

build: build-img
	chmod 755 ./build.sh
	docker run --rm -i -v $$(pwd):/tmp fc-cpp-runtime bash -c "cd /tmp && ./build.sh"

.PHONY: build