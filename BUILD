
sh_test(
    name = "win_from_linux_sh_test",
    srcs = [
        "win_from_linux.sh",
    ],
    exec_properties = {
        "dockerNetwork": "standard",
        "label:machine_size": "small",  # needed to override the default value of "small".
        "label:os": "windows_2019",  # needed to override the default value of "small".
        "container-image": "docker://gcr.io/grpc-testing/rbe_windows2019@sha256:41772e8eeb9dd8c8b996bf32d58164d84b2315c8e81e634bbff5a0216b7f52fd",
        "OSFamily": "Windows",
    },
)

genrule(
    name = "win_from_linux_genrule",
    srcs = ["win_from_linux.sh"],
    outs = ["file1.txt"],
    cmd = "echo 'hello world'; uname -sm; touch $(location file1.txt)",
    exec_properties = {
        "dockerNetwork": "standard",
        "label:machine_size": "small",  # needed to override the default value of "small".
        "label:os": "windows_2019",  # needed to override the default value of "small".
        "container-image": "docker://gcr.io/grpc-testing/rbe_windows2019@sha256:41772e8eeb9dd8c8b996bf32d58164d84b2315c8e81e634bbff5a0216b7f52fd",
        "OSFamily": "Windows",
    },
)
