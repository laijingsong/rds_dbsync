cmake_minimum_required(VERSION 3.15)
project(rds_dbsync)

set(CMAKE_CXX_STANDARD 14)

include_directories(/usr/include/postgresql/9.6/server /usr/include/postgresql /usr/include/postgresql/internal /usr/include/mysql)

add_executable(rds_dbsync
        #dbsync/dbsync-mysql2pgsql.c
        #dbsync/dbsync-pgsql2pgsql.c
        dbsync/demo.cpp
        dbsync/ini.c
        dbsync/ini.h
        dbsync/misc.c
        dbsync/misc.h
        #dbsync/mysql2pgsql.c
        dbsync/pg_logicaldecode.c
        dbsync/pg_logicaldecode.h
        dbsync/pgsync.c
        dbsync/pgsync.h
        dbsync/pqformat.c
        dbsync/readcfg.cpp
        dbsync/readcfg.h
        dbsync/stringinfo.c
        dbsync/utils.c
        dbsync/utils.h)


target_link_libraries(rds_dbsync
        pq
        dl
        m
        pthread
        )
