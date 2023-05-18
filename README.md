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

### Lesson 1.6 Xcode

- To begin your exploration of the Xcode IDE, you'll need to create a new project. Open Xcode and select "Create a new Xcode project."
- On the next screen, you'll see that Xcode provides many starting templates for creating new applications, sectioned according to the platforms that Xcode supports: iOS, watchOS, tvOS, and macOS.
  - Select the iOS App template. Click Next.
- Enter Product Name, Set Interface to "Storyboard", set Language to "Swift", Leave Use Core Date and Include Tests unselected. Click Next.
- Select a location for saving your project and click Create.Until you work with a version control system, such as Git, you can leave the box that asks if you’d like to create a git repository unselected.
- Now that you’ve created the project, you’ll arrive at the main interface of Xcode. You’ll notice that it takes up a lot of space. You might want to resize the window to fill the majority of your desktop—or take Xcode full-screen by clicking the green circle in the upper left of the window or using the Command-Control-F keyboard shortcut.
- **Xcode Interface**

  - The Xcode workspace is divided into five main sections. Click each call out to see more information.
  - <img src="./resources/xcode_interface.png" alt="Xcode Interface" width="600" />

  1. Editor Area

     - <img src="./resources/editor_area.png" alt="Editor Area" width="600" />

       1. The first is the editor area, where you spend most of your time writing Swift code and building UIs using Interface Builder.
       2. The file you select in the Project navigator column on the left determines what's displayed in the editor area.
       3. When you edit code, an overview of the entire file optionally appears on the right. This overview is the minimap (choose Editor > Minimap from the menu bar). This overview is the min map. You can interact with the minimap to navigate your source code quickly.

     - Jump Bar

       - Above the editor area is the jump bar, which contains the following controls from left to right
       - <img src="./resources/jump_bar.png" alt="Jump Bar" width="600" />

         1. Related Items - Allows you to navigate to various related items for the file you're currently editing.
         2. Go Back/Forward - Navigation buttons to move back and forth through your navigation history within the editor. This includes navigation actions such as jumping between definitions within a file and moving between different files.
         3. Path - A breadcrumb style control showing you the current editing context relative to tis parent groups and folders in the project. Click on any item in this control to navigate to other items at the same level. Note that the farthest right item navigates the structure within the file. (It might say "No Selection.")
         4. Code Review - Displays side-by-side views of the current version and other versions if you're using a source control system, such as Git, to manage your Xcode files.
         5. Adjust Editor Options - Allows you to change the options of the current editor as well as create an Assistant Editor that appears alongside your current editor with related files. Most useful when referencing other source files and when creating connections between source code and Interface Builder.
         6. Add Editor - Allows you to add an additional editor to the window - much like the assistant editor. By default this will add an editor to the right. By holding the Option key you can add an editor below. Once multiple editors are present two new buttons appear at the very left of the jump bar. One that closes the editor and another that focuses the editor - causing it to hide all others. Using multiple editors is an advanced feature that can greatly improve productivity when referencing and editing multiple files.

  2. Toolbar Area

     - Next is the toolbar, which spans the top of the Xcode workspace.
     - Moving from left to right are the following buttons:
       - <img src="./resources/toolbar.png" alt="Toolbar" width="600" />

  3. Navigator Area

     - The third section is the Navigator area, a narrow column on the left. At the top of the column is the project jump bar, which allows you to select which navigator is displayed.
     - <img src="./resources/navigator.png" alt="Navigator" width="600" />

       1. Project navigator - Lists all files associated with your project.
       2. Source Control navigator - Displays information about your project's Git repository if one is set up.
       3. Symbol navigator - Lists all the symbols, or data types, you've defined in your project. Since a single file can contain multiple symbol definitions, use this navigator when you're unsure which file a symbol defines.
       4. Find navigator - Allows you to perform a search for specified text throughout your project, with the option to also replace the text.
       5. Issue navigator - Displays all the warnings or build errors that were encountered the last time your app was built.
       6. Test navigator - Lists all the tests that you've written for your application and allows you to run each test individually.
       7. Debug navigator - Displays the order in which the code was executed when you're actively debugging an app.
       8. Breakpoint navigator - Lists all the breakpoints you've added to your project and makes it easy to enable or disable them individually.
       9. Report navigator = Provides a detailed log of each build of your project.

  4. Debug Area

     - At the bottom of the Xcode window is the fourth main section: the debug area.
     - To the left of this area is the variables view, which lists the value of each variable while you're actively debugging an app. To the right is the console pane, which displays any `print` statements you or the system has output. Each of these views can be shown or hidden using the button in the bottom right.
     - <img src="./resources/debug_area.png" alt="Debug Area" width="600" />

  5. Inspector Area
     - Finally, the Inspector area is a context-sensitive pane that displays details about any file selected in the Project navigator, such as the file's location on disk or the apps in which the file is included. When you're using Interface Builder, you'll find that this area is particularly useful for adjusting the attributes of your UI elements, including position, size, and color.

