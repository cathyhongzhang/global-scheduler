package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
)

go_library(
    name = "go_default_library",
    srcs = [
        "apps_client.go",
        "controllerrevision.go",
        "daemonset.go",
        "deployment.go",
        "doc.go",
        "generated_expansion.go",
        "replicaset.go",
        "statefulset.go",
    ],
    importmap = "k8s.io/kubernetes/vendor/k8s.io/client-go/kubernetes/typed/apps/v1beta2",
    importpath = "k8s.io/client-go/kubernetes/typed/apps/v1beta2",
    deps = [
        "//staging/src/k8s.io/api/apps/v1beta2:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/api/errors:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/apis/meta/v1:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/types:go_default_library",
        "//staging/src/k8s.io/apimachinery/pkg/watch:go_default_library",
        "//staging/src/k8s.io/client-go/apiserverupdate:go_default_library",
        "//staging/src/k8s.io/client-go/kubernetes/scheme:go_default_library",
        "//staging/src/k8s.io/client-go/rest:go_default_library",
        "//vendor/k8s.io/klog:go_default_library",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [
        ":package-srcs",
        "//staging/src/k8s.io/client-go/kubernetes/typed/apps/v1beta2/fake:all-srcs",
    ],
    tags = ["automanaged"],
)
