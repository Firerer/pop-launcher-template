# Pop Launcher Plugin Template

This repository contains a template for creating plugins for the Pop!_OS Launcher. This specific implementation demonstrates a quicklinks plugin that allows users to quickly access predefined web links through the launcher.

## Overview

The quicklinks plugin enables users to search and open predefined web links directly from the Pop!_OS Launcher. It provides fuzzy searching capabilities and sorts results based on match quality.

This repo is based on [`pop-launcher-scripts`](https://github.com/pbui/pop-launcher-scripts) repo.


## Plugin Configuration (`plugin.ron`)

The plugin configuration defines the basic properties and behavior of the launcher plugin. Refer to the [Pop Launcher repo README](https://github.com/pop-os/launcher?tab=readme-ov-file#plugin-config) for more details.


## Usage

1. Enter the launcher (typically `Super + /` or `Super`)
2. Type `links` or `l` followed by your search term
3. The plugin will display matching links from its predefined collection
4. Select a result to open the corresponding URL in your default browser


## Adding New Links

To add new links, modify the `LINKS` tuple in the `quicklinks` script:

```python
LINKS = (
    ('Google', 'https://www.google.com'),
    # Add more links here in the format:
    # ('Description', 'URL'),
)
```

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/pop-launcher-plugin-template.git
   ```

2. Make the plugin script executable:
   ```bash
   chmod +x quicklinks
   ```

3. Copy the files to the Pop Launcher plugins directory:
   ```bash
   cp plugin.ron ~/.local/share/pop-launcher/plugins/quicklinks/
   cp quicklinks ~/.local/share/pop-launcher/plugins/quicklinks/
   ```

## Contributing

Feel free to contribute to this template by:
- Adding new features
- Improving the search algorithm
- Enhancing the documentation
- Reporting bugs
- Suggesting improvements
