cmake_minimum_required(VERSION 3.26)
project(IaDCM)

set(CMAKE_CXX_STANDARD 23)

add_executable(L1
    L1/main.cpp
        L1/PowerInfo.cpp
        L1/PowerInfo.h
        L1/BatteryInfo.cpp
        L1/BatteryInfo.h
        L1/System.cpp
        L1/System.h
)
target_link_libraries(L1 PRIVATE iphlpapi setupapi PowrProf)
