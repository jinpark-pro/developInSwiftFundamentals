# Develop in Swift Fundamentals

## Unit 1 Getting Started With App Development

### Lesson 1.1 Start Defining Your App

- Guide
  - App Design Workbook
    - Begin by opening the App Design Workbook and familiarizing yourself with the layout.
    - Read the Welcome pages to learn about how to use the workbook, Keynote, and the other resources you will need.
    - You’ll use the workbook to document your app design process and ideas throughout the course, so save it in an easy-to-find place on your device.
    - Also, remember that this course focuses on UIKit, so the SwiftUI coding exercises in the App Design Workbook are optional.
    - Use the App Design Workbook to complete the following exercises.
  - Discover
    - Think about your favorite app.
    - What’s its purpose? What problem(s) does it solve?
    - Assuming you’re thinking about a well-designed app, it’s probably fairly easy to answer these questions.
    - Many great apps focus on one particular type of user and one or two issues — and therefore have a very specific set of goals.
    - Use the Discover section of the App Design Workbook to begin identifying a challenge and the people it affects.
    - By the end of this part of the workbook, you’ll have a thorough understanding of a challenge and an insight into the people who would benefit from a solution.
  - Analyze
    - Now it’s time to dig a little deeper.
    - The more you understand the issue and audience, the more targeted the app will be — and the more likely it is that it will solve a problem that a group of users experiences.
    - Complete the Analyze section of the App Design Workbook. By the end of this stage, you’ll have a clearer picture of the form your app might take.
    - You’ll look at the root causes of your users’ challenges, and you’ll use them to drive feature ideas that take advantage of key iOS capabilities while contrasting your ideas with existing apps.
  - Coming Up
    - As you build your coding knowledge in the rest of this unit, you’ll regularly return to your app idea and think about how you might use what you are learning to make the app you care about come to life. Keep your App Design Workbook handy so that you can refer back to it and add notes to keep your app design ideas and plans moving forward.

### Lesson 1.2 Introduction to Swift and Playgrounds

- A Little History
  - At the Apple Worldwide Developers Conference 2014, Apple introduced Swift as a modern language for writing apps for iOS and macOS. Apple now has new platforms, including watchOS and tvOS, that also use Swift as the primary programming language.
  - Since the 1990s, most developers have written applications for Apple platforms in Objective-C, a language built on top of the C programming language. Objective-C is more than 30 years old, and C is more than 40 years old. Both languages have served the software developer community well. They won’t be going away in the foreseeable future.
  - However, Objective-C can be challenging to learn. Because technology has been advancing so fast in recent years, Apple saw the opportunity to create a more modern language that was easier to learn and easier to read, write, and maintain.
  - As you learn Swift, you may see the influence of its C and Objective-C heritage.
- A Modern Language
  - What’s a modern language? It’s one that’s safe, fast, and expressive. As Apple was designing Swift, those three primary goals were at the core of every decision. As you learn programming concepts in Swift, you’ll come to appreciate how each decision points to safety, speed, and clarity.
  - Some of the features that make Swift a modern language include:
    - Clean syntax, which makes code readable and easier to work with
    - Optionals, a new way of expressing when a value may not exist
    - Type inference, which speeds up development and allows the compiler to help identify common issues
    - Type safety, which enforces code that’s less likely to crash your program
    - Automatic Reference Counting (ARC) for memory management, which automatically handles some of the deeper technical challenges of native programming
    - Tuples and multiple return values, which allow smaller units of code to do more
    - Generics, which help developers write code that can be used in multiple scenarios
    - Fast and concise iteration over collections, making Swift a fast language
    - Structs that support methods, extensions, and protocols, which allow Swift to optimize for memory use and speed while providing flexibility for developers
    - Map, filter, reduce, and other functional programming patterns, which simplify code and streamline common actions that previously required multiple lines of code
    - Powerful error handling, which helps the developer write fewer bugs and better handle scenarios that could cause apps to crash or perform unexpectedly
  - At the moment, you’re probably not familiar with most of the concepts on the list. That’s OK. For now, just realize that they make Swift a great language to use for building applications. As you progress through this course, you’ll learn what each of these features means and how it’s relevant to writing safe, fast, and expressive code.
