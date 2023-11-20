# Passwordless
Repository to test concepts around "Passwordless" movement with FIDO2, Passkeys and others...

_**Note:** this demo is based on [another demo by duo labs](https://github.com/duo-labs/duo-blog-going-passwordless-with-py-webauthn). [Blog post](https://duo.com/blog/going-passwordless-with-py-webauthn)._

## Required software for running locally
- [Python 3.11+](https://www.python.org/downloads/)
- Windows only: [Microsoft Build Tools for Visual Studio 2022](https://aka.ms/vs/17/release/vs_BuildTools.exe)
  - Or [MinGW](http://www.mingw.org/) (for building the [CFFI](https://cffi.readthedocs.io/en/latest/installation.html) dependency)
- Unix based systems only: any C compiler
  - macOS: [Xcode](https://developer.apple.com/xcode/)
    - Easy way, just execute: `xcode-select --install`
  - Linux distros: [GCC](https://gcc.gnu.org/)
    - Debian/Ubuntu: `sudo apt install build-essential`
    - Fedora: `sudo dnf install @development-tools`
    - Arch: `sudo pacman -S base-devel`
    - Alpine: `sudo apk add build-base`

### Optional

- [Docker](https://docs.docker.com/engine/install/) (for running the [Dockerfile](Dockerfile))

## Getting Started running locally

1. Generate a new [`venv` (Virtual environment)](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/):

    Unix:
   ```shell
   python3 -m venv venv
   ```

   Windows:
   ```powershell
   py -m venv .venv
   ```

2. Activate the `venv`:

   Unix:
   ```shell
   source venv/bin/activate
   ```

   Windows:
   ```shell
   venv\bin\Activate.bat
   ```

3. Install the dependencies:

   ```shell
   pip install -r requirements.txt
   ```

4. Run the server:

   Unix:
   ```shell
   ./start-server.sh
   ```

   Windows:
   ```shell
   .\start-server.ps1
   ```

### Running with Docker

1. Build the image:

   ```shell
   docker build -t passwordless .
   ```

2. Run the container:

   ```shell
    docker run -p 5000:5000 passwordless
    ```

## Running on Google Colab


## References

- [WebAuthn](https://www.w3.org/TR/webauthn/)
- [WebAuthn Guide](https://webauthn.guide/)
- [WebAuthn.io](https://webauthn.io/)
- [py_webauthn](https://github.com/duo-labs/py_webauthn)
