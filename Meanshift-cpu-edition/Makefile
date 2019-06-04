CU_APPS=     # specify the name of CUDA file (exclude .cu)
C_APPS=  	# specify the name of OpenMP file (exclude .c) 
CPP_APPS=Maincpp

CFLAGS=`pkg-config --cflags --libs opencv4`
GCC_HOME=gcc # specify your own gcc install path
CPP_HOME=g++ 

all: ${CU_APPS} ${C_APPS} ${CPP_APPS}

%: %.cu
	nvcc -lm -o $@ $<
%: %.c
	${GCC_HOME} -fopenmp -lm -o $@ $<
%: %.cpp
	${CPP_HOME} ${CFLAGS} -o $@ MeanShift.cpp $<

clean:
	rm -f ${CU_APPS} ${C_APPS} $(CPP_APPS)
