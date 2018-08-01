package(
    default_visibility = ["//:__subpackages__"],
)

filegroup(
    name = "vs_h",
    srcs = glob(["*.h"]),
)

cc_library(
    name = "vs2008",
    hdrs = [":vs_h"],
    includes = ["."],
)

