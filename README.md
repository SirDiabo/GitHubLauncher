# GitHub Launcher

[![.NET 9](https://img.shields.io/badge/.NET-9-512BD4)](https://dotnet.microsoft.com/)
[![License](https://img.shields.io/github/license/SirDiabo/GitHubLauncher)](https://github.com/SirDiabo/GitHubLauncher/blob/main/LICENSE)

GitHub Launcher is a neutral launcher shell for applications distributed through GitHub releases. It can track repositories, download release assets, check installed versions, launch local installs, and offer updates when newer releases are available.

## Features

- Download and install release assets from GitHub repositories
- Check local installs against the latest GitHub release
- Launch installed applications from a managed library
- Store launcher entries in an editable `games.json`
- Optional GitHub API token support for higher rate limits

## Getting Started

### Prerequisites

- .NET 9 Runtime
- Internet connection for GitHub API requests and release downloads

### Installation

1. Download the latest release from the [Releases](https://github.com/SirDiabo/GitHubLauncher/releases) page.
2. Extract the archive to your preferred location.
3. Run the executable.

## Configuration

### GitHub API Token

To avoid GitHub API rate limits, you can provide a personal access token in the launcher settings. A token with no special permissions is enough for public repositories.

### games.json Structure

The launcher uses a `games.json` file to manage entries. The file is organized into three categories: `standard`, `experimental`, and `custom`.

Each entry supports:

- `name`: display name in the launcher
- `repository`: GitHub repository in `owner/repository` format
- `folderName`: folder where the release is installed
- `gameIconUrl`: optional icon image URL

```json
{
  "standard": [
    {
      "name": "Example App",
      "repository": "owner/example-app",
      "folderName": "ExampleApp",
      "gameIconUrl": null
    }
  ],
  "experimental": [],
  "custom": []
}
```
