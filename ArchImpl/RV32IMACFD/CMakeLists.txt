# Generated on Wed, 25 May 2022 18:09:21 +0200.
#
# This file contains the CMake build info for the RV32IMACFD core architecture.

PROJECT(RV32IMACFD)

ADD_LIBRARY(${PROJECT_NAME} SHARED
	RV32IMACFDArch.cpp
	RV32IMACFDArchLib.cpp
	RV32IMACFDArchSpecificImp.cpp
	RV32IMACFDInstr.cpp
	RV32IMACFD_RISCVBaseInstr.cpp
	RV32IMACFD_RV32IInstr.cpp
	RV32IMACFD_RV32ICInstr.cpp
	RV32IMACFD_RV32MInstr.cpp
	RV32IMACFD_ZicsrInstr.cpp
	RV32IMACFD_RV32FInstr.cpp
	RV32IMACFD_RV32FCInstr.cpp
	RV32IMACFD_RV32DInstr.cpp
	RV32IMACFD_RV32DCInstr.cpp
	RV32IMACFD_ZifenceiInstr.cpp
	RV32IMACFD_tum_csrInstr.cpp
	RV32IMACFD_tum_retInstr.cpp
	RV32IMACFD_RV32AInstr.cpp
	RV32IMACFD_tum_rvaInstr.cpp
)

FILE(COPY "${CMAKE_CURRENT_LIST_DIR}/${PROJECT_NAME}Funcs.h" DESTINATION "${ETISS_BINARY_DIR}/include/jit/Arch/${PROJECT_NAME}")
INSTALL(FILES "${CMAKE_CURRENT_LIST_DIR}/${PROJECT_NAME}Funcs.h" DESTINATION "include/jit/Arch/${PROJECT_NAME}")

ETISSPluginArch(${PROJECT_NAME})