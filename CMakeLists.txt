cmake_minimum_required (VERSION 3.11)
project(i2c_analyzer)

# custom CMake Modules are located in the cmake directory.
set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)

include(ExternalAnalyzerSDK)

set(SOURCES 
src/I2cAnalyzer.cpp
src/I2cAnalyzer.h
src/I2cAnalyzerResults.cpp
src/I2cAnalyzerResults.h
src/I2cAnalyzerSettings.cpp
src/I2cAnalyzerSettings.h
src/I2cSimulationDataGenerator.cpp
src/I2cSimulationDataGenerator.h
)

add_analyzer_plugin(i2c_analyzer SOURCES ${SOURCES})
