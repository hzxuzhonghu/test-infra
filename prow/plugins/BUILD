package(default_visibility = ["//visibility:public"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_test(
    name = "go_default_test",
    srcs = [
        "plugins_test.go",
        "respond_test.go",
    ],
    embed = [":go_default_library"],
    importpath = "k8s.io/test-infra/prow/plugins",
    deps = ["//prow/github:go_default_library"],
)

go_library(
    name = "go_default_library",
    srcs = [
        "plugins.go",
        "respond.go",
    ],
    importpath = "k8s.io/test-infra/prow/plugins",
    deps = [
        "//prow/commentpruner:go_default_library",
        "//prow/config:go_default_library",
        "//prow/git:go_default_library",
        "//prow/github:go_default_library",
        "//prow/kube:go_default_library",
        "//prow/pluginhelp:go_default_library",
        "//prow/repoowners:go_default_library",
        "//prow/slack:go_default_library",
        "//vendor/github.com/ghodss/yaml:go_default_library",
        "//vendor/github.com/sirupsen/logrus:go_default_library",
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
        "//prow/plugins/approve:all-srcs",
        "//prow/plugins/assign:all-srcs",
        "//prow/plugins/blockade:all-srcs",
        "//prow/plugins/blunderbuss:all-srcs",
        "//prow/plugins/cat:all-srcs",
        "//prow/plugins/cla:all-srcs",
        "//prow/plugins/docs-no-retest:all-srcs",
        "//prow/plugins/dog:all-srcs",
        "//prow/plugins/golint:all-srcs",
        "//prow/plugins/heart:all-srcs",
        "//prow/plugins/help:all-srcs",
        "//prow/plugins/hold:all-srcs",
        "//prow/plugins/label:all-srcs",
        "//prow/plugins/lgtm:all-srcs",
        "//prow/plugins/lifecycle:all-srcs",
        "//prow/plugins/milestonestatus:all-srcs",
        "//prow/plugins/releasenote:all-srcs",
        "//prow/plugins/requiresig:all-srcs",
        "//prow/plugins/shrug:all-srcs",
        "//prow/plugins/sigmention:all-srcs",
        "//prow/plugins/size:all-srcs",
        "//prow/plugins/skip:all-srcs",
        "//prow/plugins/slackevents:all-srcs",
        "//prow/plugins/trigger:all-srcs",
        "//prow/plugins/updateconfig:all-srcs",
        "//prow/plugins/wip:all-srcs",
        "//prow/plugins/yuks:all-srcs",
    ],
    tags = ["automanaged"],
)
