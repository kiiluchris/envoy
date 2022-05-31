load(":cc_toolchain_config.bzl", "cc_toolchain_config")

package(default_visibility = ["//visibility:public"])


filegroup(
    name = "empty",
)

filegroup(
    name = "clangcl_compiler_files",
    srcs = [":builtin_include_directory_paths_clangcl"]
)

filegroup(
    name = "msvc_compiler_files",
    srcs = [":builtin_include_directory_paths_msvc"]
)


cc_toolchain_suite(
    name = "clang_suite",
    toolchains = {
        "x64_x86_windows": ":cc-compiler-x86_windows",
        "x64_x86_windows|msvc-cl": ":cc-compiler-x86_windows",
        "x64_x86_windows|clang-cl": ":cc-compiler-x64_x86_windows-clang-cl",
    },
)


cc_toolchain(
    name = "cc-compiler-x86_windows",
    all_files = ":empty",
    ar_files = ":empty",
    as_files = ":msvc_compiler_files",
    compiler_files = ":msvc_compiler_files",
    dwp_files = ":empty",
    linker_files = ":empty",
    objcopy_files = ":empty",
    strip_files = ":empty",
    supports_param_files = 1,
    toolchain_config = ":msvc_x86",
    toolchain_identifier = "msvc_x86",
)

cc_toolchain_config(
    name = "msvc_x86",
    abi_libc_version = "local",
    abi_version = "local",
    compiler = "msvc-cl",
    cpu = "x64_x86_windows",
    cxx_builtin_include_directories = [
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\include",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\ucrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\shared",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\um",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\winrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\cppwinrt",
    ],
    dbg_mode_debug_flag = "/DEBUG:FULL",
    default_link_flags = [
      "/MACHINE:X86",
      "/DWIN32",
    ],
    fastbuild_mode_debug_flag = "/DEBUG:FASTLINK",
    host_system_name = "local",
    msvc_cl_path = "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/cl.exe",
    msvc_env_include = ";".join([
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\include",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\ucrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\shared",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\um",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\winrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\cppwinrt",
    ]),
    msvc_env_lib = ";".join([
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\lib\\x86",
        "C:\\Program Files (x86)\\Windows Kits\\10\\lib\\10.0.18362.0\\ucrt\\x86",
        "C:\\Program Files (x86)\\Windows Kits\\10\\lib\\10.0.18362.0\\um\\x86",
    ]),
    msvc_env_path = ";".join([
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\bin\\HostX64\\x86",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\CommonExtensions\\Microsoft\\TestWindow",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\MSBuild\\Current\\bin\\Roslyn",
        "C:\\Program Files (x86)\\Windows Kits\\10\\bin\\10.0.18362.0\\x86",
        "C:\\Program Files (x86)\\Windows Kits\\10\\bin\\x86",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\\\MSBuild\\Current\\Bin",
        "C:\\Windows\\Microsoft.NET\\Framework64\\v4.0.30319",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\Tools\\C:\\Windows\\system32",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\CommonExtensions\\Microsoft\\CMake\\CMake\\bin",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\CommonExtensions\\Microsoft\\CMake\\Ninja",
    ]),
    msvc_env_tmp = "C:\\src\\temp",
    msvc_lib_path = "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/lib.exe",
    msvc_link_path = "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/link.exe",
    msvc_ml_path = "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/ml.exe",
    target_libc = "msvcrt",
    target_system_name = "local",
    tool_paths = {
        "ar": "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/lib.exe",
        "ml": "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/ml.exe",
        "cpp": "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/cl.exe",
        "gcc": "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/cl.exe",
        "gcov": "wrapper/bin/msvc_nop.bat",
        "ld": "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/link.exe",
        "nm": "wrapper/bin/msvc_nop.bat",
        "objcopy": "wrapper/bin/msvc_nop.bat",
        "objdump": "wrapper/bin/msvc_nop.bat",
        "strip": "wrapper/bin/msvc_nop.bat",
    },
    toolchain_identifier = "msvc_x86",
)

