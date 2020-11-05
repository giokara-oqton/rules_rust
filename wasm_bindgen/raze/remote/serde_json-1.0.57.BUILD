"""
@generated
cargo-raze crate build file.

DO NOT EDIT! Replaced on runs of cargo-raze
"""

# buildifier: disable=load
load(
    "@io_bazel_rules_rust//rust:rust.bzl",
    "rust_binary",
    "rust_library",
    "rust_test",
)

# buildifier: disable=load
load("@bazel_skylib//lib:selects.bzl", "selects")

package(default_visibility = [
    # Public for visibility by "@raze__crate__version//" targets.
    #
    # Prefer access through "//wasm_bindgen/raze", which limits external
    # visibility to explicit Cargo.toml dependencies.
    "//visibility:public",
])

licenses([
    "notice",  # MIT from expression "MIT OR Apache-2.0"
])

# Generated targets
# buildifier: disable=load-on-top
load(
    "@io_bazel_rules_rust//cargo:cargo_build_script.bzl",
    "cargo_build_script",
)

# buildifier: leave-alone
cargo_build_script(
    name = "serde_json_build_script",
    srcs = glob(["**/*.rs"]),
    crate_root = "build.rs",
    edition = "2018",
    deps = [
    ],
    rustc_flags = [
        "--cap-lints=allow",
    ],
    crate_features = [
      "default",
      "std",
    ],
    build_script_env = {
    },
    data = glob(["**"]),
    tags = [
        "cargo-raze",
        "manual",
    ],
    version = "1.0.57",
    visibility = ["//visibility:private"],
)


# buildifier: leave-alone
rust_library(
    name = "serde_json",
    crate_type = "lib",
    deps = [
        ":serde_json_build_script",
        "@rules_rust_wasm_bindgen__itoa__0_4_6//:itoa",
        "@rules_rust_wasm_bindgen__ryu__1_0_5//:ryu",
        "@rules_rust_wasm_bindgen__serde__1_0_115//:serde",
    ],
    srcs = glob(["**/*.rs"]),
    crate_root = "src/lib.rs",
    edition = "2018",
    rustc_flags = [
        "--cap-lints=allow",
    ],
    version = "1.0.57",
    tags = [
        "cargo-raze",
        "manual",
    ],
    crate_features = [
        "default",
        "std",
    ],
)