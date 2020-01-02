load("@rules_pkg//:pkg.bzl", "pkg_tar")

pkg_tar(
    name = "meta-intel",
    package_dir = "meta-intel",
    strip_prefix = ".",
    extension = "tar.gz",
    srcs = glob(["**/*"]),
    visibility = ["//visibility:public"],
)
