INCLUDE_DIRECTORIES(${ROSS_SOURCE_DIR})
## If you will be using the ROSSIO library add this
#INCLUDE_DIRECTORIES(${ROSSIO_SOURCE_DIR})

# Files you have included in your model
SET(model_srcs
	model_driver.c  
	model.h
)

# Set the executable name here: ross-model
# You will be executing the ./ross-model binary
# Main function (in this case) is found in model_main.c

ADD_EXECUTABLE(sr-model model_main.c ${model_srcs})


TARGET_LINK_LIBRARIES(sr-model ROSS m)
## Alternatively, use this command with ROSSIO
#TARGET_LINK_LIBRARIES(sr-model ROSS ROSSIO m)