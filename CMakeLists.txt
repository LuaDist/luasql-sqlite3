# Copyright (C) 2007-2012 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( luasql C )
cmake_minimum_required ( VERSION 2.8 )
include ( cmake/dist.cmake )
include ( lua )

find_package ( SQLite3 REQUIRED )
include_directories ( ${SQLITE3_INCLUDE_DIRS} src )
install_lua_module ( luasql.sqlite3 src/ls_sqlite3.c src/luasql.c LINK ${SQLITE3_LIBRARIES} )
