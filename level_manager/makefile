Flag=-Wall -Wextra
CC=g++


level2=level2/puzzle2.o level2/puzzle2functions.o level2/puzzle2x
pathChoice=path_choice/path_choice_main.o path_choice/path_choice_functions.o path_choice/pathChoicex

all: LvlManagerx level2/puzzle2x path_choice/pathChoicex

LvlManagerx: LvlManager.o LvlFunctions.o
	${CC} LvlManager.o LvlFunctions.o -o $@

LvlManager.o: LvlManager.cpp LvlManager.h
	${CC} ${Flag} -c $< -o $@

LvlFunctions.o: LvlFunctions.cpp LvlManager.h
	${CC} ${Flag} -c $< -o $@

#level 2 compilation

level2/puzzle2x: level2/puzzle2.o level2/puzzle2functions.o
	${CC} level2/puzzle2.o level2/puzzle2functions.o -o $@


level2/puzzle2.o: level2/fifteenTiles_main.cpp level2/fifteenTiles_header.h
	${CC} ${Flag} -c $< -o $@

level2/puzzle2functions.o: level2/fifteenTiles_functions.cpp level2/fifteenTiles_header.h
	${CC} ${Flag} -c $< -o $@


#Level Choice Compilation

path_choice/pathChoicex: path_choice/path_choice_main.o path_choice/path_choice_functions.o
	${CC} path_choice/path_choice_main.o path_choice/path_choice_functions.o -o $@

path_choice/path_choice_main.o: path_choice/path_choice_main.cpp path_choice/path_choice_header.h
	${CC} ${Flag} -c $< -o $@

path_choice/path_choice_functions.o: path_choice/path_choice_functions.cpp path_choice/path_choice_header.h
	${CC} ${Flag} -c $< -o $@

.PHONY: clean
clean:
	-rm -rf ${level2} ${pathChoice}


