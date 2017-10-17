cmake_minimum_required(VERSION 3.2)
project(pdo_mysql)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

INCLUDE_DIRECTORIES(
    .
    ..
    /usr/local/Cellar/php71/7.1.5_17/include/php/
    /usr/local/Cellar/php71/7.1.5_17/include/php/main
    /usr/local/Cellar/php71/7.1.5_17/include/php/Zend
)

set(SOURCE_FILES
    mysql_driver.c
    mysql_statement.c
    pdo_mysql.c
    php_pdo_mysql.h
    php_pdo_mysql_int.h
    php_pdo_mysql_sqlstate.h)

add_executable(pdo_mysql ${SOURCE_FILES})