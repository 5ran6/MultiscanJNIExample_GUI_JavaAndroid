# For more information about using CMake with Android Studio, read the
# documentation: https://d.android.com/studio/projects/add-native-code.html

# Sets the minimum version of CMake required to build the native library.

cmake_minimum_required(VERSION 3.4.1)

# Creates and names a library, sets it as either STATIC
# or SHARED, and provides the relative paths to its source code.
# You can define multiple libraries, and CMake builds them for you.
# Gradle automatically packages shared libraries with your APK.

include_directories(
    ../../../HEADERS
    ../../../LIBS_SOURCE/ANDROID_JNI)

add_library( # Sets the name of the library.
             GBFRSW_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/GBFRSW_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             GBMSAPI_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/GBMSAPI_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             WSQ_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/WSQ_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             LFS_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/LFS_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             GBFINIMG_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/GBFINIMG_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             GBJPEG_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/GBJPEG_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             AN2000_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/AN2000_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp)

add_library( # Sets the name of the library.
             GBFIR_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/GBFIR_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             GBNFIQ_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/GBNFIQ_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             GBNFIQ2_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/GBNFIQ2_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

add_library( # Sets the name of the library.
             BOZORTH_JNI

             # Sets the library as a shared library.
             SHARED

             # Provides a relative path to your source file(s).
             ../../../LIBS_SOURCE/ANDROID_JNI/BOZORTH_JNI.cpp
             ../../../LIBS_SOURCE/ANDROID_JNI/GB_JNI_Utils.cpp )

# Searches for a specified prebuilt library and stores the path as a
# variable. Because CMake includes system libraries in the search path by
# default, you only need to specify the name of the public NDK library
# you want to add. CMake verifies that the library exists before
# completing its build.

find_library( # Sets the name of the path variable.
              log-lib

              # Specifies the name of the NDK library that
              # you want CMake to locate.
              log )

# Specifies libraries CMake should link to your target library. You
# can link multiple libraries, such as libraries you define in this
# build script, prebuilt third-party libraries, or system libraries.

target_link_libraries( # Specifies the target library.
                       GBFRSW_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      GBMSAPI_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      WSQ_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      LFS_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      GBFINIMG_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      GBJPEG_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      AN2000_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )
					   
target_link_libraries( # Specifies the target library.
                      GBFIR_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      GBNFIQ_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      GBNFIQ2_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )

target_link_libraries( # Specifies the target library.
                      BOZORTH_JNI

                       # Links the target library to the log library
                       # included in the NDK.
                       ${log-lib} )