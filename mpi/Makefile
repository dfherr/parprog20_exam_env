CXX = mpicxx
CXX_FLAGS = --std=c++17 -Wall -Wextra -march=native -O3 -g -DOMPI_SKIP_MPICXX
# this compiler definition is needed to silence warnings caused by the openmpi CXX
# bindings that are deprecated. This is needed on gcc 8 forward.
# see: https://github.com/open-mpi/ompi/issues/5157

all: sequential_implementation student_submission

sequential_implementation: sequential_implementation.cpp
	$(CXX) $(CXX_FLAGS) -o sequential_implementation sequential_implementation.cpp

student_submission: student_submission.cpp
	$(CXX) $(CXX_FLAGS) -o student_submission student_submission.cpp

clean:
	rm -f sequential_implementation student_submission
