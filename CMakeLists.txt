zephyr_include_directories(include)
zephyr_library()

if(CONFIG_SHIELD_DONGLE_SCREEN)

        # Custom ST7789V driver disabled - Zephyr 4.1 uses built-in MIPI DBI driver
        # add_subdirectory(${ZEPHYR_CURRENT_MODULE_DIR}/drivers/display)
        add_subdirectory(${ZEPHYR_CURRENT_MODULE_DIR}/modules/lvgl)


endif()