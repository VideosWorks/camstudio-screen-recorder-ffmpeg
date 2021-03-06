# Copyright (C) 2018  Steven Hoving
#
# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.
#
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <https://www.gnu.org/licenses/>.

add_subdirectory(zlib)

#set(SKIP_INSTALL_HEADERS ON CACHE BOOL "" FORCE)
add_subdirectory(minilzo)
add_subdirectory(fmt)
add_subdirectory(mouse_simulation)
add_subdirectory(googletest)
add_subdirectory(google_benchmark)

# spdlog settings
set(SPDLOG_FMT_EXTERNAL ON CACHE BOOL "" FORCE)
set(SPDLOG_NO_ATOMIC_LEVELS ON CACHE BOOL "" FORCE)
add_subdirectory(spdlog)
add_subdirectory(yuvconvert)

# cpptoml settings
set(CPPTOML_BUILD_EXAMPLES OFF CACHE BOOL "Disable cpptoml examples" FORCE)
add_subdirectory(cpptoml)

# fmt format library settings.
set_target_properties(fmt PROPERTIES FOLDER "External/fmt")
set_target_properties(mouse_simulation PROPERTIES FOLDER "External/mouse_simulation")
set_target_properties(spdlog_headers_for_ide PROPERTIES FOLDER "External/spdlog")
set_target_properties(yuvconvert PROPERTIES FOLDER "External/yuvconvert")
