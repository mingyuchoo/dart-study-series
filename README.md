<p align="center">
  <a href="https://github.com/mingyuchoo/dart-study-series/blob/main/LICENSE"><img alt="license" src="https://img.shields.io/github/license/mingyuchoo/dart-study-series"/></a>
  <a href="https://github.com/mingyuchoo/dart-study-series/issues"><img alt="Issues" src="https://img.shields.io/github/issues/mingyuchoo/dart-study-series?color=appveyor" /></a>
  <a href="https://github.com/mingyuchoo/dart-study-series/pulls"><img alt="GitHub pull requests" src="https://img.shields.io/github/issues-pr/mingyuchoo/dart-study-series?color=appveyor" /></a>
</p>

# dart-study-series

## Install the Dart SDK

```bash
$ sudo apt-get update
$ sudo apt-get install apt-transport-https
$ wget -qO- https://dl-ssl.google.com/linux/linux_signing_key.pub | sudo gpg --dearmor -o /usr/share/keyrings/dart.gpg
$ echo 'deb [signed-by=/usr/share/keyrings/dart.gpg arch=amd64] https://storage.googleapis.com/download.dartlang.org/linux/debian stable main' | sudo tee /etc/apt/sources.list.d/dart_stable.list

$ sudo apt-get update
$ sudo apt-get install dart
```

```bash
$ echo 'export PATH="$PATH:/usr/lib/dart/bin"' >> ~/.profile
```
## Create small app

```bash
$ dart create -t console cli
$ cd cli

$ dart run
Building package executable...
Built cli:cli.
Hello world: 42!

$ dart test
Building package executable... (5.6s)
Built test:test.
00:01 +1: All tests passed!
```
## Compile for production

```bash
$ dart compile exe bin/cli.dart

$ time bin/cli.exe
Info: Compiling with sound null safety
Generated: /home/mgch/workspace/cli/bin/cli.exe

$ time bin/cli.exe
Hello world: 42!

real    0m0.006s
user    0m0.000s
sys     0m0.006s
```

## References

- <https://dart.dev/get-dart>

