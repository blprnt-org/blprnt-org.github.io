# Writing a Specification

Each *blprnt* specification is a directory of [markdown](./markdown_formatting.md) files.

It could be a directory with a single file, or it could be a deeply nested hierarchical structure with hundreds of directories and thousands of markdown files.

## Restaurant example

Imagine you are writing a specification for a restaurant. You start with a directory with a single document representing the specification. The file name should match the name of the directory. This is the title page of your specification:

```
/restaurant-specification
   restaurant-specification.md
```

You can add other files to a directory and they become sub-sections. Or you can add sub-sections by adding a subdirectory containing a file with the same name as the directory.

The restaurant will serve food, so you add a directory for food related specification.

```
/restaurant-specification
   restaurant-specification.md
   /food
      food.md
```

The restaurant will serve many cuisines, including burgers, so you add a sub-section for burgers:

```
/restaurant-specification
   restaurant-specification.md
   /food
      food.md
      burgers.md
```

The rendered specification will have a table of contents like:

> #### Table of Contents
> * <span style="text-decoration:underline">restaurant specification</span>
>   * <span style="text-decoration:underline">food</span>
>     * <span style="text-decoration:underline">burgers</span>

