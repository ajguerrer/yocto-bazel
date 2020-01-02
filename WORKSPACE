load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "rules_pkg",
    url = "https://github.com/bazelbuild/rules_pkg/releases/download/0.2.4/rules_pkg-0.2.4.tar.gz",
    sha256 = "4ba8f4ab0ff85f2484287ab06c0d871dcb31cc54d439457d28fd4ae14b18450a",
)

http_archive(
    name = "io_bazel_rules_docker",
    sha256 = "df13123c44b4a4ff2c2f337b906763879d94871d16411bf82dcfeba892b58607",
    strip_prefix = "rules_docker-0.13.0",
    urls = ["https://github.com/bazelbuild/rules_docker/releases/download/v0.13.0/rules_docker-v0.13.0.tar.gz"],
)

load(
    "@io_bazel_rules_docker//repositories:repositories.bzl",
    container_repositories = "repositories",
)

container_repositories()

load(
    "@io_bazel_rules_docker//repositories:go_repositories.bzl",
    container_go_deps = "go_deps",
)

container_go_deps()

load("@io_bazel_rules_docker//container:pull.bzl", "container_pull")

container_pull(
    name = "ubuntu1804",
    registry = "docker.io",
    repository = "ubuntu:18.04",
    digest = "sha256:2695d3e10e69cc500a16eae6d6629c803c43ab075fa5ce60813a0fc49c47e859",
)

http_archive(
    name = "poky",
    strip_prefix = "poky-sumo-19.0.3",
    urls = ["https://downloads.yoctoproject.org/releases/yocto/yocto-2.5.3/poky-sumo-19.0.3.tar.bz2"],
    build_file = "@//:pocky.BUILD",
    sha256 = "5fa9dc96d3c96a3e3a4f42e2945e39a0fe64cbc55b500e52601210d12976c61a",
)

http_archive(
    name = "meta_intel",
    strip_prefix = "meta-intel-sumo-19.0.3",
    urls = ["https://downloads.yoctoproject.org/releases/yocto/yocto-2.5.3/meta-intel-sumo-19.0.3.tar.bz2"],
    build_file = "@//:meta_intel.BUILD",
    sha256 = "d91bd4d3e6c30155bce724e02353bccececcf19a2362e5cf7aea42ea27f60867",
)
