# All source files for the model
SET(model_srcs
	model_main.c
	model_driver.c
	model_map.c
)

# Set the executable name here: model
# You will be executing the ./model binary
ADD_EXECUTABLE(model ${model_srcs})
INCLUDE_DIRECTORIES(${CMAKE_CURRENT_SOURCE_DIR})
TARGET_LINK_LIBRARIES(model ${ROSS_LIBRARIES} ${MPI_C_LIBRARIES})
