
# Workspace for Arm MCU GCC toolchain
workspace(name = "arm_none_eabi")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Arm Cortex-M4 == armv7e-m

# Apple Silicon host toolchain
# https://developer.arm.com/-/media/Files/downloads/gnu/12.3.rel1/binrel/arm-gnu-toolchain-12.3.rel1-darwin-arm64-arm-none-eabi.tar.xz
http_archive(
    name = "arm_gcc_darwin_arm64",
    urls = ["https://developer.arm.com/-/media/Files/downloads/gnu/12.3.rel1/binrel/arm-gnu-toolchain-12.3.rel1-darwin-arm64-arm-none-eabi.tar.xz"],
    strip_prefix = "arm-gnu-toolchain-12.3.rel1-darwin-arm64-arm-none-eabi",
    sha256 = "c22a1b092d0d401291232d21e24cf986cbb534daf3233e46a9c0bad1a3d68740",
    build_file = "//toolchain_arm_gcc/arm_gcc_darwin_arm64.BUILD",
)

# # Linux x86_64 host toolchain
# http_archive(
#     name = "arm64_gcc_linux_x86_64",
#     urls = ["https://developer.arm.com/-/media/Files/downloads/gnu/12.2.rel1/binrel/arm-gnu-toolchain-12.2.rel1-x86_64-aarch64-none-linux-gnu.tar.xz"],
#     strip_prefix = "arm-gnu-toolchain-12.2.rel1-x86_64-aarch64-none-linux-gnu",
#     sha256 = "6e8112dce0d4334d93bd3193815f16abe6a2dd5e7872697987a0b12308f876a4",
#     build_file = "//toolchain_arm64_gcc:arm64_gcc_linux_x86_64.BUILD",
# )

register_toolchains(
    "//toolchain_arm_gcc:arm_gcc_darwin_arm64",
)