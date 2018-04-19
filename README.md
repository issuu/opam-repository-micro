OPAM Repository Micro
=====================

Set of common libraries that are useful for all kinds of Issuu projects.

The idea of having small, versioned and composable libraries is to avoid
copy-pasting modules and diverging over time and also to avoid having a
monolithic [ocaml-common][common] submodule which is impossible to change as
every change might have unknown consequences upon all users when updating to a
never version of ocaml-common.

The libraries here should be as minimal as possible, with as little
dependencies as possible. In general at Issuu we tend to use the Jane Street
published libraries so these dependencies are okay, but one should strive to
use the smaller dependency if possible. In particular this means chosing [Base][base]
over Core_kernel over [Core][core], similarly with Async_kernel which is preferable to
[Async][async]. This is to allow for higher portability and fewer dependencies.

Usage
-----

You need to use OPAM (preferably OPAM 2, though version 1 will probably also
work for now) and then add this repository to your installation:

```sh
opam repository add micro https://github.com/issuu/opam-repository-micro.git
```

[common]: https://github.com/issuu/ocaml-common
[base]: https://opensource.janestreet.com/base/
[core]: https://opensource.janestreet.com/core/
[async]: https://opensource.janestreet.com/async/
