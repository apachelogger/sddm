install(DIRECTORY   "faces"                             DESTINATION "${DATA_INSTALL_DIR}")
install(DIRECTORY   "flags"                             DESTINATION "${DATA_INSTALL_DIR}")

install(FILES "org.freedesktop.DisplayManager.conf"       DESTINATION "${DBUS_CONFIG_DIR}")

install(FILES "scripts/Xsession" "scripts/Xsetup" "scripts/Xstop" DESTINATION "${DATA_INSTALL_DIR}/scripts"
        PERMISSIONS OWNER_READ OWNER_WRITE OWNER_EXECUTE
        GROUP_READ GROUP_EXECUTE
        WORLD_READ WORLD_EXECUTE)

if(BUILD_MAN_PAGES)
    add_subdirectory(man)
endif()
add_subdirectory(themes)
add_subdirectory(translations)