- **Xcode File Types**

  - Xcode knows how to work with a variety of files that span across multiple programming languages.
    - For now, you'll learn about files related to projects written in the Swift language.
    - The files in your project have filename extensions that you might see in the Finder, such as .swift and .xcodeproj, which Xcode doesn't show by default.
    - Instead, it uses icons to indicate the file type.
  - At the very top of the Project navigator, you'll see a file with a tiny blue Xcode icon.
    - <img src="./resources/xcode_icon.png" alt="Xcode Icon" width="20" />
    - Click the file to open it in the editor area.
    - This is the project file, which includes all the settings for your project and its targets.
    - Each target is a product that Xcode can build from the project.
    - For now, the targets you'll build will be executable apps.
    - Later, you may use targets to build frameworks, different versions of a particular app, or versions for different platforms like watchOS or tvOS.
  - The particular project you’re working with has only one target: an iOS app.

    - Within the project file, you can change all the details of a particular target.
    - For example, under Deployment Info, you can specify which version of iOS your code must support, change which devices your app is intended to run on, or show/hide the status bar. (1)
    - <img src="./resources/deployment_info.png" alt="Deployment Info" width="600" />

  - By selecting Signing & Capabilities at the top of the pane, you can configure code signing, which is a requirement for deploying to devices or the App Store. (1)
    - From this screen, you can also enable different features within the selected target.
    - For example, if your application needs to accept push notifications, you can add the Push Notifications capability and Xcode configures everything necessary for your app to receive notifications from the Apple Push Notifications service.
    - You can add capability configurations by clicking the + Capability button. (2)
  - Some capabilities have configuration options that you can disclose by clicking the triangle next to them.
  - <img src="./resources/signing_capabilities.png" alt="Signing and Capabilities" width="600" />

  - <img src="./resources/swift_icon.png" alt="Swift Icon" width="20" />

    - Files with this icon contain Swift code, as you'd expect.
    - Whenever you build your app, Xcode gathers up all included Swift files and runs them through the Swift compiler, which converts the code into a format your selected device understands.

  - <img src="./resources/storyboard_icon.png" alt="Storyboard Icon" width="20" />

    - This icon represents a storyboard.
    - All storyboard files are unique to Interface Builder.
    - They contain information about the design of each scene within your application, as well as how one screen transitions to another.

  - <img src="./resources/asset_icon.png" alt="Asset Catalog Icon" width="20" />

    - This icon represents an asset catalog.
    - In an asset catalog, you can manage many different kinds of assets.
    - This includes your app's icon, images, color definitions, and other forms of data to be bundled with your app.
    - An asset catalog also allows you to specify variants of your assets based on device settings and capabilities such as light and dark appearance, accessibility settings for high and low contrast, and hardware differences from screen resolutions to memory capacity and graphics chip support.

  - <img src="./resources/list_icon.png" alt="List of Properties Icon" width="20" />

    - This icon represents a file containing a list of properties and settings for your app.
    - Xcode provides a special interface for editing this file so that you rarely need to interact with it directly.
    - These settings are organized on various screens that you can find when you select the project file you learned about earlier.

