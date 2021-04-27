project(stdvexassets)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract( stdvexassets stdvexassets stdvexassets.cpp )
target_include_directories( stdvexassets PUBLIC ${CMAKE_SOURCE_DIR}/../include )
target_ricardian_directory( stdvexassets ${CMAKE_SOURCE_DIR}/../ricardian )



