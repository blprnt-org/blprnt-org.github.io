# Viewing a Specification

To view a specification

1. Change to a directory containing:

    * a single markdown file OR
    * a markdown file with the same name (plus .md) as the directory

    E.g.

    ```
    /restaurant-specification
       restaurant-specification.md
    ```

1. Launch *blprnt*

    ```shell
    $ blprnt preview
    ```

1. Open a browser to `http://localhost:5000`

The location of the specification directory can alternatively be specified as the command line argument `specs`:

```shell
$ blprnt preview --specs "/Users/bill/restaurant-specification"
```

