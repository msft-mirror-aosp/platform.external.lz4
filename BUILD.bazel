load("@rules_license//rules:license.bzl", "license")
load("@rules_license//rules:license_kind.bzl", "license_kind")

package(
    default_applicable_licenses = [":license"],
    default_visibility = ["//visibility:public"],
)

license(
    name = "license",
    license_kinds = [
        ":SPDX-license-identifier-BSD-2.0",
     ],
    license_text = "lib/LICENSE",
    visibility = [":__subpackages__"],
)

license_kind(
    name = "SPDX-license-identifier-BSD-2.0",
    conditions = ["notice"],
    url = "https://spdx.org/licenses/BSD-2-Clause.html",
)

cc_library(
    name = "lz4",
    srcs = glob(["lib/*.c"]),
    hdrs = glob([
        "lib/*.h",
    ]) + ["lib/lz4.c"],
    copts = [
        "-O3",
        "-fno-delete-null-pointer-checks",
    ],
    includes = ["lib"],
    licenses = ["LICENSE"],
    visibility = ["//visibility:public"],
)
