set(SRCS
	"src/main.cpp"
)

add_executable(test ${SRCS})

target_compile_features(test PRIVATE cxx_std_20)

# for Visual Studio/MSVC
set_target_properties(test PROPERTIES MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>")
source_group(TREE ${CMAKE_CURRENT_SOURCE_DIR} FILES ${SRCS})