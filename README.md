# gitfs-bazel
Efficient combination of [bazel](https://bazel.build/) and git [FUSE](https://www.kernel.org/doc/html/latest/filesystems/fuse.html) for large monorepos.

Our File System in User Space (FUSE) allows you to work only with a subset of git monorepo that you are interested in.
Only the files that you opened or edited are materialized on the filesystem. Reduce the checkout time from minutes to seconds.

The second piece that makes the build work efficiently is integration with bazel [remote build execution](https://bazel.build/docs/remote-execution).
Offload the expensive build task to the remote build cluster and get blazingly fast builds on a lean client.

Keep your developers happy and efficient.

This project is inspired by internal Google SourceFS project.
