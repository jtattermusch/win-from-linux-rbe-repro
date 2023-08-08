# Repro

Shows how run a test on Windows RBE cluster from a linux workstation.

```
# uses bazel with some platform handling patches
/google/data/rw/users/tj/tjgq/bazel-with-win-exec-platform-fixes --bazelrc=tools/remote_build/windows.bazelrc test :all
```

# Contents

* `third_party/toolchains`: RBE toolchains as used by the github.com/grpc/grpc repository

* `tools/remote_build`: RBE configuration as used by the github.com/grpc/grpc repository (possibly with some minor tweaks for the purposes of this repro)
The RBE instance being used is only accessible to gRPC team members (You need to change the configuration to point to an RBE instance you have access to).