- A Safe Language
  - A number of features already mentioned make Swift a safe language by helping you write code that is less likely to crash your app. Computer programs are very literal, and so code written to handle one thing may not be capable of handling another. Type safety forces you to be explicit about the “type” of each object that you create, manipulate, and assign, and only lets you write code that the given object can handle. This prevents you from writing code that may crash if it is not designed to work with the “types” of objects you are referencing. Type inference similarly allows the compiler to infer the type of an object, thereby saving you time and again ensuring that the compiler can enforce proper rules regarding what operations and functions can be performed with each type. Optionals are somewhat unique to Swift, and allow you to better express when a value may not exist. This helps you ensure that your code can handle both scenarios where values exist and scenarios where they do not. Swift also provides for sophisticated error handling, which as the name implies, allows you to write code that can handle errors gracefully and simply.
- Open Source
  - In December 2015, Apple released the Swift language and supporting resources on GitHub as an open source project. Open source can mean a lot of things. The most important point to understand is that an open source language is developed in the open, with community input and support. Everyone is welcome to contribute or simply to follow along.
    -Open development means that Swift is evolving and improving. Over time, syntax may change and support will be added for more platforms, including delivering more Swift technology to Linux. Now that you’re learning Swift, you can be confident that your knowledge will become more and more valuable as the language continues to improve and as adoption grows across Apple platforms and beyond.
  - For more information about how to follow along or participate in building the Swift language, visit the project home page at Swift.org.
- Hello World

  - Terminal

    - macOS comes with a console app called Terminal, and Swift comes with a tool called a REPL, which stands for Read, Eval, Print Loop. The REPL allows you to enter simple commands, evaluate them, and print the result.

    - ```terminal
        swift repl
        print("Hello, world")
        :quit
      ```

  - Playground
    - One of the most important things announced with Swift was playgrounds, a special Xcode document type that runs Swift code in a simple format with easily visible results.
    - Working in playgrounds is preferable to working in a REPL for many reasons. For starters, they make writing Swift code fun and simple. Using a more familiar interface, you can type in a line of code and the results appear immediately in the sidebar. If your code runs over a period of time, you can watch the progress in the timeline.
    - Playgrounds can also be extremely useful for Swift developers. They make it easy to manage more code in one place and to see multiple results in the results sidebar. Developers often use playgrounds for prototyping their Swift code, then move it into an Xcode project after testing.

### Lesson 1.3 Constants, Variables, and Data Types

- Constants and variables associate a name (like age or name) with a value of a particular type (like the number 29 or the string “John”). You can then use the name to refer to that value many times in your program. Once it’s set, the value of a constant is immutable, which means that it cannot be changed. In contrast, the value of a variable is mutable, which means that it can be changed at any time.
  By defining a constant or variable, you’re asking the compiler to allocate storage for the value in memory on the device that will run the program. You’re also asking it to associate the constant or variable name with the assigned value so you can access the value later.

- **Constants**
  - When you want to name a value that won’t change during the lifetime of the program, you’ll use a constant.
  - You define constants in Swift using the `let` keyword, `let name = "John"`.
- **Variables**
  - When you want to name a value that may change during the lifetime of the app, you’ll use a variable.
  - You define variables using the `var` keyword., `var age = 29`.
