if(CONFIG_CSI_APP_TYPE_SENDER OR CONFIG_CSI_APP_TYPE_RECEIVER)
    list(APPEND srcs "csi_manager.c")
endif()

idf_component_register(SRCS ${srcs}
                            "main.c"
                            "init_manager.c"
                    INCLUDE_DIRS "."
                    REQUIRES nvs_flash esp_event esp_wifi)