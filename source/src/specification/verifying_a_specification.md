# Verifying a Specification

In a verified specification, each assertion is linked to an automated test that verifies that assertion.

The automated tests can be created with any testing library, and run with any test runner, so long as the output file is in one of the formats that *blprnt* understands.

To verify a specification:

1. **Identify an assertion to verify.**

    The [Guessing Game Demo specification](https://github.com/blprnt-org/guess-demo/blob/main/GuessingGame/Guessing%20Game%20Specification/Guessing%20Game%20Specification.md) includes the assertion `The user must enter a valid, whole number`.

2. **Write a test that verifies the assertion.**

    The [Guessing Game Demo `UserInputTests`](https://github.com/blprnt-org/guess-demo/blob/main/GuessingGameTests/UserInputTests.cs) includes a test `WholeNumbersInRangeAreValid` that verifies the valid, whole number assertion (this is C# and the xUnit testing framework):

    ```csharp
    [Fact]
    public void WholeNumbersInRangeAreValid()
    {
        foreach (var i in Enumerable.Range(1, 10))
        {
            Assert.NotNull(_engine.Parse(i.ToString()));
        }
    }
    ```

3. **Link the specification assertion to it's test.**

    There are two types of document selections that can be linked to tests.

    ##### Block Containers

    Block containers are delimited by `:::` followed by a new line. For example,

    ```
   :::
   Block markdown content
   :::
    ```

    ##### Inline Containers

    Inline containers are delimited by `::`, and occur inline.

    ```
    This paragraph contains ::an inline container:: as well as some other text.
    ```

    To link a container, block or inline, to a test add metadata to the closing delimiter. The metadata format is `{grep='NameOfTestGoesHere'}`. If your test output file includes a test with a name that contains `NameOfTestGoesHere` then it will be linked to the container.

    ```markdown
    This paragraph ::contains an inline container::{grep='NameOfTestGoesHere'} as well as some other text.
    ```

    The verified specification:

    ![A verified specification](../gamespecverified.png)