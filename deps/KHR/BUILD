package(
    default_visibility = ["//:__subpackages__"],
)

filegroup(
    name = "KHR_h",
    srcs = glob(["*.h"]),
)

cc_library(
    name = "KHR",
    hdrs = [":KHR_h"],
    includes = ["."],
)
