
# Усложненный make-file.  Введены переменные для параметров компиляции и исполняемых файлов

.PHONY: all debug release clean

RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall
RELEASE_EXEC  = hello
DEBUG_EXEC    = hello-dbg
ISH = hello.cpp 
#SOURCE        =

all: debug release

debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(ISH)
	g++ $(DEBUG_FLAGS) $(ISH) -o $(DEBUG_EXEC) 

release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(ISH)
	g++ $(RELEASE_FLAGS) $(ISH) -o $(RELEASE_EXEC)

clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)