- **Keyboard Shortcuts**

  - As you become more proficient with Xcode, you’ll discover that it’s much faster to execute tasks using keyboard shortcuts. Make sure to learn the most common shortcuts right away:
    - Command-B: Build the project
    - Command-R: Build and run the project
    - Command-.: Stop building or running
    - Command-/: Toggle comments on selected rows of code
    - Command-[: Shift the selected code left
    - Command-]: Shift the selected code right
    - Control-I: Reindent the selected code
    - Command-0: Show and hide the Navigator area
    - Command-⬆️: Move to the top of a file
    - Option-Command-0: Show and hide the Inspector area
  - To learn more keyboard shortcuts, look on the right side of any menu, or choose Xcode > Preferences from the menu bar and select Key Bindings at the top of the window.

- **Xcode Preferences**
  - Xcode is a powerful tool with many options. As you work with Xcode you'll learn more about what it can do and how you can customize it to work how you want it to.
  - Check out the Xcode Preferences by choosing Xcode > Settings from the menu bar. You can use the Preferences to add developer accounts, customize navigation or fonts, or choose certain behaviors when text editing and more.
  - Open Xcode Preferences and navigate to the Fonts & Colors pane.
    - You can choose a new theme, or set of colors and fonts, by selecting different options in the list on the left. Some themes have a suffix of "(Light)" or "(Dark)." These variants are used respectively based on the system's current light or dark appearance.
    - Xcode also allows you to override its appearance behavior independent of the system setting from the General pane.
  - To read more about Xcode and its various tools, read the Xcode Help documentation by choosing Help > Xcode Help from the menu bar.

### Lesson 1.7 Building, Running, and Debugging an App

- **Building and Running**
  - When creating a project, make sure the interface option is set to Storyboard.
    - You'll be presented with the Xcode workspace. Locate the Scheme menu on the Xcode toolbar, then choose the device you want to simulate from the list.
    - Click the Run button ▶️, or use the keyboard shortcut (`Command-R`) to begin launching the app in Simulator.
  - After Simulator has launched, you should see a device image with a white background. ​To rotate the image from portrait to landscape orientation, use the keyboard shortcuts `Command-Left Arrow` and `Command-Right Arrow`.
  - The simulator image may appear quite large, depending on the screen resolution of your Mac and the device you chose to simulate.
  - From inside the Simulator application, you can use keyboard shortcuts, from `Command-1` to `Command-3`, to scale the device image up or down.
    - If you're using an older Mac, you may want to select an older lower-resolution device, such as an iPhone SE, to reduce the total impact of the Simulator on your system.
  - To quit Simulator, use the keyboard shortcut `Command-Q`. Or just go back to Xcode.
  - Simulator doesn't work for all portions of an app. Certain interactions depend on the actual physical device to run.
    - For example, if you try to use Simulator to test an interaction with the Camera app, the program will crash. If your code depends on other hardware components that don't exist on a Mac — maybe an accelerometer, a gyroscope, or a proximity sensor — you'll want to test with an actual device.
  - Simulator also has some software limitations.
    - For example, push notifications can be delivered only to physical devices, and the MessageUI framework — which helps compose email and text messages — is incompatible with Simulator. If you're running into a lot of issues in Simulator, try testing the code on your iPhone or iPad. Your issues may be resolved.
  - Simulator runs on a Mac, many of which are built on the Intel "x86-64" architecture, but iOS devices are built on the ARM (Advanced RISC Machine) architecture.
    - This means there can be underlying (and sometimes subtle) differences in how your app works.
  - Overall, Simulator works well when you're developing and debugging apps, but you should always test your code on actual hardware.
