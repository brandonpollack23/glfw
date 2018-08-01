package(
    default_visibility = ["//visibility:private"],
)

filegroup(
    name = "glfw_deps",
    srcs = glob(["deps/**/*.c", "deps/**/*.h"]),
)

filegroup(
    name = "glfw_src",
    srcs = glob(["src/**/*.c", "src/**/*.h", "include/GLFW/*"]),
)

filegroup(
    name = "glfw_src_textual",
    srcs = glob(["src/**/*.m", "src/**/*.in"]),
)

filegroup(
    name = "glfw_tests",
    srcs = glob(["tests/*.c"]),
)

filegroup(
    name = "glfw_source_files",
    srcs = [":glfw_deps", ":glfw_src", ":glfw_tests"]
)

# TODO docs

# TODO toolchains for different plats.
# TODO configurations for shared object/dynlib
# TODO Vulkan loader config
cc_library(
    name = "glfw",
    srcs = [":glfw_source_files"],
    textual_hdrs = ["glfw_src_textual"],
    hdrs = ["include/GLFW/glfw3.h"],
    defines = [
        "_GLFW_X11",
        "_GLFW_HAS_XF86VM",
    ],
    include_prefix = "GLFW",
    visibility = ["//visibility:public"],
)

