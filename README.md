# OPAM - A package manager for OCaml

OPAM is a source-based package manager for OCaml. It supports multiple simultaneous
compiler installations, flexible package constraints, and a Git-friendly development
workflow.

OPAM is created and maintained by [OCamlPro](http://www.ocamlpro.com).

To get started, checkout the [Quick
Install](http://opam.ocaml.org/doc/Quick_Install.html) guide.

## Compiling this repo

* Make sure you have OCaml and GNU make installed.
* Run `./configure`
* Run `make lib-ext` as advertised by `./configure` if you don't have the
  dependencies installed and only need the opam binary (not the libs). This will
  locally take care of all OCaml dependencies for you.
* Otherwise, make sure to have ocamlfind, ocamlgraph, cmdliner, jsonm, cudf,
  dose 3.2.2+opam and re >= 1.2.0 installed. Or run `opam install
  opam-lib --deps-only` if you already have a working instance. Re-run
  `./configure` once done.
* Run `make`
* Run `make install`
* Run `make libinstall` if needed (this is incompatible with `make lib-ext`, as
  the opam library would conflict with installed versions of the dependencies)

## Bug tracker

Have a bug or a feature request ? Please open an issue on [our
bug-tracker](https://github.com/ocaml/opam/issues). Please search for existing
issues before posting, and include the output of `opam config report` and any
details that may help track down the issue.

## Documentation

#### User Manual

The main documentation entry point to OPAM is the user manual,
available using `opam --help`. To get help for a specific command, use
`opam <command> --help`.

#### Tutorials

A collection of tutorials are available online at <http://opam.ocaml.org>.
These tutorials are automatically generated from the
[wiki](https://github.com/ocaml/opam/wiki/_pages) and
are also available in PDF format in the `doc/tutorials` directory.

#### API, Code Documentation and Developer Manual

A more torough technical document describing OPAM and specifying the package
description format is available in the
[doc/dev-manual](https://raw.github.com/ocaml/opam/blob/doc/dev-manual/dev-manual.pdf).
`make doc` will otherwise make the API documentation available under `doc/`.

## Community

Keep track of development and community news.

* Have a question that's not a feature request or bug report?
  [Ask on the mailing list](http://lists.ocaml.org/listinfo/infrastructure).

* Chat with fellow OPAMers on IRC. On the `irc.freenode.net` server,
  in the `#ocaml` or the `#opam` channel.

## Contributing

We welcome contributions ! Please use Github's pull-request mechanism against
the master branch of the [OPAM repository](https://github.com/ocaml/opam). If
that's not an option for you, you can use `git format-patch` and email TODO.

## Versioning

The release cycle respects [Semantic Versioning](http://semver.org/).

### Related repositories

- [ocaml/opam-repository](https://github.com/ocaml/opam-repository) is the official repository for OPAM packages and compilers. A number of non-official repositories are also available on the interwebs, for instance on [Github](https://github.com/search?q=opam-repo&type=Repositories).
- [opam2web](https://github.com/ocaml/opam2web) generates a collection of browsable HTML files for a given repository. It is used to generate http://opam.ocaml.org.
- [opam-rt](https://github.com/ocaml/opam-rt) is the regression framework for OPAM.
- [opamlot](https://github.com/ocamllabs/ocamlot) is the automated QA environment for OPAM. 

## Copyright and license

Copyright 2012-2014 OCamlPro  
Copyright 2012 INRIA

All rights reserved. OPAM is distributed under the terms of
the GNU Lesser General Public License version 3.0.

OPAM is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

