package(
    default_testonly = 1,
    default_visibility = ["//java/google/registry:registry_project"],
)

licenses(["notice"])  # Apache 2.0

load("//java/com/google/testing/builddefs:GenTestRules.bzl", "GenTestRules")

java_library(
    name = "batch",
    srcs = glob(["*.java"]),
    deps = [
        "//java/google/registry/batch",
        "//java/google/registry/bigquery",
        "//java/google/registry/flows",
        "//java/google/registry/mapreduce",
        "//java/google/registry/model",
        "//java/google/registry/util",
        "//javatests/google/registry/testing",
        "//javatests/google/registry/testing/mapreduce",
        "//third_party/objectify:objectify-v4_1",
        "@com_google_apis_google_api_services_bigquery",
        "@com_google_appengine_api_1_0_sdk//:testonly",
        "@com_google_appengine_api_stubs",
        "@com_google_appengine_tools_appengine_gcs_client",
        "@com_google_appengine_tools_appengine_mapreduce",
        "@com_google_appengine_tools_appengine_pipeline",
        "@com_google_code_findbugs_jsr305",
        "@com_google_dagger",
        "@com_google_guava",
        "@com_google_http_client",
        "@com_google_re2j",
        "@com_google_truth",
        "@com_google_truth_extensions_truth_java8_extension",
        "@javax_servlet_api",
        "@joda_time",
        "@junit",
        "@org_joda_money",
        "@org_mockito_all",
    ],
)

GenTestRules(
    name = "GeneratedTestRules",
    default_test_size = "large",
    test_files = glob(["*Test.java"]),
    deps = [":batch"],
)
