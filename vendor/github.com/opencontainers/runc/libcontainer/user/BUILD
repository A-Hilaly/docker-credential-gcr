load("@io_bazel_rules_go//go:def.bzl", "go_library")

go_library(
    name = "go_default_library",
    srcs = [
        "lookup.go",
        "user.go",
    ] + select({
        "@io_bazel_rules_go//go/platform:android": [
            "lookup_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:darwin": [
            "lookup_unix.go",
        ],
        "@io_bazel_rules_go//go/platform:dragonfly": [
            "lookup_unix.go",
        ],
        "@io_bazel_rules_go//go/platform:freebsd": [
            "lookup_unix.go",
        ],
        "@io_bazel_rules_go//go/platform:linux": [
            "lookup_unix.go",
        ],
        "@io_bazel_rules_go//go/platform:nacl": [
            "lookup_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:netbsd": [
            "lookup_unix.go",
        ],
        "@io_bazel_rules_go//go/platform:openbsd": [
            "lookup_unix.go",
        ],
        "@io_bazel_rules_go//go/platform:plan9": [
            "lookup_unsupported.go",
        ],
        "@io_bazel_rules_go//go/platform:solaris": [
            "lookup_unix.go",
        ],
        "@io_bazel_rules_go//go/platform:windows": [
            "lookup_unsupported.go",
        ],
        "//conditions:default": [],
    }),
    importpath = "github.com/opencontainers/runc/libcontainer/user",
    visibility = ["//visibility:public"],
)
