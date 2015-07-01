Try blaze-react
===============

Disclaimer: The code in this repository is based on Ryan Trinkle's awesome
  [try-reflex](https://github.com/ryantrinkle/try-reflex) repository and scripts.
I have merely adopted it to provide an easy way for experimenting with
  [blaze-react](https://github.com/meiersi/blaze-react),
    as GHCJS still requires some chuzpe to install.


Important Notes
---------------
If you're using one of these platforms, please take a look at notes before you begin:

* [NixOS](notes/NixOS.md)
* [Linux Mint](notes/LinuxMint.md)

If you encounter any problems that may be specific to your platform, please submit an issue or pull request so that we can add a note for future users.

Setup
-----
The steps below will set up an environment from which you can use Reflex with GHCJS. This process will install the [Nix package manager](https://nixos.org/nix/). If you prefer to install Nix yourself, you may do so any time prior to step 2.

1. Clone the try-blaze-react repo:

    ```bash
    git clone https://github.com/meiersi/try-blaze-react
    ```

2. Navigate into the `try-blaze-react` folder and run the try-blaze-react bootstrapping command. This will install nix, if you don't have it already, and use it to wrangle all the dependencies you'll need and drop you in an environment from which you can use Reflex. Be warned, this might take a little while the first time:

    ```bash
    cd try-blaze-react
    ./try-blaze-react
    ```

3. From this nix-shell, you can compile your haskell source using ghcjs:

    ```bash
    ghcjs --make source.hs
    ```
    This should look fairly familiar to anyone who has compiled with ghc.

4. Compilation will produce a `source.jsexe` folder containing an `index.html` file. Open that in your browser to run your app.

5. If you need to add any additional dependencies, edit packages.nix, then exit and re-enter the try-blaze-react shell.  **Don't use cabal** to install libraries while inside the nix shell - the resulting libraries may not be found properly by ghc or ghcjs.  Using cabal to configure, build, test, and run a particular package, however, should work just fine.


Tutorial
========

..more to come..
