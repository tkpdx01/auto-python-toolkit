# auto-python-toolkit

![Build Status](https://github.com/tkpdx01/auto-python-toolkit/actions/workflows/build-release.yml/badge.svg)

Create an out-of-the-box Python environment that supports offline development for your project, enhancing efficiency and simplifying your workflow.

auto-python-toolkit is a ready-to-use Python environment tailored for beginner developers. Whether working within an intranet or other offline settings, this toolkit simplifies the challenges of managing Python dependencies, environments, and versions. Key Features:

- **Offline-Friendly**: Fully supports creating and managing Python environments in offline scenarios.
- **Automation**: No need for in-depth knowledge of Python dependency or environment management—the toolkit handles the hassle for you.
- **Ready-to-Use**: Quick setup and no complex configurations, enabling you to start coding instantly.

## Quick Start

### Download

Download the latest release from [GitHub Releases](https://github.com/tkpdx01/auto-python-toolkit/releases).

### Usage

1. Unzip the toolkit to your project directory
2. Run the tool:
   ```
   python main.py
   ```
3. Follow the prompts to select your target OS and Python version

## Installation

### Prerequisites

1. Install `uv` by following the instructions at [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)
2. Make sure Python is installed on your system (for running this tool)

### Steps to create an offline environment

1. Clone this repository or download it to your project directory
2. Run the tool from your project root directory:
   ```
   python main.py
   ```
3. Select the target Windows version from the menu (supports Windows 7/10/11 and Windows Server 2016/2019/2022)
4. Select the Python version you want to use (all options are 3.7.9 or higher, as required by `uv`)
5. The tool will:
   - Download the selected Python version using uv
   - Analyze your project files to determine dependencies
   - Install dependencies using uv
   - Package everything together for offline use
6. The packaged project will be available in the `output` directory

### Command Line Options

```
python main.py --version          # Show version information
python main.py --auto             # Automatically use default Python version without prompting
python main.py --lang en          # Use English interface
python main.py --lang zh_CN       # Use Chinese interface
```

### Script Dependency Format

You can specify dependencies directly in your main script using this format:

```python
# /// script
# dependencies = [
#   "requests<3",
#   "rich",
#   "pandas",
#   "tqdm",
# ]
# ///
```

This will override any automatically detected dependencies.

## Supported Versions

### Windows Versions
- Windows 7 (64-bit)
- Windows 10 (32-bit and 64-bit)
- Windows 11 (64-bit)
- Windows Server 2016 (64-bit)
- Windows Server 2019 (64-bit)
- Windows Server 2022 (64-bit)

### Python Versions
This tool uses `uv` which supports Python 3.7 and above. Available versions:
- 3.7.9
- 3.8.20
- 3.9.21
- 3.10.16
- 3.11.11
- 3.12.9
- 3.13.2
- 3.14.0a6 (preview)

## How It Works

1. **OS Selection**: Choose the target Windows version for your offline environment
2. **Python Version Selection**: Choose the specific Python version you want to use
3. **Dependency Analysis**: The tool scans your Python files to detect imports and identifies the required packages
4. **Environment Creation**: Using `uv`, it creates a virtual environment with your selected Python version
5. **Package Installation**: Installs all detected dependencies into the virtual environment
6. **Project Packaging**: Packages the project with its environment for offline use

## Offline Usage

Once you've created the package:

1. Transfer the ZIP file to your offline environment
2. Extract the package
3. Run the `run_project.bat` file to activate the Python environment
4. You now have a fully functional Python environment with all dependencies ready to use!

## Internationalization Support

The tool supports both English and Chinese interfaces:

- Automatically detects your system language
- Can be manually specified with the `--lang` parameter
- Full i18n support for all menus and messages

## Contributing

Contributions are welcome! See [RELEASE.md](RELEASE.md) for information about the release process.

To contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Use Cases

- Intranet development
- Offline project deployment
- Python beginner learning
- Corporate environments with restricted internet access

## Chinese Description

auto-python-toolkit 是一个专为初阶开发者设计的开箱即用 Python 环境解决方案。无论您是在内网还是其他离线环境中工作，这个工具可以帮助您轻松应对 Python 依赖、环境以及版本管理的难题。 

核心特点：
- **离线开发友好**：完全支持在离线环境中创建和管理 Python 环境。
- **自动化处理**：无需对 Python 依赖和环境配置深入了解，工具会为您处理繁琐步骤。
- **开箱即用**：快速启动，无需复杂设置，即可开始开发。

### 支持的版本

#### Windows版本
- Windows 7 (64位)
- Windows 10 (32位和64位)
- Windows 11 (64位)
- Windows Server 2016 (64位)
- Windows Server 2019 (64位)
- Windows Server 2022 (64位)

#### Python版本
本工具使用`uv`，仅支持Python 3.7及以上版本。可用版本包括：
- 3.7.9
- 3.8.20
- 3.9.21
- 3.10.16
- 3.11.11
- 3.12.9
- 3.13.2
- 3.14.0a6 (预览版)

### 新增功能

- **Python版本选择**：可以选择特定的Python版本，而不仅限于系统的默认版本
- **多语言支持**：支持中英文界面，可根据系统语言自动切换或手动指定
- **脚本依赖声明**：可以直接在脚本中声明项目依赖，无需手动管理requirements.txt

### 命令行选项

```
python main.py --version          # 显示版本信息
python main.py --auto             # 自动使用默认Python版本，不显示选择菜单
python main.py --lang en          # 使用英文界面
python main.py --lang zh_CN       # 使用中文界面
```

### 使用方法

1. 在有网络的环境中运行此工具
2. 选择目标Windows版本和Python版本
3. 工具会自动下载Python、分析依赖并打包
4. 将生成的zip包复制到离线环境
5. 解压后运行run_project.bat即可激活Python环境

适用场景：内网开发、离线环境项目部署、Python 初阶入门学习。