- **Using A Personal Device**
  - The beauty of mobile apps is that you can take them anywhere. You may find that you want to share your programming progress with friends and coworkers. But before you can begin running your code on a physical device, you must have an account on the Apple Developer website. Accounts are free, so don’t worry.
  - Using a web browser, go to developer.apple.com and click Account. You can sign up using your existing Apple ID. If you don’t have an Apple ID, go ahead and create one — it’s also free.
    - Once you’ve entered your Apple ID, your developer account is good and you can head on back to Xcode.
      - With a free account, you can run your iOS apps on only one physical device. To distribute your apps to multiple devices or publish them to the App Store, you need to enroll in the Apple Developer Program.
  - Now, you need to tell Xcode about your new developer account. Open Xcode Settings using the keyboard shortcut `Command-Comma` (or choose Xcode > Settings from the Mac menu bar), and then select the Accounts button near the upper-left corner. Click the “+” button in the lower-left corner and choose Add Apple ID from the menu.
    - After entering your credentials, you're ready to run and debug apps on a physical iOS device.
  - Connect your iOS device to your Mac using the appropriate USB cable. Xcode will automatically download the necessary information from the device and will display its name in the Scheme menu. Choose the name of your physical device — which will typically be at the top of the list, before the device simulators.
  - Build and run the app again. You may receive a prompt asking you to trust the developer certificate. Follow the instructions within the alert to allow the device to run your apps.
  - Build and run once more, and you should see the same simple white screen on your iOS device.
    - To stop the app from running, click the Stop button near the left end of the Xcode toolbar (or use the Command-Period keyboard shortcut).
  - Building and Running Wirelessly
    - Xcode also gives you the option of deploying an app to your device over your network.
    - To do this, connect your iOS device to your Mac using the appropriate USB cable, and open the Devices and Simulators window by selecting Devices and Simulators from the Window dropdown.
    - Ensure that your device is selected in the list farthest to the left in the Devices and Simulators window. Check the Connect via network box.
  - If your device is on the same network as your Mac, you’ll see a globe appear next to your device’s name within a few moments. This indicates that your device is wirelessly connected.
  - You can now disconnect the USB cable connecting your device to your Mac, and build and run your app wirelessly.
  - In most cases, the above steps are sufficient for wireless pairing.
    - However, if this doesn’t work for you, you might be on a corporate or institutional network where the system administrator has put in place certain network restrictions.
    - In this case, open the Devices and Simulators window,
    - hold Control and click your device,
    - then click Connect via IP Address in the menu presented.
    - You then need to find your device's IP Address from your device's Settings, enter it in the prompt, and click Connect.
    - This should successfully pair your device. If you run into problems with wireless debugging, you can always pair over a USB cable.
