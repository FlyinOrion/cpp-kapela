# Kapela
Copyright (c) 2017-2018 The Kapela Project

## What is this?

Kapela is a blockchain-powered messaging and payment platform. Messages and payments can be sent as anonymously and securely as you require, and with the magic of decentralization, there is no single physical place where your data can be accessed without the permission of your private key signature.

### But really, What _is_ this?

The Kapela blockchain utilizes the same base algorithm that Monero implements in order to provide the following peer-reviewed features:

**User-Controlled Privacy:** Kapela uses a cryptographically sound system to allow you to send and receive messages and funds without your transactions being easily revealed on the blockchain. This ensures that your conversations, purchases, receipts, and all transfers remain as private as you want. Our protocol gives you control over who can see your messages and transactions without any unneccesary roadblocks.

**Ensured Security:** Using the power of a distributed peer-to-peer consensus network, every transaction on the network is cryptographically secured. Individual wallets have a 25 word mnemonic seed that is only displayed once, and can be written down to backup the wallet. Wallet files are encrypted with a passphrase to ensure they are useless if stolen.

**Proven Untraceability:** By taking advantage of ring signatures, a special property of a certain type of cryptography, Kapela is able to ensure that transactions are not only untraceable, but have an optional measure of ambiguity that ensures that transactions cannot easily be tied back to an individual user or computer.

**Native Monetary Functionality:** With the benefit of being a native blockchain platform, transfers of value will be available as well. With both transaction processing types(money and messages) being governed by the same security protocol, you have the same privacy control over your financial transactions as you would have over your messages.

### Contact Us!

- Web: [kapela.io](https://kapela.io)
- Forum: [forum.kapela.io](https://forum.kapela.io) (Coming soon)
- Mail: [info@kapela.io](mailto:info@kapela.io)
- GitHub: [https://github.com/kapela-project](https://github.com/kapela-project)

## Building Kapela

### On *nix:

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, and Boost 1.55 or later.

You may download them from:

- http://gcc.gnu.org/
- http://www.cmake.org/
- http://www.boost.org/

Alternatively, it may be possible to install them using a package manager.

To build, change to a directory where this file is located, and run `make`. The resulting executables can be found in `build/release/src`.

#### Advanced options:

Parallel build: run `make -j<number of threads>` instead of `make`.

Debug build: run `make build-debug`.

Test suite: run `make test-release` to run tests in addition to building. Running `make test-debug` will do the same to the debug version.

Building with Clang: it may be possible to use Clang instead of GCC, but this may not work everywhere. To build, run `export CC=clang CXX=clang++` before running `make`.

### On Windows:
Dependencies: MSVC 2013 or later, CMake 2.8.6 or later, and Boost 1.55 or later. You may download them from:

- http://www.microsoft.com/
- http://www.cmake.org/
- http://www.boost.org/

To build, change to a directory where this file is located, and run this commands:
```
mkdir build
cd build
cmake -G "Visual Studio 12 Win64" ..
```
And then do the Build. Good luck!

### HTML wallet:

1. First run kapelad, wait until it syncs...
2. Than run simplewallet in JSON-RPC enabled mode on 48782 port:   
`./simplewallet --wallet-file=WALLETFILE --password=PASSWORD --rpc-bind-port=48782`
3. Wait until it syncs...
4. Open wallet.html page in browser and you should see a web GUI
