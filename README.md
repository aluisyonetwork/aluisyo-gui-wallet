# Aluisyo Wallet (GUI)
Latest Release: v0.0.2
Maintained by Aluisyo.

## Information
Aluisyo is a free open source privacy protected peer-to-peer digital cash system that is completely decentralized, without the need for a central server or trusted parties. Users hold the crypto keys to their own money and transact directly with each other, with the help of a P2P network to check for double-spending. Aluisyo has a decentralized blockchain banking in its core and instant untraceable crypto messages that can be decrypted with recipients private key.

## Resources
- Web: [aluisyo.network](https://aluisyo.network/)
- GitHub: [https://github.com/aluisyonetwork/aluisyo-core](https://github.com/aluisyonetwork/aluisyo-core)
- Discord: [https://discord.aluisyo.network](https://discord.aluisyo.network)
- Paperwallet: [https://paperwallet.aluisyo.network/](https://paperwallet.aluisyo.network/)

## Compiling Aluisyo from source

### Linux / Ubuntu

##### Prerequisites

Dependencies: GCC 4.7.3 or later, CMake 2.8.6 or later, Boost 1.55 or later, and Qt 5.9 or later.
You may download them from:

- http://gcc.gnu.org/
- http://www.cmake.org/
- http://www.boost.org/
- https://www.qt.io

Alternatively, it may be possible to install them using a package manager.

#### Building

To acquire the source via git and build the release version, run the following commands:

- `cd ~`
- `git clone https://github.com/aluisyonetwork/aluisyo-wallet`
- `cd aluisyo-wallet`
- `git clone https://github.com/aluisyonetwork/aluisyo-core.git cryptonote`
- `make build-release`
- `mkdir bin && mv build/release/Aluisyo-GUI bin/`
- `make clean`

If the build is successful the binaries will be in the bin folder.

### Windows 10

##### Prerequisites

- Install [Visual Studio 2017 Community Edition](https://www.visualstudio.com/thank-you-downloading-visual-studio/?sku=Community&rel=15&page=inlineinstall)
- When installing Visual Studio, you need to install **Desktop development with C++** and the **VC++ v140 toolchain** components. The option to install the v140 toolchain can be found by expanding the "Desktop development with C++" node on the right. You will need this for the project to build correctly.
- Install [CMake](https://cmake.org/download/)
- Install [Boost 1.67.0](https://boost.teeks99.com/bin/1.67.0/), ensuring you download the installer for MSVC 14.1.
- Install [Qt 5.11.0](https://www.qt.io/download)

##### Building

- From the start menu, open 'x64 Native Tools Command Prompt for vs2017' or run "C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\Tools\VsMSBuildCmd.bat" from any command prompt.
- Edit the CMakeLists.txt file and set the path to QT cmake folder. For exampple: set(CMAKE_PREFIX_PATH "C:\\Qt\\5.11.0\\msvc2017_64\\lib\\cmake\\").
- `git clone https://github.com/aluisyonetwork/aluisyo-core`
- `git clone https://github.com/aluisyonetwork/aluisyo-wallet`
- Copy the contents of the aluisyo-core folder into aluisyo-wallet\cryptonote
- `cd aluisyo-wallet`
- `mkdir build`
- `cd build`
- `cmake -G "Visual Studio 15 2017 Win64" -DBOOST_LIBRARYDIR:PATH=c:/local/boost_1_67_0 ..` (Or your boost installed dir.)
- `msbuild ALUISYO-GUI.sln /p:Configuration=Release`

If the build is successful the binaries will be in the Release folder.

#### Special Thanks
Special thanks goes out to the developers from Cryptonote, Bytecoin, Monero, Forknote, TurtleCoin, and Masari.
