FILE(GLOB PY_FILES *.py)

FILE(GLOB UI_FILES *.ui)
PYQT4_WRAP_UI(PYUI_FILES ${UI_FILES})

ADD_CUSTOM_TARGET(sextante_about ALL DEPENDS ${PYUI_FILES})

INSTALL(FILES ${PY_FILES} DESTINATION ${SEXTANTE_PLUGIN_DIR}/about)
INSTALL(FILES ${PYUI_FILES} DESTINATION ${SEXTANTE_PLUGIN_DIR}/about)
