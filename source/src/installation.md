# Installation

1. Install the [.NET SDK](https://dotnet.microsoft.com/en-us/download) for your system.

1. Install the *blprnt* .NET tool.

    ```shell
    $ dotnet tool install --global blprnt
    ```

1. Run `blprnt` and verify that it works.

    ```shell
    $ blprnt

    Required command was not provided.

    Description:
      Client for Blprnt living specification server

    Usage:
      blprnt [command] [options]

    Options:
      --version       Show version information
      -?, -h, --help  Show help and usage information

    Commands:
      preview  Local preview of a spec
    ```

If you already have a specification, see [viewing a specification](./specification/viewing_a_specification.md).