- **Debugging An Application**

  - Even the best developers struggle to write perfect code. Debugging is the process of identifying and removing problems that may arise in your app. Xcode provides tools to help you through this process.
  - When you run an app as described above, either on Simulator or on your device, Xcode will connect the app to its debugger.
  - This allows you to watch the execution of your code in real time, stop code execution using breakpoints, print information from your code to the console, and much more.
  - As you proceed through this course, you’ll encounter three types of issues: warnings, compiler errors, and bugs.
  - **Warnings**
    - Warnings are the simplest kinds of issues to fix. They’re generated whenever your code is built, but they don’t prevent your program from successfully compiling and running. Some of the conditions that can throw a warning include:
      - Writing code that never gets executed
      - Creating a variable that never changes
      - Using code that’s out of date (also known as deprecated code)
    - Take a look at a warning. Back in Xcode, select ViewController in the Project navigator and, in the editor area, add the following line of code just below `super.viewDidLoad()`: `let x = 4`
    - This code assigned a value of `4` to a constant named `x`.
    - Build your application using `Command-B`. You should see a yellow caution sign with an explanation on the line you just added.
      - `Initialization of immutable value 'x' was never used; consider replacing with assignment to '_' or removing it`
      - Xcode will do its best to explain the warning in a straightforward way.
      - The compiler is telling you that it created `x` but, because it's not used in a meaningful way, you can remove it. Delete the line and rebuild to remove the warning.
  - **Compiler Errors**
    - An error is indicative of a more serious issue — for example, invalid code (such as a typo), improperly declaring a variable, or improperly calling a function.
    - Unlike a warning, an error prevents the code from ever being executed.
    - Simulator won’t even launch if your code has an error.
    - Here’s a look at two different errors in the making.
      - In ViewController, remove the open and closing parenthesis on the end of `super.viewDidLoad()`, leaving `super.viewDidLoad`. Beneath this line of code, write `navigationController.title = “Debugging”`.
    - After you build the app, you'll see two red error symbols with explanations on the lines you just updated.
      - <img src="./resources/compiler_errors.png" alt="Compiler Errors" width="600" />
      - <img src="./resources/compiler_errors_2.png" alt="Compiler Errors 2" width="600" />
      - The first error has an icon with an "X" in the center. Xcode provides a message that can help you identify the issue. The compiler expected to see an open and closing parenthesis as the proper syntax for calling a function. Add both characters at the end of `super.viewDidLoad` to remove the error.
      - The other error of the errors has a dot in the center.
        - Click this error and Xcode displays a suggestion to fix the code.
        - Click the Fix button to have Xcode implement this suggestion.
        - In this instance, Xcode provides a valid fix. However, you can’t rely on the compiler to properly fix all errors — you need to be able to address errors on your own.
  - **Bugs**

    - The third type of issue is known as a bug — and it’s the hardest issue to track down.
    - A bug is an error that occurs while running the program, resulting in a crash or incorrect output.
    - Finding bugs can involve some time and some real detective work.
    - In ViewController, add the following lines of code below `super.viewDidLoad()`:

      - ```swift
          var names = [”Tammy”, “Cole”]
          names.removeFirst()
          names.removeFirst()
          names.removeFirst()
        ```

    - You may not be familiar with Swift at this point, and that’s OK. These lines are simple to understand. names is a list containing two pieces of text, “Tammy” and “Cole.”
    - Each subsequent line removes the first item from the list. Since there are three calls to remove the first item, but only two items in the list, what do you expect will happen?
      - Build your application. Since the syntax is valid, you’ll receive the “Build Succeeded” message. Now try running the app. After a few moments, the program will crash, and the following message will appear in red on the last line of code above: `Thread 1: Fatal error: Can't remove first element from an empty collection`
      - The program crashed when it tried to remove the remaining first element and couldn't find one. You've already guessed that. But imagine you're unsure how to fix the problem. Xcode can help you to step through the program one line at a time.
    - Before you start looking for the bug, you'll need to add a breakpoint to your code.
      - A breakpoint pauses the execution of a program at a specified point. Create a breakpoint by clicking in the gutter area to the left of the line where you want execution to pause. In this case, add the breakpoint to the `var names = [”Tammy”, “Cole”]` line.
    - Build and run your app. You'll see the program pause at the breakpoint(1). That's good.
      - In the debug area(2), show the variables view to inspect the current values (the button is on the lower right(3)).
      - Because the breakpointed line hasn't yet been executed, names contains no values.
    - From here, you can use the step control buttons at the top of the debug area to slowly continue code execution:
      - Continue — Resumes code execution until the next breakpoint is reached. If you select this button now, the code will crash, since there are no other breakpoints before the third names.removeFirst().
      - Step over — Executes the selected line and pauses execution on the next line.
      - Step into — If clicked on a line with a function call, advances to the first line of the function, then pauses execution again.
      - Step out — Executes all remaining lines in the function call and pauses execution on the line after the function.
    - <img src="./resources/bugs.png" alt="Bugs" width="600" />
    - Click the "Step over" button to advance execution by one line. In the variables view, you can see that names has been assigned the proper values. So far, so good.
    - Click the “Step over” button to execute the first call to `names.removeFirst()`. names no longer includes “Tammy” in its list, so that worked fine.
    - Click “Step over” again to execute the second call to `names.removeFirst()`, leaving names an empty list with zero values. Still OK.
    - By now, it should be clear that the third call to `names.removeFirst()` is responsible for the bug.
    - Remove the third call to `names.removeFirst()` and run the program again to verify that the error has been fixed.
    - Debugging is a crucial skill for developers to build. When debugging, take the following approach:
      1. Try to understand the problem
      2. Brainstorm a potential solution
      3. Try the solution
      4. Verify it worked, repeat as necessary
    - Take each bug one step at a time. It can be frustrating to run into bugs when building apps, but it feels great when you’re able to fix them.

  - **Lab - Debug Your First App**
    - The objective of this lab is to find and resolve compiler errors, runtime errors, and compiler warnings.
    - Step 1
      - Find and Fix Compiler Errors
        - Open the Xcode project, “FirstTimeDebugging.”
        - Try to run the app. Note that it won’t run due to a few compiler errors. As you’ve learned in this lesson, compiler errors are indicated by red symbols in line with the mistake — or where the compiler guesses the mistake might be. All compiler errors are also listed in the Issue navigator.
        - Fix the compiler errors so that you can run the app. Here are two of the more common mistakes that may have caused this app’s compiler errors:
          - Missing or extra parentheses or braces (whether opening or closing).
          - Referencing a function or property but with incorrect spelling (The compiler is very literal and expects you to reference a function or property exactly by the name you gave it.)
            - ​Hint: Sometimes a single mistake can cause the compiler to flag multiple errors. Fix one mistake and you might eliminate all the error symbols.
    - Step 2
      - Find and Fix Runtime Errors
        - Were you able to remove all the red error symbols from the project? If so, try to run the app again.
        - This time, notice that the app stops execution right after opening in Simulator and that there’s a red line across one of the lines of code on the screen. The fact that the line is red indicates something went wrong. Look at the text in the console area to learn what the issue might be. Try to solve this runtime error. If it’s helpful, you might want to add breakpoints at and before the affected code, then run the app again.
    - Step 3
      - Find and Fix Compiler Warnings
      - Now that the app runs, focus your attention on a few more problems. Open the project’s Issue navigator. You’ll note several warnings, indicated by yellow triangles. Address all of these warnings.

