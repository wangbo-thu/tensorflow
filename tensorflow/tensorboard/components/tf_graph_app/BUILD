package(default_visibility = ["//tensorflow:internal"])

load("//tensorflow/tensorboard:defs.bzl", "tensorboard_webcomponent_library")
load("//tensorflow/tensorboard:web.bzl", "ts_web_library")

licenses(["notice"])  # Apache 2.0

ts_web_library(
    name = "tf_graph_app",
    srcs = [
        "index.html",
        "tf-graph-app.html",
    ],
    path = "/tf-graph-app",
    deps = [
        "//tensorflow/tensorboard/components/tf_graph_board",
        "//tensorflow/tensorboard/components/tf_graph_controls",
        "//tensorflow/tensorboard/components/tf_graph_loader",
        "//tensorflow/tensorboard/components/tf_imports:polymer",
        "//tensorflow/tensorboard/components/tf_imports:webcomponentsjs",
        "@org_polymer_iron_component_page",
    ],
)

tensorboard_webcomponent_library(
    name = "legacy",
    srcs = [":tf_graph_app"],
    destdir = "tf-graph-app",
    deps = [
        "//tensorflow/tensorboard/components/tf_graph_board:legacy",
        "//tensorflow/tensorboard/components/tf_graph_controls:legacy",
        "//tensorflow/tensorboard/components/tf_graph_loader:legacy",
        "//third_party/javascript/polymer/v1/iron-component-page:lib",
        "//third_party/javascript/polymer/v1/polymer:lib",
        "//third_party/javascript/polymer/v1/webcomponentsjs:lib",
    ],
)

filegroup(
    name = "all_files",
    srcs = glob(["**"]),
    tags = ["notsan"],
)
