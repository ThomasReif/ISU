CXX=g++
CXXFLAGS=-Wall -g -Werror -Wextra -pedantic -std=c++20 -I.
NAME=parts
SOURCES=part1.cpp part2.cpp main.cpp
OBJECTS=${SOURCES:.cpp=.o}


#Meta opskrift -> opskrift til opskrift
%.o: %.cpp	
	@echo "Compiling $<"
	@$(CXX) $(CXXFLAGS) -c $< -o $@

all: ${OBJECTS}
	@echo "Linking..."
	@$(CXX) $(CXXFLAGS) $^ -o ${NAME}
	

.PHONY: clean help all
clean:
	@echo "Cleaning..."
	@rm -f *.o ./${NAME}

help: 
	$(info type 'make' to compile program)
	$(info type 'all' to compile program)
	$(info type 'clean' to remove compiled files)