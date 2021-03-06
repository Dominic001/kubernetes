package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_binary",
    "go_library",
    "go_test",
    "cgo_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "deployment_controller.go",
        "recreate.go",
        "rollback.go",
        "rolling.go",
        "sync.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/errors:go_default_library",
        "//pkg/api/unversioned:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/client/cache:go_default_library",
        "//pkg/client/clientset_generated/internalclientset:go_default_library",
        "//pkg/client/clientset_generated/internalclientset/typed/core/unversioned:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/client/retry:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/controller/deployment/util:go_default_library",
        "//pkg/controller/informers:go_default_library",
        "//pkg/labels:go_default_library",
        "//pkg/util/errors:go_default_library",
        "//pkg/util/integer:go_default_library",
        "//pkg/util/labels:go_default_library",
        "//pkg/util/metrics:go_default_library",
        "//pkg/util/pod:go_default_library",
        "//pkg/util/replicaset:go_default_library",
        "//pkg/util/runtime:go_default_library",
        "//pkg/util/wait:go_default_library",
        "//pkg/util/workqueue:go_default_library",
        "//vendor:github.com/golang/glog",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "deployment_controller_test.go",
        "rolling_test.go",
        "sync_test.go",
    ],
    library = "go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/unversioned:go_default_library",
        "//pkg/apimachinery/registered:go_default_library",
        "//pkg/apis/extensions:go_default_library",
        "//pkg/client/clientset_generated/internalclientset/fake:go_default_library",
        "//pkg/client/record:go_default_library",
        "//pkg/client/testing/core:go_default_library",
        "//pkg/controller:go_default_library",
        "//pkg/controller/deployment/util:go_default_library",
        "//pkg/controller/informers:go_default_library",
        "//pkg/runtime:go_default_library",
        "//pkg/util/intstr:go_default_library",
        "//pkg/util/uuid:go_default_library",
    ],
)
