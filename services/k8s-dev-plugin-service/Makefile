BIN=k8s-dev-plugin

all: bin 

${BIN}: main.go server.go watcher.go
	go build -a -ldflags '-extldflags "-static"' ${GCFLAGS} -o $@

bin: ${BIN}

help:
	@echo 'make bin   --build executable file'

clean:
	rm -f ${BIN}
	
.PHONY : help all bin clean 
