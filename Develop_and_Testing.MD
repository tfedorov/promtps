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
# Prompt: Generate context-first Javadoc/Scaladoc

**Goal**  
Write a **single Javadoc/Scaladoc block** for the code I provide, focusing on
**context of use** (when/where/by whom), not what it does.

## Output rules
- Produce **only** the `/** ... */` comment (no extra text/code).
- **Active voice**. No fluff. Don’t restate class/method names. Don’t repeat types.
- Wrap lines at ~80 chars. Keep the summary ≤6 lines before any tags.
- Use `@param/@return/@throws` **only if they add real value**; keep each tag terse.

## Content to include (in order)
1. **Who** can call it (e.g., “Trino SQL authors / ETL jobs / Spark client ...”).  
2. **Where** it runs / **environment requirements** (infer from imports):
   - **Trino** (`io.trino.*`): mention **plugin installed and registered via
     `io.trino.spi.Plugin`**, and that it executes on **workers (partial)** and
     **coordinator (final)** during aggregation.
   - **Spark** (`org.apache.spark.sql.*`): mention **SparkSession created** and UDF/UDAF
     **registered**; specify whether it runs on executors during map/reduce/aggregate.
   - Otherwise: state the runtime container and any registration/init requirements.
3. **Side effects & runtime traits**: per-group state mutation (if any), memory/CPU
   profile (e.g., `~O(2^lgMaxK)`), determinism, thread confinement, and “no external
   I/O” if true.
4. If **SQL-facing**, add one minimal **SQL** example on its own line. If there’s an
   obvious optional tuning parameter (e.g., `lgMaxK`), add a second minimal SQL variant.

## Tone/format example to emulate
```java
/**
 * Trino SQL aggregate function.
 * Register via io.trino.spi.Plugin (plugin installed and enabled).
 * Usable in any Trino environment once the plugin registers this function.
 * Executes during aggregation (workers: partial; coordinator: final).
 * Consumes serialized HLL sketches (VARBINARY) and produces a serialized union.
 * Side effects: updates per-group union state; allocates memory (~2^lgMaxK);
 * no external I/O; deterministic.
 *
 * SQL: {@code SELECT col, hll_estimate(hll_merge(sketch_col)) FROM t GROUP BY col;}
 * SQL (with lgMaxK): {@code SELECT hll_estimate(hll_merge(sketch_col, 12)) FROM t;}
 */
