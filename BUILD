package(
    default_visibility = ["//visibility:private"],
)

filegroup(
    name = "glfw_src",
    srcs = glob([
          "src/**/*.c",
          "src/**/*.h",
          "include/GLFW/*"
        ], exclude=[
            "src/win32*", # TODO TOOLCHAIN/config win32 windows
            "src/wgl*", # TODO TOOLCHAIN/config wgl windows
            "src/mir*", #TODO TOOLCHAIN/CONFIG mir
            "src/wl*", #TODO TOOLCHAIN/CONFIG wayland
            "src/null*", #TODO TOOLCHAIN/CONFIG null window
            "src/cocoa*", #TODO TOOLCHAIN/CONFIG OS X
        ]),
)

filegroup(
    name = "glfw_src_textual",
    srcs = glob(["src/**/*.m", "src/**/*.in"]),
)

filegroup(
    name = "glfw_source_files",
    srcs = [":glfw_deps", ":glfw_src"]
)

filegroup(
    name = "glfw_tests",
    srcs = glob(["tests/*.c"]),
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
    includes = ["include"],
    include_prefix = "GLFW",
    visibility = ["//visibility:public"],
    deps = [
        "//deps",
        "//deps/vulkan",
        #"//deps/vs2008", #TODO enable for windows with TOOLCHAIN
        "//deps/mingw",
        "//deps/glad",
        "//deps/KHR",
    ]
)

cc_test(
    name = "glfw_test",
    srcs = [":glfw_tests"],
    deps = [
        ":glfw",
    ],
)
