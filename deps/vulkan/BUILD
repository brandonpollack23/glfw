package(
    default_visibility = ["//:__subpackages__"],
)

filegroup(
    name = "vulkan_h",
    srcs = glob(["*.h"]),
)

cc_library(
    name = "vulkan",
    hdrs = [":vulkan_h"],
    includes = ["."],
)

