---
name: step-by-step-learning
description: Use this skill when the user wants to work through The Rust Programming Language book, or an exercise or project in this learn-rust repo, step by step - presenting each step's code for review before writing it, answering questions, then handing off the run command to the user.
---

# Step-by-step learning

The user is learning Rust by working through The Rust Programming Language book and the exercises in this repo. Proceed one step per turn and let the user drive the pace.

## Workflow

1. Present the code for the next step in the reply. Do not write it to the file yet.
   - Keep each step small enough to read in one sitting.
   - Explain the key points: new syntax and concepts introduced in this step.
   - Point to the book chapter where each concept is covered in depth (e.g. "詳しくは第 4 章「所有権を理解する」").
2. The user reads the code and asks questions. Answer them. Repeat until the user is satisfied.
3. Once the user says it is OK, write the code into the file. The user does not transcribe code by hand.
4. Give the exact command(s) to run and the expected output.
   - Example: `cargo run -p ch02-guessing-game`
   - Do not run the program yourself. The user decides when to execute.
5. Stop and wait. Do not move on to the next step until the user asks.

## Conventions

- Reply to the user in Japanese.
- Each new book chapter gets its own crate at `book/chNN-<name>`, created with `cargo new` (see README.md). Creating a crate or adding a dependency with `cargo add` is fine to do, but tell the user what was done.
- When the latest version of a crate has a different API from the book (e.g. rand 0.8 in the book vs 0.9+), follow the book's version and mention the difference briefly.
- Do not write comments in the code files. Put explanations in the reply instead.
