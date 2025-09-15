## Define Your Role & Expertise Level

- I am a Senior Scala Big Data Developer working on large-scale distributed data processing.
- Explain like I'm a junior developer.
- Provide an advanced technical breakdown.
- As a Big Data Architect, I design distributed data pipelines. Explain how to build a scalable real-time streaming architecture using ...
- Add required imports if You provide code snippets
- Add required gradle dependencies if You provide code snippets

## Unit testing
### Thoughtbots
- I am a Senior Scala Big Data Developer want to generate unit tests for the method. 
  Follow Thoughtbot's best practices for writing clean, readable, and maintainable tests.

Requirements:

- Use Scalatest as the testing framework.
- Follow the AAA pattern (Arrange, Act, Assert) for clarity.
- Keep tests small, independent, and fast by avoiding unnecessary external dependencies.
- Tested function should return varialbe result or with prefix result. Input parameteres for the tested function should be input or with prefix input.
- Try to not Use mocks/stubs (e.g., Mockito or ScalaMock).
- Ensure edge cases and error handling are covered.
- Provide meaningful test names that describe the behavior

### Spark tests
- Use spark.implicits, use spark builtin functions.

## Use Real-World Context
- I am using Spark 3.4, Scala 2.12, and Apache Iceberg. I use Gradle as a build tool.
- Generates gradle for spark/scala data pipeline. It should has no modules, use plugins: idea,scala, shadow Jar

### Context base
Generate a short Javadoc/Scaladoc for the code below.
Focus on WHEN to call it (context), not what it does.

Include:

- When/Use/Skip (3 short lines)
- Preconditions (1 line)
- Effects/guarantees or perf/threading (1 line)
- If this is an SQL-facing function/UDF, add one minimal SQL example.
Style rules: active voice, no fluff, no restating the method/class name, no repeating types, wrap at ~80 chars, keep summary ≤6 lines before tags. Use @param/@return/@throws only if helpful; keep each tag to a terse phrase.

Context: <where in the pipeline this runs, typical caller, stage (e.g., “Spark
executor during map-side combine”, “Trino aggregation merge step”), data size,
latency/throughput expectations, null/NaN policy>
Code:


