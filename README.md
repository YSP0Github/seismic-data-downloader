# 地震数据下载器

## 概述

**地震数据下载器** 是一个功能强大且多功能的工具，旨在帮助用户高效、准确地从各种来源获取地震数据。该工具非常适合研究人员、工程师以及任何从事地震事件分析的人员。

## 功能

### 1. 多源数据支持
- **支持多个地震台网**：访问来自全球和区域性地震台网的数据，包括IRIS、USGS、GEOFON等。
- **实时数据和历史数据**：下载实时和历史地震数据，以满足监测和研究的需求。

### 2. 灵活的时间和空间选择
- **时间范围选择**：指定精确的时间范围进行数据下载，包括具体日期、时间段或多个不连续的时间窗口。
- **空间范围选择**：根据地理坐标（经度、纬度、深度）下载数据，或通过选择台站、区域或国家获取数据。
- **基于事件的选择**：根据地震事件的参数（如震级、深度、位置）过滤并下载相关数据。

### 3. 支持多种数据格式
- **常见格式**：下载多种格式的地震数据，如MiniSEED、SAC、SEGY，以满足不同分析工具的需求。
- **自定义格式转换**：提供数据格式转换功能，允许用户在不同格式之间进行转换，或导出为特定软件所需的格式。

### 4. 网络参数选择
- **网络、台站、位置和通道选择**：允许用户通过选择具体的网络（如XA、IU）、台站代码、位置代码和通道代码来下载特定的地震记录。
- **通配符支持**：支持使用通配符（如`*`）选择多个台站、通道或位置，简化选择过程。

### 5. 下载管理与恢复
- **批量下载**：支持批量下载多个台站或多个时间段的数据，提高效率。
- **断点续传**：在网络中断或其他异常情况下，支持恢复下载，避免重复下载已完成的部分。
- **速度控制与限速**：允许用户控制下载速度，以减少对网络带宽的影响，或避免对数据源服务器的过度请求。

### 6. 数据校验与预处理
- **数据校验**：在下载完成后，自动检查数据的完整性和一致性，确保数据质量。
- **数据预处理**：提供基本的预处理功能，如滤波、去趋势、去均值等，以简化后续的数据分析流程。

### 7. 用户友好的界面与API
- **图形用户界面（GUI）**：提供直观易用的图形界面，方便用户快速设置参数并执行下载任务。
- **命令行工具**：为高级用户提供强大的命令行工具或脚本接口，支持自动化和批量操作。
- **API集成**：提供Python API，供用户在自己的程序或分析流程中集成数据下载功能。

### 8. 日志与报告功能
- **下载日志**：记录下载的详细日志，方便用户追踪下载过程中的问题或数据来源。
- **报告生成**：生成包含台站信息、时间段、数据格式等的下载报告，便于记录和后续分析。

### 9. 性能优化与资源管理
- **多线程或并行下载**：支持多线程或并行下载，以加快大规模数据的获取速度。
- **存储管理**：自动管理下载的数据存储，支持压缩存储或自动清理旧数据，以节省存储空间。

### 10. 文档与支持
- **详细的文档**：提供详细的使用说明、教程和FAQ，帮助用户快速上手并解决常见问题。
- **用户支持**：提供技术支持或社区支持，帮助用户解决遇到的各种问题。

## 安装

要安装地震数据下载器，请克隆此仓库并安装所需的依赖项：

```bash
git clone https://github.com/YSP0Github/seismic-data-downloader.git
cd seismic-data-downloader
pip install -r requirements.txt
```
## 使用方法
### 图形用户界面（GUI）
- 运行GUI应用程序：

```bash
python run_gui.py
```
- 设置参数并开始下载地震数据。

### 命令行界面（CLI）
- 使用CLI工具下载数据：

```bash
python download_data.py --network XA --station S12 --starttime "1973-12-10T08:30:00.000" --endtime "1973-12-10T16:30:00.000"
```
## API
```bash
from seismic_downloader import SeismicDataDownloader

downloader = SeismicDataDownloader()
downloader.download_waveforms(network="XA", station="S12", starttime="1973-12-10T08:30:00.000", endtime="1973-12-10T16:30:00.000")
```

## 贡献
我们欢迎来自社区的贡献。请阅读我们的贡献指南以了解如何开始。

## 许可证
该项目基于MIT许可证 - 详情请参阅LICENSE文件。

