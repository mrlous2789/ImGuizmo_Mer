cmake_minimum_required(VERSION 3.24)
project(ImGuizmo)

file(GLOB_RECURSE HEADERS "include/*.h")
file(GLOB_RECURSE SOURCES "src/*.cpp")

add_library(
    ImGuizmo
    STATIC
    ${HEADERS}
    ${SOURCES}
)

target_include_directories(ImGuizmo PRIVATE ../DiligentTools/ThirdParty/ImGui)
target_include_directories(ImGuizmo PRIVATE ./include)