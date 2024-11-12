cmake_minimum_required(VERSION 3.5)
project(calculator C)

add_subdirectory(include)
add_subdirectory(src)

include_directories(include)

enable_testing()

# Tests existants
add_test(t1 src/calculator add 2 3)
add_test(t2 src/calculator sub 3 -2)
add_test(t3 src/calculator mul 5 5)
add_test(t4 src/calculator div 1 5)

# Nouveau test pour la fonction carré (car)
add_test(t5 src/calculator car 5 0)  # Le carré de 5 est 25, donc on passe 5 en paramètre.