cc_toolchain(
    name = "cc-compiler-x64_x86_windows-clang-cl",
    all_files = ":empty",
    ar_files = ":empty",
    as_files = ":clangcl_compiler_files",
    compiler_files = ":clangcl_compiler_files",
    dwp_files = ":empty",
    linker_files = ":empty",
    objcopy_files = ":empty",
    strip_files = ":empty",
    supports_param_files = 1,
    toolchain_config = ":clang_cl_x64_x86",
    toolchain_identifier = "clang_cl_x64_x86",
)

cc_toolchain_config(
    name = "clang_cl_x64_x86",
    abi_libc_version = "local",
    abi_version = "local",
    compiler = "clang-cl",
    cpu = "x64_x86_windows",
    cxx_builtin_include_directories = [
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\include",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\ucrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\shared",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\um",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\winrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\cppwinrt",
        "C:\\LLVM\\lib\\clang\\9.0.1\\include",
    ],
    dbg_mode_debug_flag = "/DEBUG",
    default_link_flags = [
        "/MACHINE:X86",
        # "/DEFAULTLIB:clang_rt.builtins-x86_64.lib",
        "/DWIN32",
    ],
    fastbuild_mode_debug_flag = "/DEBUG",
    host_system_name = "local",
    msvc_cl_path = "C:/LLVM/bin/clang-cl.exe",
    msvc_env_include = ";".join([
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\include",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\ucrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\shared",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\um",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\winrt",
        "C:\\Program Files (x86)\\Windows Kits\\10\\include\\10.0.18362.0\\cppwinrt",
        "C:\\LLVM\\lib\\clang\\9.0.1\\include",
    ]),
    msvc_env_lib = ";".join([
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\lib\\x86",
        "C:\\Program Files (x86)\\Windows Kits\\10\\lib\\10.0.18362.0\\ucrt\\x86",
        "C:\\Program Files (x86)\\Windows Kits\\10\\lib\\10.0.18362.0\\um\\x86",
        "C:\\LLVM\\lib\\clang\\9.0.1\\lib\\windows",
    ]),
    msvc_env_path = ";".join([
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\VC\\Tools\\MSVC\\14.29.30133\\bin\\HostX64\\x86",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\CommonExtensions\\Microsoft\\TestWindow",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\MSBuild\\Current\\bin\\Roslyn",
        "C:\\Program Files (x86)\\Windows Kits\\10\\bin\\10.0.18362.0\\x86",
        "C:\\Program Files (x86)\\Windows Kits\\10\\bin\\x86",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\\\MSBuild\\Current\\Bin",
        "C:\\Windows\\Microsoft.NET\\Framework64\\v4.0.30319",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\Tools\\",
        "C:\\Windows\\system32",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\CommonExtensions\\Microsoft\\CMake\\CMake\\bin",
        "C:\\Program Files (x86)\\Microsoft Visual Studio\\2019\\BuildTools\\Common7\\IDE\\CommonExtensions\\Microsoft\\CMake\\Ninja",
    ]),
    msvc_env_tmp = "C:\\src\\temp",
    msvc_lib_path = "C:/LLVM/bin/llvm-lib.exe",
    msvc_link_path = "C:/LLVM/bin/lld-link.exe",
    msvc_ml_path = "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/ml.exe",
    target_libc = "msvcrt",
    target_system_name = "local",
    tool_paths = {
        "ar": "C:/LLVM/bin/llvm-lib.exe",
        "ml": "C:/Program Files (x86)/Microsoft Visual Studio/2019/BuildTools/VC/Tools/MSVC/14.29.30133/bin/HostX64/x86/ml.exe",
        "cpp": "C:/LLVM/bin/clang-cl.exe",
        "gcc": "C:/LLVM/bin/clang-cl.exe",
        "gcov": "wrapper/bin/msvc_nop.bat",
        "ld": "C:/LLVM/bin/lld-link.exe",
        "nm": "wrapper/bin/msvc_nop.bat",
        "objcopy": "wrapper/bin/msvc_nop.bat",
        "objdump": "wrapper/bin/msvc_nop.bat",
        "strip": "wrapper/bin/msvc_nop.bat",
    },
    toolchain_identifier = "clang_cl_x64_x86",
)