- You can assign constants and variables from other constants and variables. This functionality is useful when you want to copy a value to one or more other variables.
- **Constant or Variable?**
  - You just learned to use a constant when the value won’t change and a variable when the value might change.
  - But there’s a nuance here that’s worth learning. Even though certain values might be variable, you can represent them with a constant because they won’t change during the lifetime of a single execution of the code.
  - Imagine you’re calculating information about the distance traveled on a trip. The program can be reused to track many trips over time, but it tracks one trip at a time. How would you represent the following data in your code?
    - Starting location
      - This is a GPS coordinate of where you started your trip. Once you begin tracking a trip in your program, the location won’t change. You’ll represent this value with a constant.
    - Destination
      - This GPS coordinate is where you want to arrive. Your app can be used for many destinations, so you may think this would be represented with a variable. But once your program begins tracking a trip, the destination won’t change. You’ll represent this value with a constant.
    - Current location
      - The GPS coordinate of your current location will change whenever you move. So you’ll represent this value with a variable.
    - Distance traveled
      - How far have you traveled from your starting point? This value changes as you move. You’ll represent it with another variable.
    - Remaining distance
      - How far must you travel to arrive at your destination? The remaining distance changes as you move. You’ll represent this value with a variable.
  - Constants and variables perform very similar jobs. You may think it would be easier to use variables for everything and ignore constants altogether. Technically your code could work this way.
  - So why should you use constants at all?
    - First, if you set a value to a constant, the compiler understands that it should never be changed.
      - This means you won’t be able to build or run your program if you try to change the constant’s value.
      - In this way, the compiler enforces safety.
    - Second, there are special optimizations that the compiler can make for constant values.
      - When you use constants for values that won’t change, the compiler can make low-level assumptions about how to store the value. These adjustments allow your program to execute faster.
    - Third, it’s the idiomatic, or accepted, way to do things in Swift.
- As you learn more about building software, you’ll come to appreciate best practices for consistently writing clean, readable code. This is especially important when working on a team with other developers. You’ll also discover that following best practices will make it easier for you to remember what your code does, especially when you want to make changes later on.
- If you want to be a great developer, you’ll need to follow shared patterns and conventions.
- **Naming Constants And Variables**
  - There are rules for naming constants or variables. The compiler enforces the rules, so you won’t be able to build and run your program if you break them.
    - Names can’t contain mathematical symbols.
    - Names can’t contain spaces.
    - Names can’t begin with a number.
  - Other than these three rules, you can name a constant or variable whatever you like.
  - In addition to the rules, there are some best practices for naming constants and variables:
    - Constant and variable names should be clear and descriptive, making it easy to understand the code when you come back to it later.
      - For example, `firstName` is better than `n` and `restaurantsNearCurrentCity` is better than `nearby`.
    - To be clear and descriptive, you’ll often want to use multiple words in a name. When you put two or more words together, the convention is to use **camel case**.
      - Lowercase the first letter in the name, and then capitalize the first letter of each new word.
      - You’ve probably noticed examples of this: defaultScore is the camel case treatment for combining default and score. Camel case is easier to read than all the words compressed together.
        - For example, `defaultScore` is clearer than `defaultscore` and `restaurauntsNearCurrentCity` is clearer than `restaurantsnearcurrentcity`.
      - Camel case also allows assistive devices to better delineate word boundaries.
- **Comments**

  - As code becomes more complex, it can be useful to leave little notes for yourself, as well as other developers who might read your code. These comments are created by placing two forward slashes in front of the text. When your code is compiled, the comments will be ignored, so write as many as you find helpful.

    - ```swift
        // Setting pi to a rough estimate
        let π = 3.14
      ```

  - If you need multiple lines for your comment, you can also place as much text as you’d like between /_ and _/ and it will be ignored by the Swift compiler.

    - ```swift
        /* The digits of pi are infinite,
        so instead I chose a close approximation.*/
        let π = 3.14
      ```

  - Comments are most frequently used to explain difficult sections of code, provide copyright information at the top of a file, and to provide dating information (when the file was created and/or modified).

