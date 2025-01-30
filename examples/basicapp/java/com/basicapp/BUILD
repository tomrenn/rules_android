load("@rules_android//android:rules.bzl", "android_binary", "android_library", "android_local_test")

android_binary(
    name = "basic_app",
    manifest = "AndroidManifest.xml",
    deps = [":basic_lib"],
)

android_local_test(
    name = "app-test",
    srcs = ["BasicActivityTest.java"],
    test_class = "foo.BasicActivityTest",
    deps = [
        "@maven//:org_robolectric_robolectric",
        "@maven//:junit_junit",
    ],
)

android_library(
    name = "basic_lib",
    srcs = ["BasicActivity.java"],
    javacopts = ["-source 11 -target 11"],
    manifest = "AndroidManifest.xml",
    resource_files = glob(["res/**"]),
)