## 联系方式
如有疑问或需要支持，请通过以下邮箱联系我们: ysp@cug.edu.cn 或 york.stephen19@gmail.com 。




# Seismic Data Downloader

## Overview

The **Seismic Data Downloader** is a powerful and versatile tool designed to facilitate the efficient and accurate retrieval of seismic data from various sources. This tool is ideal for researchers, engineers, and anyone involved in the analysis of seismic events.

## Features

### 1. Multi-source Data Support
- **Support for Multiple Seismic Networks**: Access seismic data from a variety of global and regional networks, including IRIS, USGS, GEOFON, and more.
- **Real-time and Historical Data**: Download both real-time and historical seismic data to meet both monitoring and research needs.

### 2. Flexible Time and Space Selection
- **Time Range Selection**: Specify exact time ranges for data download, including specific dates, time periods, or multiple non-continuous time windows.
- **Spatial Range Selection**: Download data based on geographic coordinates (latitude, longitude, depth) or select by station, region, or country.
- **Event-based Selection**: Filter and download data based on seismic event parameters such as magnitude, depth, and location.

### 3. Support for Multiple Data Formats
- **Common Formats**: Download seismic data in various formats such as MiniSEED, SAC, SEGY, to cater to different analysis tools.
- **Custom Format Conversion**: Convert between different data formats or export in a format required by specific software.

### 4. Network Parameter Selection
- **Network, Station, Location, and Channel Selection**: Select specific networks (e.g., XA, IU), station codes, location codes, and channel codes to download targeted seismic records.
- **Wildcard Support**: Use wildcards (e.g., `*`) to select multiple stations, channels, or locations, simplifying the selection process.

### 5. Download Management and Recovery
- **Batch Download**: Download data from multiple stations or time periods in a batch, improving efficiency.
- **Resume Download**: Resume downloads after interruptions, avoiding the need to re-download already completed portions.
- **Speed Control and Throttling**: Control download speed to minimize impact on network bandwidth or to prevent excessive requests to data source servers.

### 6. Data Validation and Preprocessing
- **Data Validation**: Automatically check the integrity and consistency of data after download to ensure data quality.
- **Data Preprocessing**: Provide basic preprocessing features such as filtering, detrending, and demeaning to simplify subsequent analysis.

### 7. User-friendly Interface and API
- **Graphical User Interface (GUI)**: An intuitive GUI for users to easily set parameters and execute download tasks.
- **Command Line Tool**: A powerful command-line interface or script interface for advanced users, supporting automation and batch operations.
- **API Integration**: A Python API for integrating the data download functionality into your own programs or analysis workflows.

### 8. Logging and Reporting
- **Download Logs**: Detailed logs of the download process for troubleshooting and tracking the source of downloaded data.
- **Report Generation**: Generate reports that include station information, time periods, data formats, and more for documentation and analysis.

### 9. Performance Optimization and Resource Management
- **Multithreading or Parallel Downloading**: Supports multithreading or parallel downloading to speed up large-scale data retrieval.
- **Storage Management**: Automatically manage downloaded data storage, including compressed storage or automatic cleanup of old data to save space.

### 10. Documentation and Support
- **Comprehensive Documentation**: Detailed user guides, tutorials, and FAQs to help users quickly get started and resolve common issues.
- **User Support**: Technical support or community support to assist users in solving various problems they may encounter.

## Installation

To install the Seismic Data Downloader, clone this repository and install the required dependencies:

```bash
git clone https://github.com/YSP0GITHUB/seismic-data-downloader.git
cd seismic-data-downloader
pip install -r requirements.txt
```

## Usage
### Graphical User Interface (GUI)
- Run the GUI application:
```bash
python run_gui.py
```
- Set your parameters and start downloading seismic data.
### Command Line Interface (CLI)
- Use the CLI tool to download data:
```bash
python download_data.py --network XA --station S12 --starttime "1973-12-10T08:30:00.000" --endtime "1973-12-10T16:30:00.000"
```
## API
```bash
from seismic_downloader import SeismicDataDownloader

downloader = SeismicDataDownloader()
downloader.download_waveforms(network="XA", station="S12", starttime="1973-12-10T08:30:00.000", endtime="1973-12-10T16:30:00.000")
```

## Contributing
We welcome contributions from the community. Please read our Contributing Guide to get started.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For questions or support, please contact us at ysp@cug.edu.cn or york.stephen19@gmail.com.
