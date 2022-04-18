load("@rules_cc//cc:defs.bzl", "cc_library")

licenses(["notice"])  # Apache 2

cc_library(
    name = "libcircllhist",
    srcs = ["src/circllhist.c"],
    hdrs = [
        "src/circllhist.h",
    ],
    copts = select({
        "@envoy//bazel:windows_x86_64": ["-DWIN32"],
        "@envoy//bazel:windows_x86_32": ["-DWIN32"],
        "//conditions:default": [],
    }),
    includes = ["src"],
    visibility = ["//visibility:public"],
)
