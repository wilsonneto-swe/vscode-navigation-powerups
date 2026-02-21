# Navigation Power-ups - VS Code Extension

## Overview

**Navigation Power-ups** is a Visual Studio Code extension that enhances your `.http` file navigation experience by adding a left bar navigation tree. The extension provides an easy-to-use interface for jumping between sections and requests within your HTTP files.

## Features

- **Navigation Tree for .http Files**: Automatically builds a navigation bar for `.http` files, allowing for quick and easy access to different sections and requests within the file.
- **Real-time Updates**: The navigation tree updates automatically as you edit your HTTP files.

## Setup

1. **Install the Extension**: Search for "Navigation Power-ups" in the VS Code marketplace and install the extension.

2. **Open an HTTP File**: Open a `.http` file in your workspace, and the extension will automatically generate a navigation tree in the side panel. Each section or request will appear as a navigable node.

3. **Navigate Through the File**: Click on any node in the navigation tree to jump directly to that section or request in the file.

## How It Works

In `.http` files, the extension uses the number of `#` characters to differentiate between sections and requests:

- **Sections**: Any headers with more than three `#` characters (e.g., `#### Section`) are treated as higher-level sections.
- **Requests**: Headers with exactly three `#` characters (e.g., `### request`) are treated as individual HTTP requests.

#### Example of `.http` file structure:

![Http file example](./images/readme-httpfile-eg.png)

```http
#### Section

##### Subsection

### request
GET https://example.com HTTP/1.1

#### Section 2

### request
GET https://example.com HTTP/1.1

``` 

In this example, the navigation tree will display "Section" and "Section 2" as parent nodes, with each `GET` request listed underneath.


## License

This extension is licensed under the MIT License.
