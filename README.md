<div align="center">
  <h1><code>Queries Answering & CRUD Operations Using Python MongoDB</code></h1>

  <p>
    <strong>Task by 
    <a href="https://www.guvi.in/">GUVI - Greek Networks</a></strong>
  </p>

  <strong>A <a href="https://www.mongodb.com/docs/drivers/pymongo/">Pymongo</a> project</strong>
  <h3>
    <strong> A Simple
    <a href="https://www.mongodb.com/languages/python/pymongo-tutorial">Guide </a> by Mongodb.com</strong>
   
  </h3>
</div>

## Task-MongoDB
This is the code to Run MongoDB Server On Google Colaboratory and answering the Queries related to Available student.json Dataset from MongoDB.


## First Install " dnspython " and " pymongo server " in Google Colaboratory
```python
!apt install mongodb
!service mongodb start
```
Output:
```
Reading package lists... Done
Building dependency tree       
Reading state information... Done
The following package was automatically installed and is no longer required:
  libnvidia-common-460
Use 'apt autoremove' to remove it.
The following additional packages will be installed:
  libpcap0.8 libstemmer0d libyaml-cpp0.5v5 mongo-tools mongodb-clients
  mongodb-server mongodb-server-core
The following NEW packages will be installed:
  libpcap0.8 libstemmer0d libyaml-cpp0.5v5 mongo-tools mongodb mongodb-clients
  mongodb-server mongodb-server-core
0 upgraded, 8 newly installed, 0 to remove and 29 not upgraded.
Need to get 53.1 MB of archives.
After this operation, 215 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu bionic-updates/main amd64 libpcap0.8 amd64 1.8.1-6ubuntu1.18.04.2 [118 kB]
Get:2 http://archive.ubuntu.com/ubuntu bionic/main amd64 libstemmer0d amd64 0+svn585-1build1 [62.5 kB]
Get:3 http://archive.ubuntu.com/ubuntu bionic/universe amd64 libyaml-cpp0.5v5 amd64 0.5.2-4ubuntu1 [150 kB]
Get:4 http://archive.ubuntu.com/ubuntu bionic/universe amd64 mongo-tools amd64 3.6.3-0ubuntu1 [12.3 MB]
Get:5 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb-clients amd64 1:3.6.3-0ubuntu1.4 [20.2 MB]
Get:6 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb-server-core amd64 1:3.6.3-0ubuntu1.4 [20.3 MB]
Get:7 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb-server all 1:3.6.3-0ubuntu1.4 [12.6 kB]
Get:8 http://archive.ubuntu.com/ubuntu bionic-updates/universe amd64 mongodb amd64 1:3.6.3-0ubuntu1.4 [10.2 kB]
Fetched 53.1 MB in 1s (61.0 MB/s)
Selecting previously unselected package libpcap0.8:amd64.
(Reading database ... 123942 files and directories currently installed.)
Preparing to unpack .../0-libpcap0.8_1.8.1-6ubuntu1.18.04.2_amd64.deb ...
Unpacking libpcap0.8:amd64 (1.8.1-6ubuntu1.18.04.2) ...
Selecting previously unselected package libstemmer0d:amd64.
Preparing to unpack .../1-libstemmer0d_0+svn585-1build1_amd64.deb ...
Unpacking libstemmer0d:amd64 (0+svn585-1build1) ...
Selecting previously unselected package libyaml-cpp0.5v5:amd64.
Preparing to unpack .../2-libyaml-cpp0.5v5_0.5.2-4ubuntu1_amd64.deb ...
Unpacking libyaml-cpp0.5v5:amd64 (0.5.2-4ubuntu1) ...
Selecting previously unselected package mongo-tools.
Preparing to unpack .../3-mongo-tools_3.6.3-0ubuntu1_amd64.deb ...
Unpacking mongo-tools (3.6.3-0ubuntu1) ...
Selecting previously unselected package mongodb-clients.
Preparing to unpack .../4-mongodb-clients_1%3a3.6.3-0ubuntu1.4_amd64.deb ...
Unpacking mongodb-clients (1:3.6.3-0ubuntu1.4) ...
Selecting previously unselected package mongodb-server-core.
Preparing to unpack .../5-mongodb-server-core_1%3a3.6.3-0ubuntu1.4_amd64.deb ...
Unpacking mongodb-server-core (1:3.6.3-0ubuntu1.4) ...
Selecting previously unselected package mongodb-server.
Preparing to unpack .../6-mongodb-server_1%3a3.6.3-0ubuntu1.4_all.deb ...
Unpacking mongodb-server (1:3.6.3-0ubuntu1.4) ...
Selecting previously unselected package mongodb.
Preparing to unpack .../7-mongodb_1%3a3.6.3-0ubuntu1.4_amd64.deb ...
Unpacking mongodb (1:3.6.3-0ubuntu1.4) ...
Setting up libstemmer0d:amd64 (0+svn585-1build1) ...
Setting up libyaml-cpp0.5v5:amd64 (0.5.2-4ubuntu1) ...
Setting up mongodb-server-core (1:3.6.3-0ubuntu1.4) ...
Setting up libpcap0.8:amd64 (1.8.1-6ubuntu1.18.04.2) ...
Setting up mongodb-clients (1:3.6.3-0ubuntu1.4) ...
Setting up mongodb-server (1:3.6.3-0ubuntu1.4) ...
invoke-rc.d: could not determine current runlevel
invoke-rc.d: policy-rc.d denied execution of start.
Created symlink /etc/systemd/system/multi-user.target.wants/mongodb.service → /lib/systemd/system/mongodb.service.
Setting up mongo-tools (3.6.3-0ubuntu1) ...
Setting up mongodb (1:3.6.3-0ubuntu1.4) ...
Processing triggers for systemd (237-3ubuntu10.56) ...
Processing triggers for man-db (2.8.3-2ubuntu0.1) ...
Processing triggers for libc-bin (2.27-3ubuntu1.6) ...
 * Starting database mongodb
   ...done.
```
The Wasmtime CLI can be installed on Linux and macOS with a small install
script:

