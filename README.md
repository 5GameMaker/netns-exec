# netns-exec

No, not the actual [netns-exec](https://github.com/pekman/netns-exec). This is an
execve version for if `netns-exec` does not compile.

This exposes running `ip netns exec` with root permissions, so if that is a
signifficant security risk, do not use this.

This project is licensed under [0-Clause BSD license]() because this thing's
so trivial copyrighting something like this is outrageous. Do whatever you
want.

## Requirements

- `sudo`
- `env`
- `iproute2`

## Installing

Do `./tinybuild`. On most systems this should be enough to produce a functional
binary.

Copy `build/netns-exec` to `/bin` and apply suid to it via `# chmod u+s /bin`.

## Usage

`$ netns-exec [NAMESPACE] [COMMAND..]`

No, there won't be a network namespaces tutorial. I just learned them myself
yesterday.
