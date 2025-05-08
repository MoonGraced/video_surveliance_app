cmake_minimum_required(VERSION 3.20)
project(video_surveliance_app)

set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCE_FILES src/source_files/main.cpp)
set(HEADER_FILES src/header_files/)

# Создание исполняемого файла
add_executable(${PROJECT_NAME} ${SOURCE_FILES})

# Подключение заголовочных файлов
target_include_directories(${PROJECT_NAME} PRIVATE ${HEADER_FILES})

# Включение оптимизаций -O3 для Release сборки
if(CMAKE_BUILD_TYPE STREQUAL "Release")
    add_compile_options(-O3)
endif()
