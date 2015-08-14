INCLUDE_DIRECTORIES(${ROSS_SOURCE_DIR} ${ROSS_BINARY_DIR})
## Must include binary dir for config.h

## If you will be using the RIO library add this
#INCLUDE_DIRECTORIES(${RIO_SOURCE_DIR} ${RIO_BINARY_DIR})

# Files you have included in your model
SET(model_srcs
	model_driver.c  
	model.h
)

# Set the executable name here: model
# You will be executing the ./model binary
ADD_EXECUTABLE(model ${model_srcs})

TARGET_LINK_LIBRARIES(model ROSS m)
## Alternatively, use this command with RIO
#TARGET_LINK_LIBRARIES(model ROSS RIO m)
