CXXFLAGS=-Wall -std=c++14
CXX=g++
INCLUDES=-I../../polylidar -I/home/jeremy/miniconda3/envs/polylidar/include -I/home/jeremy/miniconda3/envs/polylidar/include/python3.6m -I/home/jeremy/.local/include -I/home/jeremy/miniconda3/envs/polylidar/lib/python3.6/site-packages/numpy/core/include
LDFLAGS=-L/usr/local/lib

POLYLIDAR_DIR = ../../polylidar
TARGET=simple


CPPFILES=$(POLYLIDAR_DIR)/polylidar.cpp $(POLYLIDAR_DIR)/helper.cpp $(POLYLIDAR_DIR)/delaunator.cpp simple.cpp
OBJFILES=polylidar.o helper.o delaunator.o simple.o

all: $(TARGET)


OBJFILESD:$(CPPFILES)
	$(CXX) $(CXXFLAGS) -c $(CPPFILES) $(INCLUDES)


$(TARGET): OBJFILESD
	$(CXX) $(CXXFLAGS) $(LDFLAGS) $(OBJFILES) $(INCLUDES) -o ./bin/$(TARGET)

# polylidar:$(POLYLIDAR_DIR)/polylidar.cpp $(POLYLIDAR_DIR)/helper.cpp $(POLYLIDAR_DIR)/delaunator.cpp


# all: simple.cpp
	
clean:
	$(RM) ./bin/simple
	$(RM) $(OBJFILES)