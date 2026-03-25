**Задание 1.**
mkdir -p formatter_lib
>
cd formatter_lib
>
nano formatter.cpp
> file
nano formatter.h
> file
cat > CMakeLists.txt << 'EOF'
cmake_minimum_required(VERSION 3.10)

project(formatter_lib VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(formatter STATIC
    formatter.cpp
    formatter.h
)

target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
EOF
> 
mkdir build
> 
cd build
>
cmake ..
> -- The C compiler identification is GNU 14.2.0
-- The CXX compiler identification is GNU 14.2.0
-- Detecting C compiler ABI info
-- Detecting C compiler ABI info - done
-- Check for working C compiler: /usr/bin/cc - skipped
-- Detecting C compile features
-- Detecting C compile features - done
-- Detecting CXX compiler ABI info
-- Detecting CXX compiler ABI info - done
-- Check for working CXX compiler: /usr/bin/c++ - skipped
-- Detecting CXX compile features
-- Detecting CXX compile features - done
-- Configuring done (0.7s)
-- Generating done (0.0s)
-- Build files have been written to: /home/dashasasha/Рабочий стол/lab33/formatter_lib/build
make
> [ 50%] Building CXX object CMakeFiles/formatter.dir/formatter.cpp.o
[100%] Linking CXX static library libformatter.a
[100%] Built target formatter
ls -la
>итого 48
drwxrwxr-x 3 dashasasha dashasasha  4096 мар 25 09:00 .
drwxrwxr-x 3 dashasasha dashasasha  4096 мар 25 08:56 ..
-rw-rw-r-- 1 dashasasha dashasasha 14838 мар 25 09:00 CMakeCache.txt
drwxrwxr-x 6 dashasasha dashasasha  4096 мар 25 09:00 CMakeFiles
-rw-rw-r-- 1 dashasasha dashasasha  2194 мар 25 09:00 cmake_install.cmake
-rw-rw-r-- 1 dashasasha dashasasha  6750 мар 25 09:00 libformatter.a
-rw-rw-r-- 1 dashasasha dashasasha  5447 мар 25 09:00 Makefile
git add formatter_lib/
>
git status
