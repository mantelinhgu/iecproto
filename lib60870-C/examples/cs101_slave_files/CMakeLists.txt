include_directories(
   .
)

set(example_SRCS
   cs101_slave_files.c
)

IF(WIN32)
set_source_files_properties(${example_SRCS}
                                       PROPERTIES LANGUAGE CXX)
ENDIF(WIN32)

add_executable(cs101_slave_files
  ${example_SRCS}
)

target_link_libraries(cs101_slave_files
    lib60870
)
