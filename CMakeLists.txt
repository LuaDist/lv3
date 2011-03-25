# Copyright (C) 2007-2011 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

project ( lv3 C )
cmake_minimum_required ( VERSION 2.6 )
include ( dist.cmake )

install_lua_module ( v3 lv3.c v3.def )
target_link_libraries ( v3 ${ZLIB_LIBRARIES} )

install_data ( README )
install_test ( test.lua )

add_lua_test ( test.lua )

