add_contract(nordicenergy nordicenergy ${CMAKE_CURRENT_SOURCE_DIR}/src/nordicenergy.cpp)

target_include_directories(nordicenergy
   PUBLIC
   ${CMAKE_CURRENT_SOURCE_DIR}/include)

set_target_properties(nordicenergy
   PROPERTIES
   RUNTIME_OUTPUT_DIRECTORY "${CMAKE_CURRENT_BINARY_DIR}")

configure_file( ${CMAKE_CURRENT_SOURCE_DIR}/ricardian/nordicenergy.contracts.md.in ${CMAKE_CURRENT_BINARY_DIR}/ricardian/nordicenergy.contracts.md @ONLY )

target_compile_options( nordicenergy PUBLIC -R${CMAKE_CURRENT_SOURCE_DIR}/ricardian -R${CMAKE_CURRENT_BINARY_DIR}/ricardian )
