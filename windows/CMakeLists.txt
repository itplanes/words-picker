set(TARGET_NAME windows)

aux_source_directory(. DIR_LIB_SRCS)

add_library (${TARGET_NAME} ${DIR_LIB_SRCS})

# 导入Qt包，需要放在add_executable之后
set(QT Widgets)
find_package(Qt5 REQUIRED ${QT})
qt5_use_modules(${TARGET_NAME} ${QT})
