# Create a variable containing all .cpp files
FILE(GLOB files *.cpp)
FILE(GLOB libs *.so)

# Create an executable file from sources
ADD_EXECUTABLE(unit_tests ${files})
TARGET_LINK_LIBRARIES(unit_tests ${LIBRARY_OUTPUT_PATH}/libMTF.so ${LIBRARY_OUTPUT_PATH}/libDC.so ${LIBRARY_OUTPUT_PATH}/libIF.so)


#install(
#  TARGETS unit_tests
#  RUNTIME DESTINATION bin
#)