```sh
curl https://wasmtime.dev/install.sh -sSf | bash
```

Windows or otherwise interested users can download installers and
binaries directly from the [GitHub
Releases](https://github.com/bytecodealliance/wasmtime/releases) page.

## Example

If you've got the [Rust compiler
installed](https://www.rust-lang.org/tools/install) then you can take some Rust
source code:

```rust
fn main() {
    println!("Hello, world!");
}
```

and compile/run it with:

```sh
$ rustup target add wasm32-wasi
$ rustc hello.rs --target wasm32-wasi
$ wasmtime hello.wasm
Hello, world!
```

## Features

* **Fast**. Wasmtime is built on the optimizing [Cranelift] code generator to
  quickly generate high-quality machine code either at runtime or
  ahead-of-time. Wasmtime is optimized for efficient instantiation, low-overhead
  calls between the embedder and wasm, and scalability of concurrent instances.

* **[Secure]**. Wasmtime's development is strongly focused on correctness and
  security. Building on top of Rust's runtime safety guarantees, each Wasmtime
  feature goes through careful review and consideration via an [RFC
  process]. Once features are designed and implemented, they undergo 24/7
  fuzzing donated by [Google's OSS Fuzz]. As features stabilize they become part
  of a [release][release policy], and when things go wrong we have a
  well-defined [security policy] in place to quickly mitigate and patch any
  issues. We follow best practices for defense-in-depth and integrate
  protections and mitigations for issues like Spectre. Finally, we're working to
  push the state-of-the-art by collaborating with academic researchers to
  formally verify critical parts of Wasmtime and Cranelift.

* **[Configurable]**. Wasmtime uses sensible defaults, but can also be
  configured to provide more fine-grained control over things like CPU and
  memory consumption. Whether you want to run Wasmtime in a tiny environment or
  on massive servers with many concurrent instances, we've got you covered.

* **[WASI]**. Wasmtime supports a rich set of APIs for interacting with the host
  environment through the [WASI standard](https://wasi.dev).

* **[Standards Compliant]**. Wasmtime passes the [official WebAssembly test
  suite](https://github.com/WebAssembly/testsuite), implements the [official C
  API of wasm](https://github.com/WebAssembly/wasm-c-api), and implements
  [future proposals to WebAssembly](https://github.com/WebAssembly/proposals) as
  well. Wasmtime developers are intimately engaged with the WebAssembly
  standards process all along the way too.

[Wasmtime]: https://github.com/bytecodealliance/wasmtime
[Cranelift]: https://github.com/bytecodealliance/wasmtime/blob/main/cranelift/README.md
[Google's OSS Fuzz]: https://google.github.io/oss-fuzz/
[security policy]: https://bytecodealliance.org/security
[RFC process]: https://github.com/bytecodealliance/rfcs
[release policy]: https://docs.wasmtime.dev/stability-release.html
[Secure]: https://docs.wasmtime.dev/security.html
[Configurable]: https://docs.rs/wasmtime/latest/wasmtime/struct.Config.html
[WASI]: https://docs.rs/wasmtime-wasi/latest/wasmtime_wasi/
[Standards Compliant]: https://docs.wasmtime.dev/stability-wasm-proposals-support.html

## Language Support

You can use Wasmtime from a variety of different languages through embeddings of
the implementation:

* **[Rust]** - the [`wasmtime` crate]
* **[C]** - the [`wasm.h`, `wasi.h`, and `wasmtime.h` headers][c-headers], [CMake](crates/c-api/CMakeLists.txt) or [`wasmtime` Conan package]
* **C++** - the [`wasmtime-cpp` repository][wasmtime-cpp] or use [`wasmtime-cpp` Conan package]
* **[Python]** - the [`wasmtime` PyPI package]
* **[.NET]** - the [`Wasmtime` NuGet package]
* **[Go]** - the [`wasmtime-go` repository]

[Rust]: https://bytecodealliance.github.io/wasmtime/lang-rust.html
[C]: https://bytecodealliance.github.io/wasmtime/examples-c-embed.html
[`wasmtime` crate]: https://crates.io/crates/wasmtime
[c-headers]: https://bytecodealliance.github.io/wasmtime/c-api/
[Python]: https://bytecodealliance.github.io/wasmtime/lang-python.html
[`wasmtime` PyPI package]: https://pypi.org/project/wasmtime/
[.NET]: https://bytecodealliance.github.io/wasmtime/lang-dotnet.html
[`Wasmtime` NuGet package]: https://www.nuget.org/packages/Wasmtime
[Go]: https://bytecodealliance.github.io/wasmtime/lang-go.html
[`wasmtime-go` repository]: https://pkg.go.dev/github.com/bytecodealliance/wasmtime-go
[wasmtime-cpp]: https://github.com/bytecodealliance/wasmtime-cpp
[`wasmtime` Conan package]: https://conan.io/center/wasmtime
[`wasmtime-cpp` Conan package]: https://conan.io/center/wasmtime-cpp

## Documentation

[📚 Read the Wasmtime guide here! 📚][guide]

The [wasmtime guide][guide] is the best starting point to learn about what
Wasmtime can do for you or help answer your questions about Wasmtime. If you're
curious in contributing to Wasmtime, [it can also help you do
that][contributing]!

[contributing]: https://bytecodealliance.github.io/wasmtime/contributing.html
[guide]: https://bytecodealliance.github.io/wasmtime

---

It's Wasmtime.