- **Types**

  - Each constant or variable in Swift has a `type` that describes its kind of value.
  - Swift includes many predefined types you can use to more easily write clean code. Whether your program needs to include numbers, strings, or Boolean (true or false) values, you can use types to represent a specific kind of information.
  - Here are a few of the most common types in Swift.
    | Name | Type | Purpose | Example |
    |:---|:---|:---|:---|
    | Integer | Int | Represents whole numbers or integers | 4 |
    | Double | Double | Represents numbers requiring decimal points, or real numbers | 13.45 |
    | Boolean | Bool | Represents `true` or `false` values | true |
    | String | String | Represents text | "Once upon a time..." |
  - Swift also supports collection types, which group multiple values into a single constant or variable. One collection type is named an Array, which stores an ordered list of values. Another collection type is named a Dictionary, which has keys that help you look up specific values. You’ll learn more about collections in a future lesson.
  - The Swift standard library includes all the types above, so you can always use them.
  - “In addition, you can define your own types in Swift by creating a type definition. Consider a simple Person type:

    - ```swift
        struct Person {
          let firstName: String
          let lastName: String
         
          func sayHello() {
            print(”Hello there! My name is \(firstName) \(lastName).”)
          }
        }
      ```

  - You can think about a type definition as a blueprint. A blueprint designates how to construct a building but isn’t a building itself. However, you can create many buildings from a single blueprint.
  - A type definition declares the information it stores (properties) and its capabilities or actions (methods).
    - In this case, a `Person` stores `String` information in two properties, `firstName` and `lastName`, and has one action, the method `sayHello()`.
  - The example above describes how the type Person should look and perform. When you create a type and assign it to a variable or constant, you’re creating a version or instance of the type. Thus, an instance is a value. Consider the following code:

    - ```swift
        let aPerson = Person(firstName: “Jacob”, lastName: “Edwards”)
        let anotherPerson = Person(firstName: “Candace”, lastName:
        “Salinas”)
         
        aPerson.sayHello()
        anotherPerson.sayHello()

        Console Output:
        Hello there! My name is Jacob Edwards.
        Hello there! My name is Candace Salinas.
      ```

    - This code creates two instances of the Person type.
      - One instance represents a Person named Jacob Edwards, and the other instance represents a person named Candace Salinas.

- **Type Safety**

  - Swift is considered a type-safe language. Type-safe languages encourage or require you to be clear about the types of values your code can work with. For example, if part of your code expects an Int, you can’t pass it a Double or a String.
  - When compiling your code, Swift performs type checking on all your constants and variables and flags any mismatched types as errors. If you mismatch types, you can’t run your program.

    - ```swift
        let playerName = “Julian”
        var playerScore = 1000
        var gameOver = false
         
        playerScore = playerName
        // Will be flagged for mismatched types, will not compile.
      ```

  - Because type safety enforces the type a constant or variable can hold, assigning a String to a variable that only holds an Int doesn’t make sense. You’ll learn how Swift figured out the types shortly.
  - Type safety also applies to variables, constants, and literal values that represent data that may seem compatible. For example, Swift recognizes Int and Double as completely different types, even though they both represent numbers.

    - ```swift
        var wholeNumber = 30
        var numberWithDecimals = 17.5
         
        wholeNumber = numberWithDecimals
        // Will be flagged for mismatched types, will not compile.
      ```

  - In the case above, both variables are numeric types, but wholeNumber will be an Int and numberWithDecimals will be a Double. In Swift, you can't assign a value of one type to a variable of another type.
  - When working with numbers, you may find that you need to assign a very large value to a variable or constant. This can be difficult to read, since it is hard to see how many zeros there are in 1000000000. Fortunately, Swift allows you to put underscores in your numbers as a way of formatting for easier reading.

    - ```swift
        var largeUglyNumber = 1000000000
        var largePrettyNumber = 1_000_000_000
      ```

