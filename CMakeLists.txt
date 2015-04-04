set(stb_ROOT_DIR ${TUPA_DEPS_DIR}/common/stb)

set(stb_SOURCE_FILES
    ${stb_ROOT_DIR}/stb_voxel_render.h
)

set(stb_INCLUDE_DIRS
	${TUPA_DEPS_DIR}/stb
)

IF(${TARGET} MATCHES "Windows")
    set(stb_INCLUDE_DIRS)
ENDIF()

IF(${TARGET} MATCHES "Linux")
    set(stb_LIBS
        )
ELSEIF(${TARGET} MATCHES "Windows")
    set(stb_LIBS
        )
ENDIF()

#include_directories (${stb_INCLUDE_DIRS})
add_library (stb INTERFACE)
target_sources(stb INTERFACE ${stb_SOURCE_FILES})

#target_link_libraries (stb ${stb_LIBS})
