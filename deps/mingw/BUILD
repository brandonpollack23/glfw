package(
    default_visibility = ["//:__subpackages__"],
)

filegroup(
    name = "mingw_h",
    srcs = glob(["*.h"]),
)

cc_library(
    name = "mingw",
    hdrs = [":mingw_h"],
    includes = ["."],
)
