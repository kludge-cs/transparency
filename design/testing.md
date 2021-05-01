# Testing

## Abstract

Our unit and integration test naming convention is structured like
a sentence. At KCS, we refer to this concept as "verbal testing". Having this
standardized enables us to write unambiguous, concise and understandable test
names that match how we would describe their expected outcomes.

We use conditions, statements, and commands.
Keywords should be written in uppercase, and everything else in lowercase,
similar to writing in assembly, or if English were a programming language.

For example,
- `GIVEN query parameters THEN THROW` -> if there are present query
  parameters, then the program should raise an error.
- `IF -v is set AND program is cat DO NOT MATCH anything` -> if `-v` is set and
  the program is `cat`, then the return value should not match "anything".

## Keywords

| Condition | Meaning                                       |
|-----------|-----------------------------------------------|
| `GIVEN`   | When the following element is present         |
| `IF`      | When the following certain condition is true  |
| `AND`     | When the following condition is also true     |
| `OR`      | If a prior or the following condition is true |
| `NOT`     | Negates the following condition               |

| Statement | Meaning                                 |
|-----------|-----------------------------------------|
| `THEN`    | The program should do the following     |
| `DO NOT`  | The program should not do the following |

| Command   | Meaning                                    |
|-----------|--------------------------------------------|
| `MATCH`   | The program should match an expected value |
| `THROW`   | The program should raise an error or panic |
