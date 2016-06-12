AUTOMAKE_OPTIONS = foreign

bin_PROGRAMS = helloworld
helloworld_SOURCES = main.cpp

AM_CXXFLAGS = -Wall -fPIC
if ENABLEGCOV
AM_CXXFLAGS += -fprofile-arcs -ftest-coverage
endif
