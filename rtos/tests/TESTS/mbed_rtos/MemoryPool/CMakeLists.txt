# Copyright (c) 2020-2021 ARM Limited. All rights reserved.
# SPDX-License-Identifier: Apache-2.0

include(mbed_greentea)

if(APPLICATION_PROFILE_CONFIG_BAREMETAL)
    set(TEST_SKIPPED "MemoryPool test cases require a RTOS to run.")
endif()

mbed_greentea_add_test(
    TEST_NAME
        mbed-rtos-memorypool
    TEST_SOURCES
        main.cpp
    TEST_SKIPPED
        ${TEST_SKIPPED}
)
