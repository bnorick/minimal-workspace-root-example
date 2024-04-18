# minimal-workspace-root-example

It doesn't work, as expected.
```sh
/opensource/minimal-workspace-root-example$ rye --version
rye 0.32.0
commit: 0.32.0 (e1b4f2a29 2024-03-29)
platform: linux (x86_64)
self-python: cpython@3.12.2
symlink support: true
uv enabled: true

/opensource/minimal-workspace-root-example$ pushd project0 && rye sync && popd
[...]
Done!

/opensource/minimal-workspace-root-example$ pushd project1 && rye sync && popd
[...]
Done!

/opensource/minimal-workspace-root-example$ pushd project2 && rye sync && popd
[...]
Done!

/opensource/minimal-workspace-root-example$ pushd project1 && python -c "import project0; print(project0.hello())"; popd
/opensource/minimal-workspace-root-example/project1 /opensource/minimal-workspace-root-example
Traceback (most recent call last):
  File "<string>", line 1, in <module>
ModuleNotFoundError: No module named 'project0'
/opensource/minimal-workspace-root-example
```