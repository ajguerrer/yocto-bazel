load("@rules_pkg//:pkg.bzl", "pkg_tar")

pkg_tar(
    name = "poky",
    package_dir = "poky",
    strip_prefix = ".",
    extension = "tar.gz",
    srcs = glob(["**/*"]),
    visibility = ["//visibility:public"],
)
