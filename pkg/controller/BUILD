package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "client_builder.go",
        "controller_ref_manager.go",
        "controller_utils.go",
        "doc.go",
        "lookup_cache.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/api/validation:go_default_library",
        "//pkg/apis/extensions/v1beta1:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/client/clientset_generated/clientset/typed/core/v1:go_default_library",
        "//pkg/serviceaccount:go_default_library",
        "//pkg/util/hash:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:github.com/golang/groupcache/lru",
        "//vendor:k8s.io/apimachinery/pkg/api/errors",
        "//vendor:k8s.io/apimachinery/pkg/api/meta",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/fields",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
        "//vendor:k8s.io/apimachinery/pkg/types",
        "//vendor:k8s.io/apimachinery/pkg/util/sets",
        "//vendor:k8s.io/apimachinery/pkg/watch",
        "//vendor:k8s.io/apiserver/pkg/authentication/serviceaccount",
        "//vendor:k8s.io/client-go/kubernetes",
        "//vendor:k8s.io/client-go/rest",
        "//vendor:k8s.io/client-go/tools/cache",
        "//vendor:k8s.io/client-go/tools/record",
        "//vendor:k8s.io/client-go/util/clock",
        "//vendor:k8s.io/client-go/util/integer",
    ],
)

go_test(
    name = "go_default_test",
    srcs = ["controller_utils_test.go"],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/api:go_default_library",
        "//pkg/api/testapi:go_default_library",
        "//pkg/api/v1:go_default_library",
        "//pkg/client/clientset_generated/clientset:go_default_library",
        "//pkg/securitycontext:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/api/equality",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/sets",
        "//vendor:k8s.io/apimachinery/pkg/util/uuid",
        "//vendor:k8s.io/client-go/rest",
        "//vendor:k8s.io/client-go/tools/cache",
        "//vendor:k8s.io/client-go/tools/record",
        "//vendor:k8s.io/client-go/util/clock",
        "//vendor:k8s.io/client-go/util/testing",
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
        "//pkg/controller/certificates:all-srcs",
        "//pkg/controller/cloud:all-srcs",
        "//pkg/controller/cronjob:all-srcs",
        "//pkg/controller/daemon:all-srcs",
        "//pkg/controller/deployment:all-srcs",
        "//pkg/controller/disruption:all-srcs",
        "//pkg/controller/endpoint:all-srcs",
        "//pkg/controller/garbagecollector:all-srcs",
        "//pkg/controller/informers:all-srcs",
        "//pkg/controller/job:all-srcs",
        "//pkg/controller/namespace:all-srcs",
        "//pkg/controller/node:all-srcs",
        "//pkg/controller/podautoscaler:all-srcs",
        "//pkg/controller/podgc:all-srcs",
        "//pkg/controller/replicaset:all-srcs",
        "//pkg/controller/replication:all-srcs",
        "//pkg/controller/resourcequota:all-srcs",
        "//pkg/controller/route:all-srcs",
        "//pkg/controller/service:all-srcs",
        "//pkg/controller/serviceaccount:all-srcs",
        "//pkg/controller/statefulset:all-srcs",
        "//pkg/controller/ttl:all-srcs",
        "//pkg/controller/volume/attachdetach:all-srcs",
        "//pkg/controller/volume/persistentvolume:all-srcs",
    ],
    tags = ["automanaged"],
)
