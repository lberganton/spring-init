# Spring Init

Spring Init is an interactive Bash script for generating Spring Boot projects.
It uses the [Spring Initializr API](https://docs.spring.io/initializr/docs/current/reference/html/#api-guide),
so it's bassicaly a shell version of [Spring Initializr](https://start.spring.io/index.html)

# Dependencies

- `curl`: for HTTP communication;
- `jq`: for JSON processment;
- `tar`: for extracting project file.

# How to use

```bash
springinit <path>
```

The objective of the script is to create a directory with your project. The `path` is an optional parameter. If provided, the
generated project directory will be placed in <path>. If not, the process working directory will be used.

When invoked, an interactive prompt appears, asking for inputs in this order:

1. Project type
2. Language
3. Group id
4. Artifact id
5. Project name
6. Package name
7. Packaging method
8. Java version
9. Dependencies

Some items will show all options availiable, example:

```
Packaging (jar war) [jar]:
```

The space-separated values in parentheses are the availiable options, the value in the square brackets is the default value, an
empty input will use the default value.

The dependencies must be a space-separated list of values. The availiable options can be shown with `-l`.
