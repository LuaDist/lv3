# Copyright (C) 2007-2009 LuaDist.
# Created by Peter Kapec
# Redistribution and use of this file is allowed according to the terms of the MIT license.
# For details see the COPYRIGHT file distributed with LuaDist.
# Please note that the package source code is licensed under its own license.

PROJECT(lv3 C)
CMAKE_MINIMUM_REQUIRED(VERSION 2.6)
INCLUDE(dist.cmake)

# Build
ADD_LUA_MODULE(v3 lv3.c v3.def)
TARGET_LINK_LIBRARIES(v3 ${ZLIB_LIBRARIES})

# Install all files and documentation
INSTALL (TARGETS v3 DESTINATION ${INSTALL_CMOD})
INSTALL (FILES README DESTINATION ${INSTALL_DATA})
INSTALL (FILES test.lua DESTINATION ${INSTALL_TEST})
