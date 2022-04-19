workspace(name = "envoy")

load("//bazel:api_binding.bzl", "envoy_api_binding")

envoy_api_binding()

load("//bazel:api_repositories.bzl", "envoy_api_dependencies")

envoy_api_dependencies()

load("//bazel:repositories.bzl", "envoy_dependencies")

envoy_dependencies()

load("//bazel:repositories_extra.bzl", "envoy_dependencies_extra")

envoy_dependencies_extra()

load("//bazel:dependency_imports.bzl", "envoy_dependency_imports")

envoy_dependency_imports()

http_archive(
    name = "standalone_cc_toolchain",
    urls = ["https://github.com/meteorcloudy/windows-crosstool/archive/1e717be66497e114ea80296e5ad0485fb468bb25.zip"],
    strip_prefix = "windows-crosstool-1e717be66497e114ea80296e5ad0485fb468bb25",
)

load("@standalone_cc_toolchain//:cc_configure.bzl", "cc_configure")

cc_configure()
