INCLUDE_DIRECTORIES("${CMAKE_CURRENT_SOURCE_DIR}")

SET(src 
  THOmpTensorConv.c)

SET(src ${src})

ADD_LIBRARY(THOmp SHARED ${src})
TARGET_LINK_LIBRARIES(THOmp TH)

INSTALL(TARGETS THOmp
          RUNTIME DESTINATION "${Torch_INSTALL_BIN_SUBDIR}"
          LIBRARY DESTINATION "${Torch_INSTALL_LIB_SUBDIR}"
          ARCHIVE DESTINATION "${Torch_INSTALL_LIB_SUBDIR}")
