[![Github top language](https://img.shields.io/github/languages/top/FHPythonUtils/ImageEdit.svg?style=for-the-badge)](../../)
[![Codacy grade](https://img.shields.io/codacy/grade/caca6f53db3a44f08b7cbdb25284e784.svg?style=for-the-badge)](https://www.codacy.com/gh/FHPythonUtils/ImageRound)
[![Codacy coverage](https://img.shields.io/codacy/coverage/caca6f53db3a44f08b7cbdb25284e784.svg?style=for-the-badge)](https://www.codacy.com/gh/FHPythonUtils/ImageRound)
[![Repository size](https://img.shields.io/github/repo-size/FHPythonUtils/ImageEdit.svg?style=for-the-badge)](../../)
[![Issues](https://img.shields.io/github/issues/FHPythonUtils/ImageEdit.svg?style=for-the-badge)](../../issues)
[![License](https://img.shields.io/github/license/FHPythonUtils/ImageEdit.svg?style=for-the-badge)](/LICENSE.md)
[![Commit activity](https://img.shields.io/github/commit-activity/m/FHPythonUtils/ImageEdit.svg?style=for-the-badge)](../../commits/master)
[![Last commit](https://img.shields.io/github/last-commit/FHPythonUtils/ImageEdit.svg?style=for-the-badge)](../../commits/master)
[![PyPI Downloads](https://img.shields.io/pypi/dm/imageedit.svg?style=for-the-badge)](https://pypi.org/project/imageedit/)
[![PyPI Version](https://img.shields.io/pypi/v/imageedit.svg?style=for-the-badge)](https://pypi.org/project/imageedit/)

<!-- omit in toc -->
# ImageEdit

<img src="readme-assets/icons/name.png" alt="Project Icon" width="750">

[**Now available on pypi.org!**](https://pypi.org/project/imageedit/)

Create various icon masks and shading effects with the imageedit library.
Six example files under main: round.py, makeProjIcons.py, makePWAImages.py,
makeRetro.py, getPWAScreenshots.py and readWriteLayered.py.

Leverages the following libraries to do the heavy lifting:
```none
pillow
layeredimage
svgtrace
blendmodes
```

Have a look under test/test_readWriteLayered for an example of converting an
xcf to ora and png. Unfortunately, visibility of xcf is currently ignored :(

- [Documentation](#documentation)
- [Example Files](#example-files)
- [Comparison to similar solutions](#comparison-to-similar-solutions)
	- [GUI](#gui)
	- [Web](#web)
	- [Advantages of this solution](#advantages-of-this-solution)
	- [Disadvantages of this solution](#disadvantages-of-this-solution)
- [How to use out of the box](#how-to-use-out-of-the-box)
	- [makePWAImages](#makepwaimages)
	- [makeRetro](#makeretro)
- [Install With PIP](#install-with-pip)
- [Language information](#language-information)
	- [Built for](#built-for)
- [Install Python on Windows](#install-python-on-windows)
	- [Chocolatey](#chocolatey)
	- [Download](#download)
- [Install Python on Linux](#install-python-on-linux)
	- [Apt](#apt)
- [How to run](#how-to-run)
	- [With VSCode](#with-vscode)
	- [From the Terminal](#from-the-terminal)
- [Download](#download-1)
	- [Clone](#clone)
		- [Using The Command Line](#using-the-command-line)
		- [Using GitHub Desktop](#using-github-desktop)
	- [Download Zip File](#download-zip-file)
- [Community Files](#community-files)
	- [Licence](#licence)
	- [Changelog](#changelog)
	- [Code of Conduct](#code-of-conduct)
	- [Contributing](#contributing)
	- [Security](#security)
- [Screenshots](#screenshots)
	- [Desktop](#desktop)

## Documentation
See the [DOCS](/DOCS.md) for more information.

See the documentation for each library for more information on things you
can use it for.

## Example Files
- getPWAScreenshots.py
- makeProjIcons.py
- makePWAImages.py
- makeRetro.py
- readWriteLayered.py
- round.py

## Comparison to similar solutions

Similar solutions include but are not limited to:

### GUI
https://www.getpaint.net/

### Web
https://realfavicongenerator.net/

### Advantages of this solution
- Lightweight: few dependencies required (python, pillow, blendmodes,
layeredimage, and svgtrace)
- Quick: when given a regular or mask image it can produce many
variants in a relatively short amount of time
- Customizable: write your own scripts to leverage imageEdit (python knowledge
required)
- Produce a PWA mask icon out of the box
- SVG tracing lib doesn't require potrace/ pypotrace which can be challenging to
set up on Windows
- SVG tracing using imageTracerJs.py (https://github.com/jankovicsandras/imagetracerjs)
is pretty good (requires pyppeteer: https://github.com/miyakogi/pyppeteer)

### Disadvantages of this solution
- Specific image dimensions needed out of the box: whilst this is something that
could be changed, maskable icons are 640x640 and regular icons are 512x512

## How to use out of the box

### makePWAImages

1. Put regular 512x512 image or mask 640x640 image under main/input in this
example I am using lightfox.png

	<img src="readme-assets/examples/lightfox.png" alt="LightFox" width="128">

2. Run ```makePWAImages.py``` and navigate to main/output/lightfox.png/pwa

	<div>
	<img src="readme-assets/examples/mask.png" alt="LightFox" width="128">
	<img src="readme-assets/examples/round-192.png" alt="LightFox" width="38">
	<img src="readme-assets/examples/round-512.png" alt="LightFox" width="102">
	<img src="readme-assets/examples/square-180.png" alt="LightFox" width="36">
	<img src="readme-assets/examples/squircle-256.png" alt="LightFox" width="52">
	</div>

### makeRetro
1. Put regular 512x512 image or mask 640x640 image under main/input. In this
   example I am using BlendModes.png

	<img src="readme-assets/examples/blendmodes.png" alt="BlendModes" width="128">

2. Run ```makeRetro.py``` and navigate to main/output/blendmodes.png/retro
	Personal Computers

	<div>
	<img src="readme-assets/examples/3level.png" alt="BlendModes" width="128">
	<img src="readme-assets/examples/bbc-micro.png" alt="BlendModes" width="128">
	<img src="readme-assets/examples/zxspectrum.png" alt="BlendModes" width="128">
	<img src="readme-assets/examples/websafe.png" alt="BlendModes" width="128">
	</div>

	Mobile Operating Systems

	iOS

	<div>
	<img src="readme-assets/examples/ios1.png" alt="BlendModes" width="128">
	<img src="readme-assets/examples/ios7.png" alt="BlendModes" width="128">
	</div>

	Android

	<div>
	<img src="readme-assets/examples/android2.png" alt="BlendModes" width="128">
	<img src="readme-assets/examples/android6.png" alt="BlendModes" width="128">
	<img src="readme-assets/examples/android7.png" alt="BlendModes" width="128">
	<img src="readme-assets/examples/android8.png" alt="BlendModes" width="128">
	</div>

## Install With PIP

```python
pip install imageedit
```

Head to https://pypi.org/project/imageedit/ for more info

See python files under main for example usage

## Language information
### Built for
This program has been written for Python 3 and has been tested with
Python version 3.8.0 <https://www.python.org/downloads/release/python-380/>.

## Install Python on Windows
### Chocolatey
```powershell
choco install python
```
### Download
To install Python, go to <https://www.python.org/> and download the latest
version.

## Install Python on Linux
### Apt
```bash
sudo apt install python3.8
```

## How to run
### With VSCode
1. Open the .py file in vscode
2. Ensure a python 3.8 interpreter is selected (Ctrl+Shift+P > Python:Select
Interpreter > Python 3.8)
3. Run by pressing Ctrl+F5 (if you are prompted to install any modules, accept)
### From the Terminal
```bash
./[file].py
```

## Download
### Clone
#### Using The Command Line
1. Press the Clone or download button in the top right
2. Copy the URL (link)
3. Open the command line and change directory to where you wish to clone to
4. Type 'git clone' followed by URL in step 2
```bash
$ git clone https://github.com/[user-name]/[repository]
```


More information can be found at
<https://help.github.com/en/articles/cloning-a-repository>

#### Using GitHub Desktop
1. Press the Clone or download button in the top right
2. Click open in desktop
3. Choose the path for where you want and click Clone

More information can be found at
<https://help.github.com/en/desktop/contributing-to-projects/cloning-a-repository-from-github-to-github-desktop>

### Download Zip File

1. Download this GitHub repository
2. Extract the zip archive
3. Copy/ move to the desired location

## Community Files
### Licence
MIT License
Copyright (c) FredHappyface
(See the [LICENSE](/LICENSE.md) for more information.)

### Changelog
See the [Changelog](/CHANGELOG.md) for more information.

### Code of Conduct
In the interest of fostering an open and welcoming environment, we
as contributors and maintainers pledge to make participation in our
project and our community a harassment-free experience for everyone.
Please see the
[Code of Conduct](https://github.com/FHPythonUtils/.github/blob/master/CODE_OF_CONDUCT.md) for more information.

### Contributing
Contributions are welcome, please see the [Contributing Guidelines](https://github.com/FHPythonUtils/.github/blob/master/CONTRIBUTING.md) for more information.

### Security
Thank you for improving the security of the project, please see the [Security Policy](https://github.com/FHPythonUtils/.github/blob/master/SECURITY.md) for more information.

## Screenshots

### Desktop
<div>
<img src="readme-assets/screenshots/desktop/screenshot-0.png" alt="Screenshot 1" width="600">
<img src="readme-assets/screenshots/desktop/screenshot-1.png" alt="Screenshot 2" width="600">
<img src="readme-assets/screenshots/desktop/screenshot-2.png" alt="Screenshot 3" width="600">
</div>
