package_group(
    name = "default_visibility",
    includes = ["//tensorflow_federated/python/core:core_visibility"],
    packages = [
        # Subpackages
        "//tensorflow_federated/python/core/backends/native/...",
    ],
)

package(default_visibility = [":default_visibility"])

licenses(["notice"])

py_library(
    name = "native",
    srcs = ["__init__.py"],
    srcs_version = "PY3",
    visibility = ["//tensorflow_federated/python/core/backends:__pkg__"],
    deps = [
        ":compiler",
        ":execution_contexts",
    ],
)

py_library(
    name = "compiler",
    srcs = ["compiler.py"],
    srcs_version = "PY3",
    deps = [
        "//tensorflow_federated/python/core/api:computation_base",
        "//tensorflow_federated/python/core/impl:do_not_use_compiler",
    ],
)

py_library(
    name = "execution_contexts",
    srcs = ["execution_contexts.py"],
    srcs_version = "PY3",
    deps = [
        ":compiler",
        "//tensorflow_federated/python/core/impl/context_stack:context_stack_impl",
        "//tensorflow_federated/python/core/impl/executors:execution_context",
        "//tensorflow_federated/python/core/impl/executors:executor_stacks",
    ],
)
