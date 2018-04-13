cmake_minimum_required(VERSION 3.1)
project(OMPEval)

set(LibDivideFiles "${CMAKE_CURRENT_LIST_DIR}/libdivide/libdivide.h")
set(OMPEvalFiles
        "${CMAKE_CURRENT_LIST_DIR}/omp/CardRange.cpp"
        "${CMAKE_CURRENT_LIST_DIR}/omp/CardRange.h"
        "${CMAKE_CURRENT_LIST_DIR}/omp/CombinedRange.cpp"
        "${CMAKE_CURRENT_LIST_DIR}/omp/CombinedRange.h"
        "${CMAKE_CURRENT_LIST_DIR}/omp/Constants.h"
        "${CMAKE_CURRENT_LIST_DIR}/omp/EquityCalculator.cpp"
        "${CMAKE_CURRENT_LIST_DIR}/omp/EquityCalculator.h"
        "${CMAKE_CURRENT_LIST_DIR}/omp/Hand.h"
        "${CMAKE_CURRENT_LIST_DIR}/omp/HandEvaluator.cpp"
        "${CMAKE_CURRENT_LIST_DIR}/omp/HandEvaluator.h"
        "${CMAKE_CURRENT_LIST_DIR}/omp/OffsetTable.hxx"
        "${CMAKE_CURRENT_LIST_DIR}/omp/Random.h"
        "${CMAKE_CURRENT_LIST_DIR}/omp/Util.h"
        "${CMAKE_CURRENT_LIST_DIR}/ttest/ttest.h")

add_library(libOMPEval STATIC ${OMPEvalFiles} ${LibDivideFiles})
target_include_directories(libOMPEval PUBLIC ${CMAKE_CURRENT_LIST_DIR})