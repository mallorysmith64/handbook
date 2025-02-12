---
title: Welcome to Jurassic Park
tags: ['c-sharp', 'console', 'enumeration', 'oop', 'linq']
---

In this assignment, you will be creating a console application that manages a zoo full of dinosaurs.

## Objectives

- Practice control structures.
- Practice data structures.
- Practice working with user data.
- Practice with LINQ.
- Practice with OOP concepts.

## Requirements

- Create a simple console application that manages the dinosaurs in your zoo.

### Setup

```shell
dotnet new sdg-console -o JurassicPark
```

### Explorer Mode

- Create a class to represent your dinosaurs. The class should have the following properties

  - `Name`
  - `DietType` - This will be "carnivore" or "herbivore"
  - `WhenAcquired` - This will default to the current time when the dinosaur is created
  - `Weight` - How heavy the dinosaur is in pounds.
  - `EnclosureNumber` - the number of the pen the dinosaur is in

- Add a method `Description` to your class to print out a description of the dinosaur to include all the properties. Create an output format of your choosing. Feel free to be creative.

- Keep track of your dinosaurs in a `List<Dinosaur>`.
- When the console application runs, it should let the user choose one of the following actions:
  - `View`
    - This command will show the all the dinosaurs in the list, ordered by `WhenAcquired`. If there aren't any dinosaurs in the park then print out a message that there aren't any.
  - `Add`
    - This command will let the user type in the information for a dinosaur and add it to the list. Prompt for the `Name`, `Diet Type`, `Weight` and `Enclosure Number`, but the `WhenAcquired` must be supplied by the code.
  - `Remove`
    - This command will prompt the user for a dinosaur name then find and delete the dinosaur with that name.
  - `Transfer`
    - This command will prompt the user for a dinosaur name and a new `EnclosureNumber` and update that dino's information.
  - `Summary`
    - This command will display the number of carnivores and the number of herbivores.
  - `Quit`
    - This will stop the program

### Adventure Mode

- Consider what to do in Add/Remove/Transfer if multiple Dinos have the same name. Should `Add` prevent that from happening? Should `Transfer` and `Remove` show the multiple Dinos and prompt the user which one to work with?

- Add an option to view the Dinosaurs acquired after a given date (to be given by the user).
- Add an option to view all the Dinosaurs in a given enclosure number.

### Epic Mode

- Learn how to read and write from a file. At the start of the program load all the dinosaurs from a file. When the program ends write out all the dinosaurs to the same file.
