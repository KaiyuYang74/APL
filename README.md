## API Query Language

AQL (API Query Language) aims to help with common frustrations encountered when interacting with web APIs. AQL streamlines the process of making API requests, handling responses, and implementing logic based on those responses. We aim to make this process better for our target users, backend developers (of all levels of experience).

AQL provides a straightforward, readable syntax for making API requests, handling data, and implementing control flow logic. This is done through the features below:

- **Simplified Requests**: abstracts the complexity of GET, PUT, POST, or DELETE request. You simply specify the command and the URL. Optionally, you can include a body, headers, authorizations, etc. with the request. By default, the { key, value } will be counted as body unless the key is specified with a special keyword “AQL@”.

- **Variable Management**: allows you to set data (like strings, integers, JSON, or API responses) to variables for later usage, simplifying state management and data manipulation.

- **Control Flow Logic**: allows the usage of loops and conditional that is similar to most other popular languages.

There are other features for more convenience: for example, you can access the first key and value from a JSON variable using a special property-name, all-caps “.AQLKEY” and “.AQLVALUE”

## Prerequisites

Before you begin, ensure you have the following installed:

- [Java](https://www.java.com/en/), [JDK](https://openjdk.org/) JDK 19 or newer
- [Gradle](https://gradle.org/install/) 7.0 or newer

### Using Gradle

- Build the project using Gradle.

  ```sh
  gradle build
  ```

- To run the application, execute the following command:

  ```sh
  gradle run
  ```

- To run tests, use the following command:

  ```sh
  gradle test
  ```

### Trouble shoot

- Please try JDK 21, if you encounter any issues.

## Project Structure

- `src`: Contains the source code for AQL.
  - `ast`: Code for abstract syntax tree structures and related classes.
  - `main`: Entry point of the application, GUI, and related classes.
  - `controller`: Controller classes which includes, Visitor, Evaluator, and other Helper.
- `test`: Unit Tests (visitor & evaluator), Regression Tests, Integration & End-to-End Tests.
- `lib`: External libraries used by the project.
- `AQLParser` & `AQLLexer`: ANTLR4 grammar files for AQL.
