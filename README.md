# SpeedTest-PyPy for Home Assistant

[![GitHub Release][releases-shield]][releases]
[![HACS Supported][hacs-shield]][hacs]
[![License][license-shield]](LICENSE)

![Project Maintenance][maintenance-shield]

A custom component for Home Assistant that provides SpeedTest.net integration using PyPy for improved performance.

## Features

- Measures download speed, upload speed, and ping
- Server selection capability
- Automatic speed tests at configurable intervals
- Detailed server information in attributes
- Enhanced performance through PyPy implementation

## Installation

### HACS Installation (Preferred)
1. Ensure [HACS](https://hacs.xyz/) is installed in your Home Assistant instance
2. Add this repository to HACS as a custom repository:
   - Click on HACS in the sidebar
   - Click on the three dots in the top right corner
   - Select "Custom repositories"
   - Add `https://github.com/cociweb/hacs-speedtest-pypy` with category "Integration"
3. Click the "+ Explore & Download Repositories" button
4. Search for "SpeedTest-PyPy"
5. Click Install
6. Restart Home Assistant

### Manual Installation
1. Download the latest release from [GitHub](https://github.com/cociweb/hacs-speedtest-pypy/releases)
2. Extract the contents to your `/config/custom_components/speedtest_pypy` directory
3. Restart Home Assistant

## Configuration

### Through the UI
1. Go to **Settings** -> **Devices & Services**
2. Click the "+ ADD INTEGRATION" button
3. Search for "SpeedTest-PyPy"
4. Follow the configuration steps

## Available Sensors

| Sensor | Description | Unit |
|--------|-------------|------|
| `sensor.speedtest_pypy_ping` | Latency to the test server | ms |
| `sensor.speedtest_pypy_download` | Download speed | Mbps |
| `sensor.speedtest_pypy_upload` | Upload speed | Mbps |

### Sensor Attributes

Each sensor includes the following attributes:
- Server Name
- Server Country
- Server ID
- Bytes Received (download sensor only)
- Bytes Sent (upload sensor only)

## Options

In the integration options, you can:
- Select a specific SpeedTest server
- Configure the update interval

## Contributing

If you want to contribute to this project, please read the [Contributing Guide](CONTRIBUTING.md).

---

[releases-shield]: https://img.shields.io/github/release/cociweb/hacs-speedtest-pypy.svg
[releases]: https://github.com/cociweb/hacs-speedtest-pypy/releases
[hacs-shield]: https://img.shields.io/badge/HACS-Custom-orange.svg
[hacs]: https://github.com/hacs/integration
[license-shield]: https://img.shields.io/github/license/cociweb/hacs-speedtest-pypy.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2025.svg