### Lesson 1.8 Documentation

- Every developer has a preferred method of accessing documentation. Some prefer to view it in a web browser, while others like to use the documentation browser provided by Xcode. By learning multiple ways to interact with documentation, you can decide which method works best for you. The faster you can find answers to your questions, the faster you can get back to writing code.
- **Documentation Browser**
  - In the previous lesson, you added lines of code inside the viewDidLoad() function. Do you have any idea what that function does or when the function is called in your program? Xcode provides a fast answer using the Quick Help feature. Option-click the viewDidLoad() method name, and Xcode displays a popover with a brief description of the function.
  - Within the Quick Help popover, click Open in Developer Documentation to conveniently access the Xcode Developer Documentation for the function. The documentation includes a more thorough explanation of the function, the OS versions that support it, the framework it belongs to (in this case UIKit), and references to related functions.
  - In the navigation on the left, you can jump quickly to different sections of the Developer Documentation. (You can also access Developer Documentation from the Window menu or by using the shortcut, Command-Shift-0.)
  - At the top of the documentation window, you’ll see a search field, which allows you to look up documentation about any function, class, or framework. This feature makes it quick to search through thousands of pages of documentation, so answers are readily available—which is why many developers choose to leave the documentation window open while they’re coding.
  - Try navigating through the Xcode documentation. Start typing UIViewController. As you type, Xcode will suggest matching options with autocompletion. As soon as you see UIViewController in the menu, select it to display the documentation for UIViewController.
  - In the right-hand column, under On This Page, click the Topics link to jump down the page. The Topics section displays a list of symbols grouped by topic. A symbol is a function or variable associated with a particular class. In the documentation, these symbols are sorted into logical categories rather than in alphabetical order, so you can more easily locate items that interest you.
  - When you're building a new feature, these logical categories are a great way to find out if the object can do what you need.
  - Look through the topics for UIViewController and try to find the symbol for the view property. Click this symbol.
  - Here you’ll see information for your selected property. Most instance property documentation will follow a similar pattern:
    - A short description - A quick summary of what the property is
    - Declaration - The name used to access the property and the property’s associated type
    - Discussion - An in-depth description, discussing the finer (albeit, important) elements to consider when using the property
    - See Also - Other symbols that are related to the property that may be of interest
  - In the upper-left corner, you’ll see two buttons with chevrons < >. Use these to navigation backward < and forward > through your viewing history. Click the back button to return to the documentation for UIViewController. Find the symbol for the function `viewWillAppear(_:)`.
  - Most method documentation will follow a very similar pattern to instance property documentation with one possible addition:
    - Parameters — If the function has parameters (inputs), they are listed with the name used to access the parameter and a short description of the parameter
  - You’ll work more with the documentation browser as you work through this course.
- **Sample Code and Topics**
  - There's more to Developer Documentation than just descriptions of types and methods. As you work your way through coding concepts, it can be useful to read more about a certain topic or try out some sample code. The top level of documentation for the UIKit framework, for example, includes numerous overview topics and articles to help you get started. And the views and controls subtopic includes a UIKit Catalog sample code project.
  - You'll need to learn how to read and understand documentation to be a successful developer. Because documentation is very technical, it can be hard to digest when reading it the first time. It takes practice.
  - Throughout this course you will be given links to reference guides and API documentation in the “Related Resources” section. Read through them. You may not always understand every sentence or concept from reading, but you will be building a very useful skill that will help you be a successful developer.

