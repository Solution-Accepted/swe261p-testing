# Week 3

Due: **Week 5, Wed. Feb. 5**

## Content

1. Fork your project into GitHub. Add all your team members to the forked project, add Prof. Jones and TA Maruf as collaborators.

2. Introduction. What is the tool that you are testing? What is its purpose? Any other aspects that are relevant: size in terms of LOC, languages that it is written in, etc.

    - What is the tool that you are testing:

      [Guava](https://github.com/google/guava)

    - What is its purpose:

      Guava is an open-source, Java-based library developed by Google. It facilitates the best coding practices and helps reduce coding errors. It provides utility methods for collections, caching, primitives support, concurrency, common annotations, string processing, I/O, and validations. This tutorial adopts a simple and intuitive way to describe the basic-to-advanced concepts of Guava and how to use its APIs.

    - Size in terms of LOC (Java):

      - Total Lines: *779857*
      - Source Code Lines: *513936*

    - Languages：

      Java, 100%

    - Flavors:

      - JRE flavor. (>= JDK 1.8)
      - Android flavor. (JDK 1.7 and Android)

3. Document its build. What did you need to do to get it built and running?

    - Build

      - IDE: IntelliJ IDEA
      - Build tool: Maven
      - [IntelliJ IDEA lets you manage Maven projects](https://www.jetbrains.com/help/idea/delegate-build-and-run-actions-to-maven.html)

    - Run

        - In a Maven project, open pom.xml and add following code:

          ```xml
          <dependency>
            <groupId>com.google.guava</groupId>
            <artifactId>guava</artifactId>
            <version>28.2-jre</version>
            <!-- or, for Android: -->
            <version>28.2-android</version>
          </dependency>
          ```

        - In a Gradle project like Android app, open /app/build.gradle and add

            ```gradle
            dependencies {
              // Pick one:

              // 1. Use Guava in your implementation only:
              implementation("com.google.guava:guava:28.2-jre")

              // 2. Use Guava types in your public API:
              api("com.google.guava:guava:28.2-jre")

              // 3. Android - Use Guava in your implementation only:
              implementation("com.google.guava:guava:28.2-android")

              // 4. Android - Use Guava types in your public API:
              api("com.google.guava:guava:28.2-android")
            }
            ```

4. Document the existing test cases (JUnit or otherwise). How do you run them?
5. Partitioning. Select a feature that allows for partitioning. Specify your partitions (and boundaries when appropriate) in English — describe them. Then, write new test cases in JUnit and document them and how they run.
