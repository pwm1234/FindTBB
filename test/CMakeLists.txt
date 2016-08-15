cmake_minimum_required(VERSION 2.6)
project(TestFindTBB)

list(APPEND CMAKE_MODULE_PATH "..")

message("CMAKE_SYSTEM_NAME = '${CMAKE_SYSTEM_NAME}'")
message("CMAKE_BUILD_TYPE  = '${CMAKE_BUILD_TYPE}'")

message("User Input Variables:")
message("TBB_ROOT_DIR = '${TBB_ROOT_DIR}'")
message("TBB_INCLUDE_DIR = '${TBB_INCLUDE_DIR}'")
message("TBB_LIBRARY = '${TBB_LIBRARY}'")
message("TBB_tbb_LIBRARY = '${TBB_tbb_LIBRARY}'")
message("TBB_tbb_debug_LIBRARY = '${TBB_tbb_debug_LIBRARY}'")
message("TBB_tbbmalloc_LIBRARY = '${TBB_tbbmalloc_LIBRARY}'")
message("TBB_tbbmalloc_debug_LIBRARY = '${TBB_tbbmalloc_debug_LIBRARY}'")
message("TBB_tbb_preview_LIBRARY = '${TBB_tbb_preview_LIBRARY}'")
message("TBB_tbb_preview_debug_LIBRARY = '${TBB_tbb_preview_debug_LIBRARY}'")
message("TBB_USE_DEBUG_BUILD = '${TBB_USE_DEBUG_BUILD}'")

message("Environment Varaibles used by FindTBB:")
message("TBB_INSTALL_DIR = '$ENV{TBB_INSTALL_DIR}'")
message("TBBROOT         = '$ENV{TBBROOT}'")
message("LIBRARY_PATH    = '$ENV{LIBRARY_PATH}'")

find_package(TBB COMPONENTS tbbmalloc tbbmalloc_proxy tbb_preview)


set(TBB_SEARCH_COMPOMPONENTS tbb_preview tbbmalloc_proxy tbbmalloc tbb)

message("FindTBB Result Variables:")
message("TBB_FOUND = '${TBB_FOUND}'")
message("TBB_tbbmalloc_FOUND = '${TBB_tbbmalloc_FOUND}'")
message("TBB_tbbmalloc_proxy_FOUND = '${TBB_tbbmalloc_FOUND}'")
message("TBB_tbb_preview_FOUND = '${TBB_tbb_preview_FOUND}'")
message("TBB_VERSION = '${TBB_VERSION}'")
message("TBB_VERSION_MAJOR = '${TBB_VERSION_MAJOR}'")
message("TBB_VERSION_MINOR = '${TBB_VERSION_MINOR}'")
message("TBB_INTERFACE_VERSION = '${TBB_INTERFACE_VERSION}'")
foreach(_comp ${TBB_SEARCH_COMPOMPONENTS})
  message("TBB_${_comp}_LIBRARY_RELEASE = '${TBB_${_comp}_LIBRARY_RELEASE}'")
  message("TBB_${_comp}_LIBRARY_DEBUG = '${TBB_${_comp}_LIBRARY_DEBUG}'")
  message("TBB_${_comp}_LIBRARY = '${TBB_${_comp}_LIBRARY}'")
endforeach()

message("FindTBB Output Variables:")
message("TBB_INCLUDE_DIRS = '${TBB_INCLUDE_DIRS}'")
message("TBB_LIBRARIES_RELEASE = '${TBB_LIBRARIES_RELEASE}'")
message("TBB_LIBRARIES_DEBUG = '${TBB_LIBRARIES_DEBUG}'")
message("TBB_LIBRARIES = '${TBB_LIBRARIES}'")
message("TBB_DEFINITIONS = '${TBB_DEFINITIONS}'")