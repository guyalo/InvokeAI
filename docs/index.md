---
title: Home
---

<!--
  The Docs you find here (/docs/*) are built and deployed via mkdocs. If you want to run a local version to verify your changes, it's as simple as::

  ```bash
  pip install -r requirements-mkdocs.txt
  mkdocs serve
  ```
-->
<div align="center" markdown>

# ^^**InvokeAI: A Stable Diffusion Toolkit**^^ :tools: <br> <small>Formerly known as lstein/stable-diffusion</small>

[![project logo](assets/logo.png)](https://github.com/invoke-ai/InvokeAI)

[![discord badge]][discord link]

[![latest release badge]][latest release link]
[![github stars badge]][github stars link]
[![github forks badge]][github forks link]

[![CI checks on main badge]][ci checks on main link]
[![CI checks on dev badge]][ci checks on dev link]
[![latest commit to dev badge]][latest commit to dev link]

[![github open issues badge]][github open issues link]
[![github open prs badge]][github open prs link]

[ci checks on dev badge]:
  https://flat.badgen.net/github/checks/invoke-ai/InvokeAI/development?label=CI%20status%20on%20dev&cache=900&icon=github
[ci checks on dev link]:
  https://github.com/invoke-ai/InvokeAI/actions?query=branch%3Adevelopment
[ci checks on main badge]:
  https://flat.badgen.net/github/checks/invoke-ai/InvokeAI/main?label=CI%20status%20on%20main&cache=900&icon=github
[ci checks on main link]:
  https://github.com/invoke-ai/InvokeAI/actions/workflows/test-invoke-conda.yml
[discord badge]: https://flat.badgen.net/discord/members/ZmtBAhwWhy?icon=discord
[discord link]: https://discord.gg/ZmtBAhwWhy
[github forks badge]:
  https://flat.badgen.net/github/forks/invoke-ai/InvokeAI?icon=github
[github forks link]:
  https://useful-forks.github.io/?repo=lstein%2Fstable-diffusion
[github open issues badge]:
  https://flat.badgen.net/github/open-issues/invoke-ai/InvokeAI?icon=github
[github open issues link]:
  https://github.com/invoke-ai/InvokeAI/issues?q=is%3Aissue+is%3Aopen
[github open prs badge]:
  https://flat.badgen.net/github/open-prs/invoke-ai/InvokeAI?icon=github
[github open prs link]:
  https://github.com/invoke-ai/InvokeAI/pulls?q=is%3Apr+is%3Aopen
[github stars badge]:
  https://flat.badgen.net/github/stars/invoke-ai/InvokeAI?icon=github
[github stars link]: https://github.com/invoke-ai/InvokeAI/stargazers
[latest commit to dev badge]:
  https://flat.badgen.net/github/last-commit/invoke-ai/InvokeAI/development?icon=github&color=yellow&label=last%20dev%20commit&cache=900
[latest commit to dev link]:
  https://github.com/invoke-ai/InvokeAI/commits/development
[latest release badge]:
  https://flat.badgen.net/github/release/invoke-ai/InvokeAI/development?icon=github
[latest release link]: https://github.com/invoke-ai/InvokeAI/releases

</div>

<a href="https://github.com/invoke-ai/InvokeAI">InvokeAI</a> is an
implementation of Stable Diffusion, the open source text-to-image and
image-to-image generator. It provides a streamlined process with various new
features and options to aid the image generation process. It runs on Windows,
Mac and Linux machines, and runs on GPU cards with as little as 4 GB or RAM.

**Quick links**: [<a href="https://discord.gg/ZmtBAhwWhy">Discord Server</a>] [<a href="https://github.com/invoke-ai/InvokeAI/">Code and Downloads</a>] [<a href="https://github.com/invoke-ai/InvokeAI/issues">Bug Reports</a>] [<a href="https://github.com/invoke-ai/InvokeAI/discussions">Discussion, Ideas & Q&A</a>]

<div align="center"><img src="assets/invoke-web-server-1.png" width=640></div>

!!! note

    This fork is rapidly evolving. Please use the [Issues tab](https://github.com/invoke-ai/InvokeAI/issues) to report bugs and make feature requests. Be sure to use the provided templates. They will help aid diagnose issues faster.

## :octicons-package-dependencies-24: Installation

This fork is supported across Linux, Windows and Macintosh. Linux
users can use either an Nvidia-based card (with CUDA support) or an
AMD card (using the ROCm driver). For full installation and upgrade
instructions, please see:
[InvokeAI Installation Overview](https://invoke-ai.github.io/InvokeAI/installation/)

Linux users who wish to make use of the PyPatchMatch inpainting
functions will need to perform a bit of extra work to enable this
module. Instructions can be found at [Installing PyPatchMatch](installation/INSTALL_PATCHMATCH.md).

## :fontawesome-solid-computer: Hardware Requirements

### :octicons-cpu-24: System

You wil need one of the following:

- :simple-nvidia: An NVIDIA-based graphics card with 4 GB or more VRAM memory.
- :simple-amd: An AMD-based graphics card with 4 GB or more VRAM memory (Linux only)
- :fontawesome-brands-apple: An Apple computer with an M1 chip.

### :fontawesome-solid-memory: Memory

- At least 12 GB Main Memory RAM.

### :fontawesome-regular-hard-drive: Disk

- At least 12 GB of free disk space for the machine learning model, Python, and
  all its dependencies.

!!! info

    If you are have a Nvidia 10xx series card (e.g. the 1080ti), please run the invoke script in
    full-precision mode as shown below.

    Similarly, specify full-precision mode on Apple M1 hardware.

    Precision is auto configured based on the device. If however you encounter errors like
    `expected type Float but found Half` or `not implemented for Half` you can try starting
    `invoke.py` with the `--precision=float32` flag:

    ```bash
    (invokeai) ~/InvokeAI$ python scripts/invoke.py --full_precision
    ```
## :octicons-gift-24: InvokeAI Features

- [The InvokeAI Web Interface](features/WEB.md)
    - [WebGUI hotkey reference guide](features/WEBUIHOTKEYS.md)
    - [WebGUI Unified Canvas for Img2Img, inpainting and outpainting](features/UNIFIED_CANVAS.md)
<!-- seperator -->
- [The Command Line Interace](features/CLI.md)
    - [Image2Image](features/IMG2IMG.md)
    - [Inpainting](features/INPAINTING.md)
    - [Outpainting](features/OUTPAINTING.md)
    - [Adding custom styles and subjects](features/CONCEPTS.md)
    - [Upscaling and Face Reconstruction](features/POSTPROCESS.md)
<!-- seperator -->
- [Generating Variations](features/VARIATIONS.md)
<!-- seperator -->
- [Prompt Engineering](features/PROMPTS.md)
<!-- seperator -->
- Miscellaneous
    - [NSFW Checker](features/NSFW.md)
    - [Embiggen upscaling](features/EMBIGGEN.md)
    - [Other](features/OTHER.md)

## :octicons-log-16: Latest Changes

### v2.1.3 <small>(13 November 2022)</small>

- A choice of installer scripts that automate installation and configuration. See [Installation](https://github.com/invoke-ai/InvokeAI/blob/2.1.3-rc6/docs/installation/INSTALL.md).
- A streamlined manual installation process that works for both Conda and PIP-only installs. See [Manual Installation](https://github.com/invoke-ai/InvokeAI/blob/2.1.3-rc6/docs/installation/INSTALL_MANUAL.md).
- The ability to save frequently-used startup options (model to load, steps, sampler, etc) in a `.invokeai` file. See [Client](https://github.com/invoke-ai/InvokeAI/blob/2.1.3-rc6/docs/features/CLI.md)
- Support for AMD GPU cards (non-CUDA) on Linux machines.
- Multiple bugs and edge cases squashed.

### v2.1.0 <small>(2 November 2022)</small>

- [Inpainting](https://invoke-ai.github.io/InvokeAI/features/INPAINTING/)
  support in the WebGUI
- Greatly improved navigation and user experience in the
  [WebGUI](https://invoke-ai.github.io/InvokeAI/features/WEB/)
- The prompt syntax has been enhanced with
  [prompt weighting, cross-attention and prompt merging](https://invoke-ai.github.io/InvokeAI/features/PROMPTS/).
- You can now load
  [multiple models and switch among them quickly](https://docs.google.com/presentation/d/1WywGA1rny7bpFh7CLSdTr4nNpVKdlUeT0Bj0jCsILyU/edit?usp=sharing)
  without leaving the CLI.
- The installation process (via `scripts/configure_invokeai.py`) now lets you select
  among several popular
  [Stable Diffusion models](https://invoke-ai.github.io/InvokeAI/installation/INSTALLING_MODELS/)
  and downloads and installs them on your behalf. Among other models, this
  script will install the current Stable Diffusion 1.5 model as well as a
  StabilityAI variable autoencoder (VAE) which improves face generation.
- Tired of struggling with photoeditors to get the masked region of for
  inpainting just right? Let the AI make the mask for you using
  [text masking](https://docs.google.com/presentation/d/1pWoY510hCVjz0M6X9CBbTznZgW2W5BYNKrmZm7B45q8/edit#slide=id.p).
  This feature allows you to specify the part of the image to paint over using
  just English-language phrases.
- Tired of seeing the head of your subjects cropped off? Uncrop them in the CLI
  with the
  [outcrop feature](https://invoke-ai.github.io/InvokeAI/features/OUTPAINTING/#outcrop).
- Tired of seeing your subject's bodies duplicated or mangled when generating
  larger-dimension images? Check out the `--hires` option in the CLI, or select
  the corresponding toggle in the WebGUI.
- We now support textual inversion and fine-tune .bin styles and subjects from
  the Hugging Face archive of
  [SD Concepts](https://huggingface.co/sd-concepts-library). Load the .bin file
  using the `--embedding_path` option. (The next version will support merging
  and loading of multiple simultaneous models).
- ...

### v2.0.1 <small>(13 October 2022)</small>

- fix noisy images at high step count when using k\* samplers
- dream.py script now calls invoke.py module directly rather than via a new
  python process (which could break the environment)

### v2.0.0 <small>(9 October 2022)</small>

- `dream.py` script renamed `invoke.py`. A `dream.py` script wrapper remains for
  backward compatibility.
- Completely new WebGUI - launch with `python3 scripts/invoke.py --web`
- Support for
  <a href="https://invoke-ai.github.io/InvokeAI/features/INPAINTING/">inpainting</a>
  and
  <a href="https://invoke-ai.github.io/InvokeAI/features/OUTPAINTING/">outpainting</a>
- img2img runs on all k\* samplers
- Support for
  <a href="https://invoke-ai.github.io/InvokeAI/features/PROMPTS/#negative-and-unconditioned-prompts">negative
  prompts</a>
- Support for CodeFormer face reconstruction
- Support for Textual Inversion on Macintoshes
- Support in both WebGUI and CLI for
  <a href="https://invoke-ai.github.io/InvokeAI/features/POSTPROCESS/">post-processing
  of previously-generated images</a> using facial reconstruction, ESRGAN
  upscaling, outcropping (similar to DALL-E infinite canvas), and "embiggen"
  upscaling. See the `!fix` command.
- New `--hires` option on `invoke>` line allows
  <a href="https://invoke-ai.github.io/InvokeAI/features/CLI/#txt2img">larger
  images to be created without duplicating elements</a>, at the cost of some
  performance.
- New `--perlin` and `--threshold` options allow you to add and control
  variation during image generation (see
  <a href="https://github.com/invoke-ai/InvokeAI/blob/main/docs/features/OTHER.md#thresholding-and-perlin-noise-initialization-options">Thresholding
  and Perlin Noise Initialization</a>
- Extensive metadata now written into PNG files, allowing reliable regeneration
  of images and tweaking of previous settings.
- Command-line completion in `invoke.py` now works on Windows, Linux and Mac
  platforms.
- Improved
  <a href="https://invoke-ai.github.io/InvokeAI/features/CLI/">command-line
  completion behavior</a>. New commands added:
  - List command-line history with `!history`
  - Search command-line history with `!search`
  - Clear history with `!clear`
- Deprecated `--full_precision` / `-F`. Simply omit it and `invoke.py` will auto
  configure. To switch away from auto use the new flag like
  `--precision=float32`.

For older changelogs, please visit the
**[CHANGELOG](CHANGELOG/#v114-11-september-2022)**.

## :material-target: Troubleshooting

Please check out our
**[:material-frequently-asked-questions: Q&A](help/TROUBLESHOOT.md)** to get
solutions for common installation problems and other issues.

## :octicons-repo-push-24: Contributing

Anyone who wishes to contribute to this project, whether documentation,
features, bug fixes, code cleanup, testing, or code reviews, is very much
encouraged to do so. If you are unfamiliar with how to contribute to GitHub
projects, here is a
[Getting Started Guide](https://opensource.com/article/19/7/create-pull-request-github).

A full set of contribution guidelines, along with templates, are in progress,
but for now the most important thing is to **make your pull request against the
"development" branch**, and not against "main". This will help keep public
breakage to a minimum and will allow you to propose more radical changes.

## :octicons-person-24: Contributors

This fork is a combined effort of various people from across the world.
[Check out the list of all these amazing people](other/CONTRIBUTORS.md). We
thank them for their time, hard work and effort.

## :octicons-question-24: Support

For support, please use this repository's GitHub Issues tracking service. Feel
free to send me an email if you use and like the script.

Original portions of the software are Copyright (c) 2020
[Lincoln D. Stein](https://github.com/lstein)

## :octicons-book-24: Further Reading

Please see the original README for more information on this software and
underlying algorithm, located in the file
[README-CompViz.md](other/README-CompViz.md).
