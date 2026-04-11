# MineSweeper CLI

A command-line Minesweeper game built with **Test-Driven Development (TDD)** and the **Model-View-Controller (MVC)** architecture.

## Project Structure

```
minesweeper-tdd/
├── src/                                # Application source (MVC structure)
│   ├── App.java                        # Entry point: wires MVC components
│   ├── model/
│   │   └── MinesweeperModel.java       # Model: game logic, state, data
│   ├── view/
│   │   └── MinesweeperView.java        # View: CLI rendering and display
│   └── controller/
│       └── MinesweeperController.java  # Controller: input handling, game loop
├── test/                               # JUnit test suites
│   ├── MinesweeperModelTest.java       # Path testing, data flow testing, unit tests
│   ├── MinesweeperIntegrationTest.java # Bottom-up integration tests
│   └── MinesweeperValidationTest.java  # BVA, EC, decision table, state, use case
├── lib/                                # Dependencies
│   ├── junit-4.13.2.jar
│   └── hamcrest-core-1.3.jar
├── legacy/                             # Solution 1 reference code
│   └── Minesweeper.java
├── docs/                               # Documentation and diagrams
│   ├── Report.md
│   ├── Testing.md
│   └── img/
│       ├── use.png                     # Use Case Diagram
│       ├── seq.png                     # Sequence Diagram
│       └── class.webp                  # Class Diagram
└── README.md
```

## MineSweeper Presentation

Click below to watch our final presentation for this project.

[![Watch the demo](https://i9.ytimg.com/vi/QP_Nnw_cIgY/mqdefault.jpg?sqp=CNy_584G-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGGUgZShlMA8=&rs=AOn4CLCfJEU3lT8H6Zn6ri2jbGg9NbNXPQ)](https://youtu.be/QP_Nnw_cIgY)
---


## How to Build and Run

```bash
# Compile source (targeting Java 8 compatibility)
javac -d out --release 8 -sourcepath src src/model/*.java src/view/*.java src/controller/*.java src/App.java

# Run the game
java -cp out App
```

## How to Run Tests

```bash
# Compile tests (targeting Java 8 compatibility)
javac -d out --release 8 -cp "out:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar" test/*.java

# Run all 71 tests
java -cp "out:lib/junit-4.13.2.jar:lib/hamcrest-core-1.3.jar" org.junit.runner.JUnitCore MinesweeperModelTest MinesweeperIntegrationTest MinesweeperValidationTest
```

> **Note:** If you are using JDK 8, you can omit the `--release 8` flag.
> **Windows:** Replace `:` with `;` in classpath separators.

## How to Play

| Command       | Action                          |
|---------------|---------------------------------|
| `row col`     | Reveal the cell at (row, col)   |
| `f row col`   | Flag/unflag the cell            |
| `quit`        | Exit the game                   |

**Example:**
```
Enter move (row col) or (f row col) to flag: 3 4
Enter move (row col) or (f row col) to flag: f 2 2
Enter move (row col) or (f row col) to flag: quit
```

## Team Members

| Name                     | Student ID |
|--------------------------|------------|
| Glen Issac               | 200499313  |
| Shivam Jigneshbhai Soni  | 200474721  |
| Luka Dundjerovic         | 200494589  |
