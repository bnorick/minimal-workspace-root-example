# minimal-workspace-root-example

It works, yay.
```sh
/opensource/minimal-workspace-root-example$ /opensource/rye/target/debug/rye --version
rye 0.33.0
commit: 0.32.0+2 (3bfb83932 2024-04-18)
platform: linux (x86_64)
self-python: cpython@3.12.2
symlink support: true
uv enabled: true

/opensource/minimal-workspace-root-example$ pushd project0 && /opensource/rye/target/debug/rye sync && popd
[...]
Done!

/opensource/minimal-workspace-root-example$ pushd project1 && /opensource/rye/target/debug/rye sync && popd
[...]
Done!

/opensource/minimal-workspace-root-example$ pushd project2 && /opensource/rye/target/debug/rye sync && popd
[...]
Done!

/opensource/minimal-workspace-root-example$ pushd project1 && python -c "import project0; print(project0.hello())"; popd
/opensource/minimal-workspace-root-example/project1 /opensource/minimal-workspace-root-example /opensource/minimal-workspace-root-example
Hello from project0!
/opensource/minimal-workspace-root-example /opensource/minimal-workspace-root-example
```