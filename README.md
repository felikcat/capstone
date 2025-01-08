[![CI](https://github.com/allyourcodebase/capstone/actions/workflows/ci.yaml/badge.svg)](https://github.com/allyourcodebase/capstone/actions)

# capstone

This is [capstone](https://github.com/capstone-engine/capstone), packaged for [Zig](https://ziglang.org/).

This fork requires at least Zig 0.14.0-dev.2627+6a21d18ad.

## Installation

First, update your `build.zig.zon`:

```
# Initialize a `zig build` project if you haven't already
zig init
zig fetch --save git+https://github.com/felikcat/capstone.git#5.0.3
```

You can then import `capstone` in your `build.zig` with:

```zig
const capstone_dependency = b.dependency("capstone", .{
    .target = target,
    .optimize = optimize,
});
your_exe.linkLibrary(capstone_dependency.artifact("capstone"));
```
