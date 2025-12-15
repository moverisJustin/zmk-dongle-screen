zephyr_include_directories(include)
zephyr_library()

if(CONFIG_SHIELD_DONGLE_SCREEN)

        # Custom ST7789V driver disabled - Zephyr 4.1 uses built-in MIPI DBI driver
        # add_subdirectory(${ZEPHYR_CURRENT_MODULE_DIR}/drivers/display)

        # Custom LVGL module disabled - Zephyr 4.1 uses LVGL 9.x with new APIs
        # The old lvgl.c used LVGL 8.x APIs (lv_disp_drv_t, etc.) which are removed in LVGL 9.x
        # Zephyr's built-in LVGL integration handles display initialization now
        # add_subdirectory(${ZEPHYR_CURRENT_MODULE_DIR}/modules/lvgl)


endif()