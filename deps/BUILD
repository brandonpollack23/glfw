package(
    default_visibility = ["//:__subpackages__"],
)

filegroup(
    name = "top_level_dep_h",
    srcs = glob(["*.h"]),
)

filegroup(
    name = "top_level_dep_src",
    srcs = glob(["*.c"]),
)

cc_library(
    name = "deps",
    srcs = [":top_level_dep_src"] + [":top_level_dep_h"],
    hdrs = [":top_level_dep_h"],
    includes = ["."],
    deps = [
        "//deps/glad"
    ]
)