### Lesson 1.9 Interface Builder Basics

- The best way to learn the basics of Interface Builder is to dive into Xcode and explore some of its features.
- Start by creating a new Xcode project using the iOS App template.
  - When creating the project, make sure the interface option is set to Storyboard. Name the project "IBBasics."
- **Storyboards**
  - Interface Builder opens whenever you select an XIB file (.xib) or a storyboard file (.storyboard) from the Project navigator.
  - An XIB file contains the user interface for a single visual element, such as a full-screen view, a table view cell, or a custom UI control. XIBs were used more heavily before the introduction of storyboards and you may hear seasoned macOS or iOS developers refer to XIB files as “Nib” files. They're still a useful format in certain situations, but this lesson focuses on storyboards.
  - In contrast with an XIB, a storyboard file includes many pieces of the interface, defining the layout of one or many screens as well as the progression from one screen to another. As a developer, you'll find that the ability to see multiple screens at once will help you understand the flow within your app.
  - <img src="./resources/storyboard.png" alt="Storyboard" widt="600" />
  - By default, a new iOS app project comes with one storyboard named Main.storyboard. Because Xcode doesn't show file extensions by default, it appears as Main in the Project navigator. Click it now to open the storyboard in Interface Builder. In the center of the screen, you'll see a single scene with a plain white view on an otherwise blank canvas. This scene is called the initial view controller, and it is the first screen that will appear when you open the app. As you add more scenes to the storyboard, you can drag them anywhere on the canvas. To see more view controllers at once, use two fingers on a Multi-Touch trackpad to pinch and zoom the canvas out or to zoom in on a particular view. If you don't have a trackpad, you can use the zoom buttons near the bottom of the canvas to achieve the same result.
  - Build and run the project. Simulator displays the same white screen you saw in the storyboard. How did the app know to display this screen? To investigate, select the top-most file (IBBasics) in the Project navigator, and find the Deployment Info section under the General heading. The entry in Main Interface defines which storyboard file is loaded first when the app launches.(It's disappeared on Xcode v14.) Because you created the project using the iOS App template, this entry was preconfigured to use the Main storyboard.
  - You can change the initial view controller by moving the entry point (the right-facing arrow) to the left of the desired view controller(1). Currently in this project, the Main storyboard has only one view controller, so you won't be able to change it.
    - <img src="./resources/entry_point.png" alt="Entry Point" widt="400" />
- **Interface Builder Layout**
  - To the left of the main canvas is the Document Outline view. To reveal it, click the Show Document Outline button in the bottom left corner of the canvas(1). The Document Outline displays a list of each view controller in the scene, along with a hierarchical list of the elements within each view controller. Click the gray triangles to the left of each item to inspect the contents. As you might notice, clicking the view in the outline will highlight the corresponding element on the canvas(2).
    - <img src="./resources/document_outline.png" alt="Document Outline" widt="200" />
  - Select the Library button + in the Xcode toolbar to display the Object library. The Object library contains buttons, text fields, labels, and other view controllers that you can add to your scene.
  - Scroll through the Object library to find and select “Button,” then drag the item from the library onto the view. As you drag the button toward the upper-left corner of the view, try to use the layout guides.
    - Layout guides appear as a dotted blue line when you are placing or resizing a view object in Interface Builder.
    - Layout guides help you center your content, use appropriate margins and spacing between objects, and avoid putting content in the status bar at the top of the screen.
  - Go ahead and release the mouse or trackpad to insert the button into the view. Notice that the button object now shows up in the Document Outline as well.
  - On the right side of the screen, you see the Inspector area. If you don’t see it, click the "Hide or Show the Inspectors" button at the top left of the toolbar or use the keyboard shortcut, Option-Command-0.
  - In addition to the File, History, and Quick Help inspectors (which are always available), the top of the Inspector area displays four context-sensitive inspectors when you're in Interface Builder. To explore these different inspectors and how they can help you customize the objects in your view, select the button you just added—either in the Document Outline or in the scene itself.
