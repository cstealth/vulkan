CXX 	  := g++
CXX_FLAGS := -Wall -Wextra -std=c++17 -ggdb

SRC_DIR := src
OBJ_DIR := obj
BIN_DIR := bin
LIB_DIR := lib

EXE := $(BIN_DIR)/main
SRC := $(wildcard $(SRC_DIR)/*.cpp)
OBJ := $(SRC:$(SRC_DIR)/%.cpp=$(OBJ_DIR)/%.o)

CFLAGS = -std=c++17 -O2

LDFLAGS = -lglfw -lvulkan -ldl -lpthread -lX11 -lXxf86vm -lXrandr -lXi

all: $(EXE)

run: clean all 
	clear 
	@echo "Running..."
	./$(EXE)

$(EXE): $(SRC)
	@echo "Building ..."
	$(CXX) $(CXX_FLAGS) -I$(INCLUDE) -L$(LIB_DIR) $^ -o $@ $(LDFLAGS)

clean:
	@echo "Cleaning ..."
	-rm $(BIN_DIR)/*