- **Type Inference**

  - You may have noticed that you don’t have to specify the type of value when you declare a constant or variable. This is called type inference. Swift uses type inference to make assumptions about the type based on the value assigned to the constant or variable.

    - ```swift
        let cityName = “San Francisco”
        // “San Francisco” is obviously a `String`, so the compiler
        automatically assigns the type of cityName to a `String`.
         
        let pi = 3.1415927
        // 3.1415927 is a number with decimal points, so the compiler
        automatically assigns the type of pi to a `Double`.
      ```

  - Once you assign a value to a constant or variable, the type is set and can’t be changed. This is true even for variables. The value of a variable may change, but not its type.
  - You might find cases where it’s useful, or even required, to explicitly specify the type of a constant or variable. This is referred to as a type annotation. To specify a type, add a colon (:), a space, and the type name following the constant or variable name.

    - ```swift
        let cityName: String = “San Francisco”
        let pi: Double = 3.1415927
      ```

  - You can use a type annotation with different number types. The Swift compiler will adjust the value to match the type.

    - ```swift
        let number: Double = 3
        print(number)

        Console Output:
        3.0
      ```

  - There are three common cases for using type annotation:

    1. When you create a constant or variable but haven’t yet assigned it a value.

       - ```swift
          let firstName: String
          //...
          firstName = “Layne”
         ```

    2. When you create a constant or variable that could be inferred as more than one type.

       - ```swift
          let middleInitial: Character = “J”
          // “J” would be inferred as a `String`, but we want a `Character`

          var remainingDistance: Double = 30
          // `30` would be inferred as an `Int`, but the variable should support decimal numbers for accuracy as the number decreases.
         ```

    3. When you write your own type definition.

       - ```swift
          struct Car {
          var make: String
          var model: String
          var year: Int
          }
         ```

- **Required Values**

  - Whenever you define a constant or variable, you must either specify a type using a type annotation or assign it a value that the compiler can use to infer the type.

    - ```swift
        var x
        // This would result in an error.”
      ```

  - Even when you use a type annotation, your code can’t work with a constant or variable if you haven’t yet assigned it a value.

    - ```swift
        var x: Int
        print(x)
        // This would result in an error.
      ```

  - Once the value is assigned, the constant or variable becomes available.

    - ```swift
        var x: Int
        x = 10
        print(x)
      ```

### Lesson 1.4 Operators

- **Assign A Value**

  - Use the `=` operator to assign a value. The name on the left is assigned the value on the right.
  - The `=` operator is also used to modify or reassign a value.
  - The following code declares a `shoeSize` variable and assigns `8` as its value. The value is then modified to 9:

    - ```swift
        var shoeSize = 8
        shoeSize = 9 // Reassigns shoeSize to 9
      ```

- **Basic Arithmetic**
  - You can use the `+`, `-`, `*`, and `/` operators to perform basic math functionality.
  - When you use the division operator (`/`) on `Int` values, the result will be an `Int` value rounded down to the nearest whole number, because the `Int` type supports whole numbers.
  - If you explicitly declare constants or variables as `Double` values, the results will include decimal values.
  - Make sure to use `Double` values whenever your code requires decimal-point accuracy.
- **Compound Assignment**
  - It's a better way to modify a value. You can use a compound assignment operator, which adds the `=` operator after an arithmetic operator: `+=`, `-=`, `*=`, and `/=`.
  - Compound assignment operators help you write cleaner, more concise code.
- **Remainder Operator**
  - Use the remainder operator (`%`) to quickly calculate the remainder from the division of two `Int` values.
- **Order of Operations**
  - Mathematic operations always follow a specific order.
  - Multiplication and division have priority over addition and subtraction, and parentheses have priority over all four.
  - The remainder operator has the same precedence as multiplication and division.
- **Numeric Type Conversion**

  - As you've learned, you can't mix and match number types when performing mathematical operations.
  - You can create a new type by prefixing the type you want to convert it.

    - ```swift
        let x = 3
        let y = 0.14
        let pi = Double(x) + y
      ```

    - `Double(x)` creates a new `Double` value from the `Int` value `x`, enabling the compiler to add it to `y` and assign the result to `pi`.

