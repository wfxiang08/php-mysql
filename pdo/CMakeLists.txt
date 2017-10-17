cmake_minimum_required(VERSION 3.2)
project(pdo)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

INCLUDE_DIRECTORIES(
    .
    /usr/local/Cellar/php71/7.1.5_17/include/php/
    /usr/local/Cellar/php71/7.1.5_17/include/php/main
    /usr/local/Cellar/php71/7.1.5_17/include/php/Zend
)

set(SOURCE_FILES
    pdo.c
    pdo_dbh.c
    pdo_sql_parser.c
    pdo_sqlstate.c
    pdo_stmt.c
    php_pdo.h
    php_pdo_driver.h
    php_pdo_error.h
    php_pdo_int.h)

add_executable(pdo ${SOURCE_FILES})