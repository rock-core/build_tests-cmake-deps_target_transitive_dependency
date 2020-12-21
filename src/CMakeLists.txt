rock_library(deps_target_transitive_dependency_pkgconfig
    SOURCES Dummy.cpp
    HEADERS Dummy.hpp)

rock_library(deps_target_transitive_dependency_cmake
    SOURCES DummyCMake.cpp
    HEADERS DummyCMake.hpp
    EXPORT cmake)

install(EXPORT cmake
        NAMESPACE deps_target_transitive_dependency::
        DESTINATION lib/cmake/deps_target_transitive_dependency)
install(FILES deps_target_transitive_dependency-config.cmake
        DESTINATION lib/cmake/deps_target_transitive_dependency)
