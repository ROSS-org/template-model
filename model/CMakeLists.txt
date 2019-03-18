# All source files for the model
SET(model_srcs
	model_main.c
	model_driver.c
	model_map.c
	model.h
)

# Set the executable name here: model
# You will be executing the ./model binary
BLT_ADD_EXECUTABLE(NAME model
  SOURCES ${model_srcs}
  INCLUDES ${CMAKE_CURRENT_SOURCE_DIR}
  DEPENDS_ON ROSS MPI)
