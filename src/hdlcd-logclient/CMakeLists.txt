set(Boost_USE_STATIC_LIBS OFF) 
set(Boost_USE_MULTITHREADED ON)  
set(Boost_USE_STATIC_RUNTIME OFF) 
find_package(Boost REQUIRED COMPONENTS system signals program_options regex)
include_directories(${Boost_INCLUDE_DIR})
include_directories("${PROJECT_SOURCE_DIR}/src/shared")

find_package(Threads)

add_executable(hdlcd-logclient
    main-hdlcd-logclient.cpp
)

if(WIN32)
    set(ADDITIONAL_LIBRARIES wsock32 ws2_32)
else()
    set(ADDITIONAL_LIBRARIES "")
endif()

target_link_libraries(hdlcd-logclient
    ${Boost_LIBRARIES}
    ${CMAKE_THREAD_LIBS_INIT}
    ${ADDITIONAL_LIBRARIES}
)

install(TARGETS hdlcd-logclient RUNTIME DESTINATION bin)