### Lesson 1.5 Control Flow

- You will write code that makes decisions about what lines of code should be executed depending on results of previously executed code. This is call control flow.
- In this lesson, you'll learn how to use logical operators to check conditions and to sue control flow statements (`if`, `if-else`, and `switch`) to choose what code will be executed as a result.
- **Logical and Comparison Operators**
  - Each if statement uses a logical or comparison operator to decide if something is true or false. The result determines whether to run the block of code or to skip it.
  - Here’s a list of the most common logical and comparison operators:
    | Operator | Type | Description |
    |:--:|:---|:---|
    | == | Comparison | Two items must be equal. |
    | != | Comparison | The values must not be equal to each other. |
    | > | Comparison | Value on the left must be greater than the value on the right. |
    | >= | Comparison | Value on the left must be greater than or equal to the value on the right. |
    | < | Comparison | Value on the left must be less than the value on the right. |
    | <= | Comparison | Value on the left must be less than or equal to the value on the right. |
    | && | Logical | AND - The conditional statement on the left and right must be `true`. |
    | || | Logical | OR - The conditional statement on the left or right must be `true`. |
    | ! | Logical | NOT - Returns the logical opposite of the conditional statement immediately following the operator. |
  - You can mix and match operators to create a Boolean value, or `Bool`.
  - Boolean values are either `true` or `false` and you can combine them with an `if` statement to determine if code should be run or skipped.
- **If Statements**
  - The most straightforward conditional statement is the if statement.
  - An if statement says that “If this condition is true, then run this block of code.” If the condition isn't true, the program skips the block of code.
  - In most cases, you’ll use an if statement to check simple conditions with only a few possible outcomes.
- **If-Else Statements**
  - By adding an else clause to an `if` statement, you can specify a block of code to execute if the condition is not `true`.
  - Bu using `else if`, you can declare more blocks of code to run based on any number of conditions.
- **Boolean Values**
  - You can assign the results of a logical comparison to a `Bool` constant or variable to check or access the value later.
    - `Bool` values can only be `true` or `false.
  - It's also possible to invert a `Bool` value using the logical NOT operator, which is represented with `!`.
  - In the same way, you can use the logical AND operator, represented by `&&`, to check if two or more conditions are `true`.
  - You have yet another option: the logical OR operator, represented by `||`, to check if either one of two conditions is `true`.
- **Switch Statement**
  - You’ve seen `if` statements and `if-else` statements that you can use to run certain blocks of code depending on certain conditions.
    - But a long chain of `if`, `else if`, `else if ... else` statements can become messy and difficult to read after a small number of options.
  - Swift has another tool for control flow known as a `switch` statement that’s optimal for working with many potential conditions.
  - A basic `switch` statement takes a value with multiple options and allows you to run separate code based on each option, or `case`.
    - You can also provide a `default` case to specify a block of code that will run in all the cases you haven’t specifically defined.
  - Any given `case` statement can also evaluate multiple conditions at once: `case "a", "e", "i":`.
  - When working with numbers, you can use interval matching to check for inclusion in a range: `case 0...9:`.
  - The `switch` operator is the right tool for control flow when you want to run different code based on many different conditions.
- **Ternary Conditional Operator**
  - An interesting (and very common) use case for an `if` statement is to set a variable or return a value.
    - If a certain condition is `true`, you want to set a variable to one value.
    - If the condition is `false`, you want to set the variable to a different value.
  - Because this situation is so common in programming, many languages include a special operator, known as a ternary conditional operator (`?:`), for writing more concise code.
    - Swift programmers generally leave out the word “conditional” and refer to this as simply the “ternary operator.”
  - The ternary operator has three parts:
    - A question with a `true` or `false` answer.
    - A value if the answer to the question is `true`.
    - A value if the answer to the question is `false`.
      - `condition ? true : false`
