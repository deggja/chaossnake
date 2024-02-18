<div align="center">
  <a href="https://go.dev/">
    <img src="https://img.shields.io/badge/Go-v1.21-brightgreen.svg" alt="go version">
  </a>
</div>

<div align="center">

  <h1>Serpent</h1>
  <h3>Control snake. Eat food. Create chaos.</h3>

</div>

## Contents
- [**What is Serpent?**](#-what-is-serpent-)
- **[Installation](#installation)**
  - [Build from source](#build-from-source-)
  - [Precompiled binaries](#precompiled-binaries-)
- [**Usage**](#usage)
  - [Starting the game](#starting-the-game-)
  - [Playing Serpent](#playing-serpent-)
  - [Kubernetes interaction](#kubernetes-interaction-)
- [**Contribute**](#contribute-)
- [**Acknowledgements**](#acknowledgments)

## ⭐ What is Serpent? ⭐

Serpent lets you play snake while wrecking havock in your Kubernetes cluster. Have fun while you can.

### How does it work? 🤔

Each piece of food you eat corresponds to a pod in your cluster (I left out kube-system though..).

## Installation

### Homebrew 🍺

To install Serpent using Homebrew, you can run the following commands:

```sh
brew tap deggja/serpent https://github.com/deggja/serpent
brew install serpent
```

### Build from source 💻

To build Serpent from the source, you need a working Go environment with version 1.21 or higher. Follow these steps:

```sh
git clone https://github.com/deggja/serpent.git --depth 1
cd serpent
go build -o serpent
```

## Usage

### Starting the game

To start the game, simply run the compiled binary:

```sh
./serpent
```

## Playing Serpent

Use the arrow keys to navigate the snake around the screen:

- **Up arrow** - Move up
- **Down arrow** - Move down
- **Left arrow** - Move left
- **Right arrow** - Move right

[![asciicast](https://asciinema.org/a/Q4usmR4HB8LhHojJA9qJeQmdX.svg)](https://asciinema.org/a/Q4usmR4HB8LhHojJA9qJeQmdX)

## Kubernetes interaction

Serpent will require access to your Kubernetes cluster. Ensure your `kubeconfig` is set up correctly before starting the game. The application currently expects the kubeconfig at its default location.

As you play and the pods are deleted, Serpent will log the actions to a `chaos.log` file for your review.

## Contribute 🔨

Feel free to dive in! [Open an issue](https://github.com/deggja/serpent/issues) or submit PRs.

## Acknowledgments

This project utilizes [Termloop](https://github.com/JoelOtter/termloop), a simple Go library for creating terminal-based games. Thanks to the creators and contributors of Termloop for providing such a versatile tool.

Logo is generated using DALL-E and edited using canva.

## License

Serpent is released under the MIT License. Check out the [LICENSE](https://github.com/deggja/serpent/LICENSE) file for more information.
