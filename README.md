# Repro

Shows how run a test on Windows RBE cluster from a linux workstation.


Running sh_test will fail:
```
# uses bazel with some platform handling patches
/google/data/rw/users/tj/tjgq/bazel-with-win-exec-platform-fixes --bazelrc=tools/remote_build/windows.bazelrc test :win_from_linux_sh_test
```
Example failure: https://source.cloud.google.com/results/invocations/7ec72506-e146-4e2e-88a7-1052e8db0356


Running genrule works:
```
/google/data/rw/users/tj/tjgq/bazel-with-win-exec-platform-fixes --bazelrc=tools/remote_build/windows.bazelrc test :win_from_linux_genrule
```
Example run: https://source.cloud.google.com/results/invocations/f00443b3-204b-4cce-bb3f-b65c3ef3b438

# Contents

* `third_party/toolchains`: RBE toolchains as used by the github.com/grpc/grpc repository

* `tools/remote_build`: RBE configuration as used by the github.com/grpc/grpc repository (possibly with some minor tweaks for the purposes of this repro)
The RBE instance being used is only accessible to gRPC team members (You need to change the configuration to point to an RBE instance you have access to).
