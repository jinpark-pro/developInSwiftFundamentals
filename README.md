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
  - An XIB file contains the user interface for <u>a single visual element</u>, such as a full-screen view, a table view cell, or a custom UI control. XIBs were used more heavily before the introduction of storyboards and you may hear seasoned macOS or iOS developers refer to XIB files as “Nib” files. They're still a useful format in certain situations, but this lesson focuses on storyboards.
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
- **Outlets And Actions**
  - You'll often need a way to reference your visual elements in code so that they can be adjusted at runtime, or when the app is already running. This reference from Interface Builder to code is called an outlet. When you have an object that you want the user to interact with, you create an action—a reference to a piece of code that will execute when the interaction takes place.
  - Select the view controller in the outline view, then select the Identity inspector. The template you chose when creating the project has set the Custom Class to ViewController. Open the assistant editor by clicking the Adjust Editor Options button and choosing Assistant Editor.
  - The source code of ViewController is displayed alongside the storyboard (because it corresponds to the Custom Class field in the Identity inspector).
  - But the ViewController class still doesn’t have access to the button you added. To make the object accessible in code, you’ll need to create an outlet.
  - Creating an Outlet
    - Control-click (or right-click) the button in the storyboard, and start dragging toward the assistant editor pane that contains the ViewController class definition. As you drag the pointer into the code, you see a blue line.
    - When you release the pointer, the "Outlets and Actions" dialog appears. Make sure that Connection is set to Outlet and Storage is set to Strong. In the Name field, specify a variable name for the button: "myButton." Click the Connect button to finalize the creation of the outlet, generating a line of code that defines the outlet.
    - Now that you have access to the button in code, add the following line inside the viewDidLoad() function: `myButton.tintColor = .red`
    - This line changes the color of the button’s title from blue to red. Build and run your application to see the change take effect.
    - That’s great, but you’ll probably notice that nothing happens when you try clicking the button. To add functionality, you’ll need to create an action that’s tied to the button.
  - Creating an Action
    - Once again, Control-click (or right-click) the button in the storyboard, and drag the cursor into the ViewController class definition.
    - When the “Outlets and Actions” dialog appears, set Connection to Action. In this situation, your entry in the Name field doesn’t define a variable; it defines the action the button tap is tied to. Name the action “buttonPressed.” Click the Connect button to finalize the creation of the action.
    - You now have a function to execute whenever the button is tapped. To test it, add the following line inside the buttonPressed function: `print(”The button was pressed”)`
    - This code prints a message to the Xcode console whenever the function is executed. Build and run your app, then click the button to see the message print in the console at the bottom right of the screen.
    - Back in the outline view, select the button again, then select the Connections inspector. Now that you’ve wired up an outlet and an action to the button, you’ll see them both in the Connections pane.
- **A Note About Interface Builder**

  - Every attribute in Interface Builder represents a property that can also be configured programmatically, or in code. Interface Builder is simply a graphical interface for configuring and setting properties on UIKit classes that are displayed in your app.
  - Add a label to your scene, then look at the Attributes inspector for the label.
  - Now look up the symbols, or properties and functions, for UILabel in the Documentation Browser. You’ll find that each setting in Interface Builder has a companion property.
  - | Interface Builder Attribute | Property Name                        |
    | --------------------------- | ------------------------------------ |
    | Text                        | text                                 |
    | Color                       | textColor                            |
    | Dynamic Type                | adjustsFontForContentSizeCategory    |
    | Font                        | font                                 |
    | Alignment                   | textAlignment                        |
    | Lines                       | numberOfLines                        |
    | Enabled                     | enabled                              |
    | Highlighted                 | isHighlighted                        |
    | Baseline                    | baselineAdjustment                   |
    | Line Break                  | lineBreakMode                        |
    | Autoshrink                  | adjustsFontSizeToFitWidth            |
    | Tighten Letter Spacing      | allowsDefaultTighteningForTruncation |
    | Highlighted                 | highlightedTextColor                 |
    | Shadow                      | shadowColor                          |
    | Shadow Offset               | shadowOffset                         |
  - Many objects that you can configure in Interface Builder have properties that can only be set programmatically. For example, `UIScrollView` has a `contentSize` property that does not have a matching option in the Attributes inspector.
  - When you need to adjust one of these settings, you can do so programmatically by setting up an @IBOutlet for the scroll view and updating the properties using dot-notation. `scrollView.contentSize = CGSize(width: 100, height: 100)`
  - In fact, everything that you can do in Interface Builder can also be done programmatically, including setting up all child views and adding them to the screen.

    - ```swift
        let label = UILabel(frame: CGRect(x: 16, y: 16, width: 200, height: 44))
        view.addSubview(label) // Adds label as a child view to `view`
      ```

  - This type of setup is most commonly done in the viewDidLoad() method of a view controller, which gives you access to the view controller’s main view property before it’s displayed on the screen.
  - While you can do everything programmatically, you can see that Interface Builder can save you a lot of time when setting up complex views. As your projects grow, storyboards help you more easily maintain your interface setup. Additionally, Interface Builder has support for building complex views that support multiple device sizes, all in one place.
  - You will learn much more about Interface Builder and storyboards as you work through the rest of the course.

### Guided Project: Light

- You'll have created an app, called Light, that changes the screen from black to white, and back again, whenever the user taps a button.
- To successfully build the light, you'll need to use Xcode documentation, set breakpoints, and create outlets and actions.

#### 1. Create A Button and An Action

- Create a new Xcode project using the iOS App template, set the interface option to Storyboard, and name the project "Light."
- Select the Main storyboard in the Project navigator to open your storyboard in Interface Builder.
- Select View Controller in the Document Outline, then click the Identity inspector button at the top of the Inspector area to confirm that this particular view controller is of type ViewController.
- If you're using Simulator, use the Devices button at the bottom of the canvas (the current selection is shown next to the button) to adjust the size of the canvas. Set the canvas size to the iPhone 13 Pro configuration, and select the iPhone 12 Pro or iPhone 13 Pro simulator from the menu toward the left end of the Xcode toolbar.
- If you’re using your own device for this project, the size of the view controller may not be identical to the size of your screen. Use the “View as” button at the bottom of the canvas to adjust the size of the canvas to match your device, but leave it in portrait orientation.
- Select the view controller’s view, then select the Attributes inspector, which will allow you to customize the attributes of any interface element. The background color for this view has already been set to white. That’s the desired state of your app on launch, so you don’t need to change anything right now.
- Next, add a button that’ll be used to change the view's background color, simulating a light turning on and off. Press the + button at the top right of the toolbar to open the Library. As you learned in an earlier lesson, this library includes a list of common objects you can add to a storyboard. Scroll through the list, or use the search filter at the top of the library area.
- Find the “Button” object in the library and drag it over on top of the view. When you release the cursor, the Document Outline should indicate that the button has been added as a subview.
- Move the button to the upper-left corner of the view. Margin-alignment guides will help snap the object into the correct position.
- Give your button an action to perform when it's clicked or tapped. Add an assistant editor using the Adjust Editor Options button and choose Assistant Editor to split the Xcode workspace into two parts: Interface Builder and its corresponding code.
- Now Control-drag (or right-click) the button into an available area within the ViewController class definition. As you drag, a blue line extends from the button and a blue horizontal bar will display below your cursor, indicating a valid place to create a connection.
- When you release the mouse cursor, you will be prompted to create an outlet or define an action. Change Connection to Action, then set Name to “buttonPressed.” When you click the Connect button, Xcode will create a new method that will be called whenever the button is tapped. You may notice the @IBAction keyword right before the buttonPressed(\_:) method. @IBAction signals to Xcode that a relationship can be created between a visual element in a storyboard and the function.
- Build and run the app. When you press the button, nothing happens, because there’s no code within the buttonPressed(\_:) method to execute. To verify that the method is being called, you can place a breakpoint within the method definition. Now press the button and the breakpoint will be triggered.
- Now that you’ve verified that the action is working correctly, you can add some code to change the background color. Remove the breakpoint before proceeding.

#### 2. Change The Background

- If the light is on (that is, if the background color is white) then the light should be switched off. Otherwise, if the light is off (the background is black), then the light should be switched on. The statement "the light is on" is either a true or false statement, so it would make sense to use a Boolean to determine how to change the background color.
- Near the top of the ViewController class definition, create a variable called lightOn and set the initial value to true, since the screen starts off with a white background. `var lightOn = true`
- Each time the button is tapped, the value should change from true to false, or from false to true. Swift booleans have a method, toggle(), that does precisely this. Since the buttonPressed(\_:) method is called whenever the tap is executed, make the change there.

  - ```swift
      @IBAction func buttonPressed(_ sender: Any) {
          lightOn.toggle()
      }
    ```

- After the value has been changed, you can use the new value to determine how to change the background color. If the light is supposed to be off, change it to black. Or if it’s supposed to be on, change it to white. You can write this logic using a simple if-statement.

  - ```swift
      @IBAction func buttonPressed(_ sender: Any) {
          lightOn.toggle()
          if lightOn {
            view.backgroundColor = .white
          } else {
            view.backgroundColor = .black
          }
      }
    ```

- Build and run your application, and the background should successfully change on each press.
- As your application’s size continues to grow, make sure that your code stays organized. Rather than put the if-statement directly inside the buttonPressed(\_:) method, you can move it to a new method that handles updating the entire user interface.
- Select the entire if-statement, and then choose Editor > Refactor >​ Extract to Method.
- Xcode moves the code out of place into a new method and enters a special editing mode that allows you to set the new method's name and update where it’s called at the same time. Type updateUI and press the Return key to set the name.
- Xcode moved the selected code into a new method named updateUI(), and then added a call to updateUI() where the code once lived.
- The result should look like the following:

  - ```swift
      fileprivate func updateUI() {
        if lightOn {
          view.backgroundColor = .white
        } else {
          view.backgroundColor = .black
        }
      }
       
      @IBAction func buttonPressed(_ sender: Any) {
          lightOn.toggle()
          updateUI()
      }
    ```

- Notice the `fileprivate` keyword that Xcode used in front of the method name. Swift uses this special access modifier to specify where the method can be called from. If you use the Xcode refactor feature and need to call your method outside of the file it’s defined in, remove the fileprivate keyword in front of it.
- This is a small change for a small app. You will see this pattern persist throughout this book, and you will find it much easier to debug interface issues if the code that updates the view is all contained in a single method.

#### 3. Update The Button Text

- You’ve now successfully set the button to change the background color of the view, but the title of the button text remains the same no matter the state of the light. At the moment, there’s no way to reference your newly created button in code. You must first create an outlet to the button. Control-drag the button in Interface Builder to an empty space at the top of the view controller’s definition in the editor area. In the popover, verify that Outlet is selected under Connection, and enter “lightButton” in the Name field.
- As you learned in an earlier lesson, you’re able to see these details of the outlet, from left to right:
  - Circle — The filled circle indicates that the outlet is connected. The circle would be empty if the property isn’t connected to anything.
  - @IBOutlet — This keyword signals to Xcode that the property on this line is an outlet.
  - var lightButton — This declares a property called “lightButton.”
  - UIButton! — The type of the property is UIButton!. The exclamation point warns you that the program will crash if you try to access this property and the outlet isn’t connected. You’ll learn more about the exclamation point when you learn about optionals in a later unit.
- Having created the outlet, you can now make changes to the button programmatically. Start by finding the right place for updating the button’s title and the right action for it to perform.
- <img src="./resources/breakpoint.png" alt="Breakpoint" width="400" />
- Add a breakpoint to the first line of the `buttonPressed(_:)` method, then build and run your app. As you might expect, when you press the button to change the color, the corresponding action, `buttonPressed(_:)`, will be executed. But since you added a breakpoint, the code will pause before executing the line with the breakpoint.(1)
- Click the “Step over” button (2) to run the first line. Now your app is paused just before running the updateUI() method. Click the “Step into” button (3). Now the app is paused just before executing the first line of updateUI.
- Take a moment to try and read the body of the updateUI() method. Since Swift is a very readable programming language, you can probably interpret the lines to say: “If the light is on, the view’s background color should be white, or else the view’s background color should be black.”
- Now consider how the button’s title should be decided. If the light is on, the button’s title should read “Off,” or else the button’s title should read “On.” It makes sense that the button’s title should be updated in a similar way to the view’s background color.
- You’ve now found a reasonable place to update the text—in the updateUI() method. But what’s the actual function for doing so? As you learned earlier, Xcode documentation is always available to support you. So whenever you’re unsure of something, it’s a good habit to look to the documentation for answers.
- To learn how to set the title of lightButton, start by reading the documentation on its type, UIButton. You can access the documentation directly using Window > Developer Documentation from the Xcode menu. This opens a separate window with the documentation viewer.
- Start entering UIButton in the documentation search field. Autocompletion quickly suggests options. As soon as you see UIButton in the menu, go ahead and select it.
- Scroll down to the Symbols section to find a list called “Configuring the Button.” ​There you’ll find a function to set the title: `func setTitle(String?, for: UIControl.State)`.
- Click the function name to see its declaration and a list of its parameters. The first parameter is the desired text, and the second parameter is a UIControl.State. UIControl.State represents the different potential states of a button, for example: if it is sitting idle, if the user has begun tapping it, or if the button is disabled. Click UIControl.State in the Declaration section.
- In this new list of symbols, the Constants section contains a normal constant, which corresponds to the state of the button when it’s enabled and sitting idle on the screen. This is the correct state for setting the button’s title.
- With your new knowledge of the updateUI() method, you can remove the breakpoints you added earlier and adjust the method to look like the following:

  - ```swift
      func updateUI() {
        if lightOn {
          view.backgroundColor = .white
          lightButton.setTitle(”Off”, for: .normal)
        } else {
          view.backgroundColor = .black
          lightButton.setTitle(”On”, for: .normal)
        }
      }
    ```

- Build and run your app. Clicking or tapping the button should now change both the background color and the button text. But there’s a bug: Before the button is clicked, the text still reads “Button,” not “On” or “Off.” How can you update the code to resolve this issue?
- Your project already has code that will make sure the button’s text matches the on or off state of the light: updateUI(). You just need to call it when the view first loads — so that the button is updated when the view appears, instead of when the user first taps the button. You can run setup code in the viewDidLoad() function, which is already defined in your view controller subclass and is called when the view controller is ready to appear on the screen.
- Call updateUI() within this method, as shown in the following example:

  - ```swift
      override func viewDidLoad() {
          super.viewDidLoad()
          updateUI()
      }
    ```

- Build and run your app again. On launch, the text of the button should now read "Off."

#### 4. Improve The User Experience

- Now take a moment to think about its design and how the user experiences the app. What could be improved?
- Looking at the button, you might realize that the text feels extraneous. It’s pretty clear whether the light is currently on or off — the background color indicates that. Does the user need to see the text at all?
- Does it matter where on the screen the button is located? And isn’t it a little odd that most of the screen isn’t tappable?
- It may be better to remove the text from the button and to make the button fill the entire screen. That way, the user can tap anywhere on the screen to turn the light on and off. An important part of building any app is considering the little details and trying to build an intuitive, simple, powerful user interface. In this case, it makes sense for the user to be able to tap anywhere on the screen to toggle the background color.
- To begin, you’ll need to resize the button to fill the screen. Select the button in Interface Builder, then drag its top-left and bottom-right corners, extending the button to cover the entire white view.
- Remove the title text for the button. The tappable area of the button will still perform as expected, but it will now appear as though only the white view exists on the canvas.
- With the text gone, you can remove the lines of code in updateUI() that make changes to the button’s title.
- In this updated design, the button’s properties don’t need to change while someone is using the app. That means the outlet — which you created at the beginning of the project — is no longer needed. As a developer, you want to keep your code as clean as possible, so it’s a good idea to clear out the @IBOutlet.
- First, sever the connection between the button and its outlet. To do so, select the button in Interface Builder, then show the Connections inspector. Here you can see all the events and outlets connected to a particular object. In this case, you can see that the button is tied to the buttonPressed: action and to the lightButton outlet. ​Click the X next to the outlet to remove it.
- Since there are no longer any objects connected to lightButton, the little circle next to @IBOutlet is no longer filled in. It’s now safe to delete the declaration of lightButton.
- Build and run your app one last time to test your new design improvements. You should now be able to tap or click anywhere on the screen to change its background color.
- Because both lines in the if-else statement do the same thing (set the backgroundColor), the updateUI() method might look cleaner if you use a ternary operator instead of an if-else statement.

  - ```swift
      func updateUI() {
        view.backgroundColor = lightOn ? .white : .black
      }
    ```

- Build and run your application once more to verify that the ternary operator works as intended.

- **Wrap-Up**
  - You've successfully created an app that changes the screen from black to white, and back, at the tap of a button—something like a flashlight. You've simplified the design of the app as well, making conscious decisions to improve the user experience by removing the button title and filling the screen with a tappable area. Even though you have limited knowledge of Swift, you were able to step through lines of code and refer to the documentation to complete this project.

## Unit 2 Introduction To UIKit

- You'll learn about structures, collections, loops, and different ways to work with the information that makes up an app. You'll also build a Keynote prototype of your own app idea and think about how the skills you're learning can be used to eventually build a functioning app. At the end of the unit, you'll build an ambitious project.
- What You'll Design
  - The App Design Workbook will guide you through designing a working prototype of your app in Keynote.
- What You’ll Build
  - Apple Pie is a simple word-guessing game where the user must guess a word, letter by letter, before all the apples fall off the apple tree. If there are apples remaining, the user wins—and can eat delicious Apple Pie.

### Lesson 2.1 Start Your App Prototype

- Before diving into coding, most app developers save time and energy by first creating a working prototype to iterate on their ideas and get feedback before finalizing the structure of their app. Developers build prototypes in all sorts of ways, from simple notebook sketches to partially completed apps in Xcode.
- In this unit, you’ll build a prototype in Keynote—a happy medium. It’ll be easier to create than using Xcode, but have more fidelity to the look and feel of an app than paper. In this lesson, you’ll start by mapping screens to form an app architecture.
- Prototyping
  - A prototype is a fake version of your app that you can show other people to get feedback. It should give users a sense of how your app works, even though it may not do much. If you start from your app's goals and features, creating a prototype can be fun, and it can delight your users even if you don't write a single line of code.
- Map
  - In the last unit, you outlined a concrete plan for what features and functionality your app should have, including choosing an MVP feature that can help a user solve the primary problem. Starting with this feature set, you are ready to create a prototype to show potential users. The first step in this process is to turn your list of features into workflows showing how a user will navigate within the app. This is where your app starts to take shape.
  - Complete the Map section of the App Design Workbook. In these activities, you’ll create an outline of the information and functions on each screen — and how they relate to each other. You’ll derive your app’s architecture from the its key functions, making decisions based on how you expect users to work with it. By the end of this section you’ll have a Keynote file with linked screen outlines, which is the beginning of your prototype.

### Lesson 2.2 Strings

- Swift’s strings are represented by the String type, and the most common way to define one is by using a string literal.
- A string literal is a raw representation of a String value. You write a string literal by surrounding a set of characters with double quotation marks “.
- String literals are commonly used to set an initial value for a constant or variable: `let greeting = “Hello”`, `var otherGreeting = “Salutations”`
  - If you assign a string to a constant (using let), the string is immutable and can't be modified.
  - If the string is assigned to a variable (using var), the string is mutable and can change.
- If your string literal needs to be multiple lines, simply surround your set of characters with three double quotation marks “””. In its multiline form, the string literal includes all of the lines between its opening and closing quotes. The string begins on the first line after the opening quotes and ends on the line before the closing quotes.

  - ```swift
      let joke = “””
        Q: Why did the chicken cross the road?
        A: To get to the other side!
        “””
      print(joke)
      Console Output:
      Q: Why did the chicken cross the road?
      A: To get to the other side!
    ```

- Any space preceding each line in your multiline string literal will be ignored if it aligns with the closing """ quotation marks. Multiline string literals may contain double quotes (").

  - ```swift
      let greeting = """
        It is traditional in programming to print "Hello, world!"
        """
    ```

- To include double quotes in single-line string literals, you'll need to use the backslash (\), known in Swift as the escape character. That's because you're “escaping” the normal interpretation of characters in the string, `let greeting = “It is traditional in programming to print \”Hello, world!\””`
- You can use the escape character with other letters and symbols to produce specific results:
  - Double quote: \”
  - Single quote: \’
  - Backslash: \\
  - Tab: \t
  - Newline (go to the next line—like pressing Return): \n
- You’ll often find that you want to start with an empty string, then add to it over time. This means you’ll need to make it a variable. Use the following syntax to initialize the string without any text: `var myString = “”`
- If you need to check if a Swift String is empty, you can use the Boolean property, `isEmpty`:

  - ```swift
      var myString = “”
       
      if myString.isEmpty {
        print(”The string is empty”)
      }
    ```

- As you might expect, individual characters are of type Character. But since strings are much more common in programming than individual characters, Swift will always infer the type of a collection of characters — or even a single character — as String, unless you specify otherwise with a type annotation:

  - ```swift
      let a = “a” //’a’ is a String
      let b: Character = “b” //’b’ is a Character
    ```

#### Concatenation And Interpolation

- Sometimes you need to combine strings. The + operator isn’t just for numbers; it can add strings together too. You can use + to create a new String value from multiple String values. This is called concatenation.
- If the existing String is a variable, you can use the += operator to add to it or modify it.

  - ```swift
      let string1 = “Hello”
      let string2 = “, world!”
      let myString = string1 + string2 // “Hello, world!”

      var myString = “Hello”
      myString = myString + “, world!” // “Hello, world!”
      myString += “ Hello!” // “Hello, world! Hello!”
    ```

- As strings grow in complexity, the use of the + operator can make your code tricky to handle. In the code above, for example, you might forget to add a space before “Hello!”
- Swift provides a syntax, known as string interpolation, that makes the inclusion of constants, variables, literals, and expressions easier. String interpolation allows you to easily combine many values into a single String constant or variable.
- You can insert the raw value of a constant or variable into a String by preceding the name with a backslash \ and wrapping the name in parentheses (). In the example below, the printed String will contain the raw values of the name and age constants.
- You can place entire expressions within the parentheses. These expressions will always be evaluated first, before being printed or stored.

  - ```swift
      let name = “Rick”
      let age = 30
      print(”\(name) is \(age) years old”) // Rick is 30 years old

      let a = 4
      let b = 5
      print(”If a is \(a) and b is \(b), then a + b equals \(a+b)”)
      Console Output:
      If a is 4 and b is 5, then a + b equals 9
    ```

- Using string interpolation, the raw values of the a and b constants are inserted into the printed String value.
- It was hinted at above, but since the result of string interpolation is a String, you can also use it anywhere you'd use a String or string literal:

  - ```swift
      let listName = "Shopping"
      var items = 14
      myLabel.text = "There are \(items) items on your \(listName) list"
      // The label displays "There are 14 items on your Shopping list"
       
      func setLabel(_ label: UILabel, to text: String) {
        label.text = text
      }
       
      setLabel(myLabel, to: "There are \(items) items on your \(listName) list")
      // The label displays "There are 14 items on your Shopping list"
    ```

#### String Equality And Comparison

- Developers often need to compare String values to see if they’re equal to each other.
- Just as you do with numbers, you can check for equality between two strings using the == operator. As you might expect, == checks for identical characters in the same order. Since uppercase characters aren’t identical to their lowercase counterparts, the strings have the same value if the case of each character also matches. This is known as case sensitivity.
- But maybe you want to ignore the capitalization of a string when checking for string equality. You can use the `lowercased()` method to normalize the two, comparing an all-lowercase version of the string with an all-lowercase version of the calling string.
- You could have also used lowercased()'s counterpart, `uppercased()`, which creates an all-uppercase version of the string.
- If you want to match the beginning or the end of the string, you can use the `hasPrefix(_:)` or `the hasSuffix(_:)` method. Just like ==, these matches are case-sensitive.

  - ```swift
      let name = “Johnny Appleseed”
      if name.lowercased() == “joHnnY aPPleseeD”.lowercased() {
        print(”The two names are equal.”)
      }
      Console Output:
      The two names are equal.

      let greeting = “Hello, world!”
      print(greeting.hasPrefix(”Hello”))
      print(greeting.hasSuffix(”world!”))
      print(greeting.hasSuffix(”World!”))
      Console Output:
      true
      true
      false
    ```

- Maybe you want to check if one string is somewhere within another string. You can use the `contains(_:)` method to return a Boolean value that indicates whether or not the substring was found.

  - ```swift
      let greeting = “Hi Rick, my name is Amy.”
      if greeting.contains(”my name is”) {
        print(”Making an introduction”)
      }
    ```

- Since a string is a collection of characters, its length is equal to the total number of characters. The size of any collection can be determined using its `count` property. You can use this property to compare strings or to evaluate whether strings meet a certain requirement.

  - ```swift
      let name = “Ryan Mears”
      let count = name.count // 10
       
      let newPassword = “1234”
       
      if newPassword.count < 8 {
          print(”This password is too short. Passwords should have at
          least eight characters.”)
      }
      Console Output:
      This password is too short. Passwords should have at least
      eight characters.
    ```

- In the last unit, you learned that you can use switch statements to perform specific blocks of code based on a particular case. You can also use the switch statement to pattern-match multiple values of strings or characters and to respond accordingly.

  - ```swift
      let someCharacter: Character = “e”
      switch someCharacter {
        case “a”, “e”, “i”, “o”, “u”:
          print(”\(someCharacter) is a vowel.”)
        default:
          print(”\(someCharacter) is not a vowel.”)
      }
      Console Output:
      e is a vowel.
    ```

#### More Advanced String Topics

- Similar to the lowercased(), hasPrefix(_:), hasSuffix(_:), and contains(\_:) methods mentioned previously, strings come with a variety of properties and methods that can be useful for tracking locations of characters within strings, creating new strings from “substrings,” inserting characters or strings into existing strings, and much more. Much of this functionality is shared among all Swift collections. For now you don’t need to worry about these more advanced string topics, but keep in mind that you can always turn to documentation to learn more should you wish to do more advanced string manipulation with Swift. For reference, here are a few useful String properties and methods that you could look up:

  - startIndex
  - endIndex
  - index(before:)
  - index(after:)
  - index(\_:offsetBy:)
  - insert(\_:at:)
  - insert(contentsOf:at:)
  - remove(at:)
  - removeSubrange(\_:)
  - replaceSubrange(\_:with:)

- For a full list of methods and more information you can review the [String documentation](https://developer.apple.com/documentation/swift/string).

#### Unicode

- Every Swift String adheres to an international computing standard called Unicode. Unicode compliance allows Swift to go beyond the short list of letters and symbols in the English language. Instead, Unicode encompasses over 128,000 different characters used across multiple languages. This includes accents on characters (é), emoji (🐮), symbols (∞), Kanji (七), and other specialized characters. In addition, Unicode supports text that reads right to left, as well as left to right.
  Swift ensures that you can work with Unicode characters conveniently, so that “e,” “é,” and “🐮” are treated as single characters with a length of 1.
- In reality, a character is a Unicode “extended grapheme cluster” which is a fancy way of saying that some characters are actually comprised of multiple (often invisible) characters although they appear to the user as a single character. For example, “ü” comprises two characters and “👩🏽‍🎓” comprises four characters! Swift makes working with these much easier.

### Lesson 2.3 Functions

- When someone gives you the task “get dressed,” it seems like such a simple instruction. But the details of what you'll wear, how you'll put the clothes on, and where you'll get the clothes from are all wrapped up within the “get dressed” phrase. The idea of taking something that is complex and defining a simpler way to refer to it is an abstraction, and a function is one of the fundamental ways to create an abstraction in code.
- A function is made up of a name, a set of inputs, and a set of outputs. Both inputs and outputs are optional. You call or invoke a function to cause your program to do something such as print text to the console.
- In Swift, a function can take zero, one, or many parameters, and likewise return zero, one, or many values. When a function does return values, you can choose to ignore them.
- Similar to the declaration of a constant with let or a variable with var, the func keyword tells the Swift compiler that you're declaring a function. Immediately following func, you add the name of the function followed by parentheses (), which may or may not include a list of parameters within them. If the function has a return value, you'll write an arrow (->), followed by the type of data the function will return, such as Int, String, Person, and so on.
- **Defining A Function**

  - `func functionName (parameters) -> ReturnType { // body of the function }`
  - Here’s an example of a function that will display the first ten digits of pi (π). Since printing pi requires no additional input, there are no parameters. And since printing pi doesn’t need to return anything relevant to the function caller, no return value is specified.
  - Once a function has been properly declared, you can call it, or execute it, from anywhere just by writing its name.

    - ```swift
        func displayPi() {
            print(”3.1415926535”)
        }

        displayPi()
        Console Output:
        3.1415926535
      ```

- **Parameters**

  - To specify a function with a parameter, insert a name for the value, a colon (:), and the value’s type—all inside the parentheses. For example, say you wanted to write a function called triple that takes in an Int, triples the value, and then prints it.
  - The parameter value is a constant you can use within the function. When you call a function, you pass values for its parameters as arguments. In the code below, the argument for value in the call to the function triple(value:) is 10.

    - ```swift
        func triple(value: Int) {
          let result = value * 3
          print(”If you multiply \(value) by 3, you’ll get \(result).”)
        }

        triple(value: 10)
        Console Output:
        If you multiply 10 by 3, you’ll get 30.
      ```

  - To give a function multiple parameters, separate each parameter with a comma (,). Here’s an example of a function that takes in two Int parameters, multiplies them together, and then prints the result. The function is then called with one argument per parameter

    - ```swift
        func multiply(firstNumber: Int, secondNumber: Int) {
          let result = firstNumber * secondNumber
          print(”The result is \(result).”)
        }
         
        multiply(firstNumber: 10, secondNumber: 5)
        Console Output:
        The result is 50.
      ```

- **Argument Labels**

  - So far, the labels for the arguments passed to a function are the same as the names for the parameters it uses internally. In the next example, firstName is used both within the function and when the function is called:

    - ```swift
        func sayHello(firstName: String) {
          print(”Hello, \(firstName)!”)
        }
         
        sayHello(firstName: “Aidyn”)
      ```

  - But imagine that you want your function to read a little more cleanly: `sayHello(to: “Miles”, and: “Riley”)`
  - The argument labels to and and make the function read very clearly: "Say hello to Miles and Riley." However, check out the implementation of this function:

    - ```swift
        func sayHello(to: String, and: String) {
          print(”Hello \(to) and \(and)”)
        }
      ```

  - Within the body of the function, to and and are poor names for parameters. To make the name of the parameter within the function different from the label used to call the function, specify a separate argument label before the parameter name. In the code below, to is the argument label for the parameter person, while and is the argument label for the parameter anotherPerson:

    - ```swift
        func sayHello(to person: String, and anotherPerson: String) {
          print(”Hello \(person) and \(anotherPerson)”)
        }
         
        sayHello(to: “Miles”, and: “Riley”)
      ```

  - If the function is clearer without an argument label, you can go ahead and omit it. For example, take the print function: `print(”Hello, world!”)`
  - The name of the function already makes it very clear what should be passed in as a parameter. It would feel extraneous if you had to call the function in the following way: `print(message: “Hello, world!”)`
  - To omit the argument label, use `_`. In the next example, the label for the firstNumber parameter is omitted, while the to label adds meaning and makes the function call more readable:

    - ```swift
        func add(_ firstNumber: Int, to secondNumber: Int) -> Int {
            return firstNumber + secondNumber
        }

        let total = add(14, to: 6)
      ```

- **Default Parameter Values**

  - Parameters allow a function to remain flexible, but often there’s a value you want to use most of the time. For example, you might drink water with nearly all of your meals, but every now and then you have a glass of orange juice instead.
  - As part of the function definition, you can provide a default value for any parameter. This way, you can call the function with or without the parameter. If the parameter is unspecified, the function simply uses the default value.

    - ```swift
        func display(teamName: String, score: Int = 0) {
          print(”\(teamName): \(score)”)
        }
         
        display(teamName: “Wombats”, score: 100) // ”Wombats: 100”
        display(teamName: “Wombats”) // ”Wombats: 0”
      ```

  - A certain level of thought needs to go into defining a function with default parameter values and argument labels. The compiler can do only so much when inferring what you're calling. If you mix default values and parameters without argument labels, you need to validate that every variation of the function call can be inferred.

    - For example, the compiler can't infer which variant of your function to call when defined like the following:

      - ```swift
          func displayTeam(_ teamName: String, _ teamCaptain: String = "TBA", _ hometown: String, score: Int = 0) {
            // ...
          }
           
          displayTeam("Dodgers", "LA") // ERROR: Missing argument for parameter #3 in call
        ```

    - You may find it obvious that you want the function to use the default value of “TBA” for teamCaptain and assign “Dodgers” to teamName and “LA” to hometown. But the compiler recognizes only three String parameters without argument labels, and only two values to assign. It can't assume that you intended to use the default value for teamCaptain.
    - It's best to leave arguments with default values at the end of the function signature and always provide an argument label. In the above example, the compiler would be satisfied if teamCaptain had an argument label: `func displayTeam(_ teamName: String, _ hometown: String, teamCaptain: String = "TBA", score: Int = 0)`

- **Return Values**

  - It’s unlikely that you’ll always want to print “The result is” before the result from multiply. Instead, it might make more sense if the function simply returned the new value. To do so, you’ll need to adjust the function declaration to have a return value and to specify the value’s type. You’ve learned that multiplying two Int types will always result in an Int, so that’s the return type you’ll use.
  - Within the function’s body, you’ll use the return keyword to specify what the return function will return.

    - ```swift
        func multiply(firstNumber: Int, secondNumber: Int) -> Int {
          let result = firstNumber * secondNumber
          return result
        }
      ```

  - Rather than multiplying the values, storing the new value in result, and immediately returning it, the function could also be written without the constant.
  - Starting with Swift 5.1, you can even omit the return keyword for functions that have a single line implementation. Because multiply(firstNumber:secondNumber:) has a return type and only one line of code in its body, the result of that expression is used as its return value.
  - To call this function and use the return value, you can assign the return value to a constant.
  - If you don’t need to use constant value ever again in the future, you could use the function inside the print statement and skip assigning the value to a constant

    - ```swift
        func multiply(firstNumber: Int, secondNumber: Int) -> Int {
          firstNumber * secondNumber
        }

        let myResult = multiply(firstNumber: 10, secondNumber: 5)
        //myResult = 50
        print(”10 * 5 is \(myResult)”)

        print(”10 * 5 is \(multiply(firstNumber: 10, secondNumber: 5))”)
      ```

### Lesson 2.4 Structures

- Swift comes with predefined structures for representing common types of data. You can define your own structures when you want a type that fits the specific needs of your program or app.
- In its simplest form, a structure is a named group of one or more properties that make up a type. Properties represent the information about an instance of the structure.
- You define a structure using the struct keyword along with a unique name. You can then define properties as part of the struct by listing the constant or variable declarations with the appropriate type annotation. The convention is to capitalize the names of types and to use camel case for the names of properties.
- Consider the simple declaration of a Person structure with a name property:

  - ```swift
      struct Person {
        var name: String
      }
    ```

- The above declaration simply defines the properties of a Person type. It doesn’t have a value in itself. For that, you have to create an instance of the Person type. Then you can access the data stored in its properties, such as the person’s name, using dot syntax.

  - ```swift
      let firstPerson = Person(name: “Jasmine”)
      print(firstPerson.name)
      Console Output:
      Jasmine
    ```

- As the name in the example implies, more than one Person might get created throughout the lifetime of your program. The next instance you create could be called secondPerson, or you could create a collection called people that holds multiple Person objects. You’ll learn about collections in an upcoming lesson.
- You can add functionality to a structure by adding a method. A method is a function that’s assigned to a specific type. In this example, our Person instances can now sayHello.

  - ```swift
      struct Person {
        var name: String
        func sayHello() {
          print(”Hello, there! My name is \(name)!”)
        }
      }
    ```

- You can now call the instance method directly using dot syntax.

  - ```swift
      let person = Person(name: “Jasmine”)
      person.sayHello()
      Console Output:
      Hello, there! My name is Jasmine!
    ```

- **Instances**

  - You’ve just learned that a structure defines a new type. To use that type, you must create an instance of it, a process called initialization. After initialization, each instance inherits all the properties and features of the structure.
  - In the following example, both myShirt and yourShirt are Shirt objects with size and color properties. But each one is a separate shirt with distinct values for each property, and therefore a separate instance of the Shirt type. The Size and Color types define a group of available options, called an enumeration, which you’ll learn about in a future lesson. For now, since you haven’t defined Size and Color, this example won’t compile if you copy it into a playground. Instead, just look at the code and try to understand conceptually what is happening.

    - ```swift
        struct Shirt {
          var size: Size
          var color: Color
        }
        // Defines the attributes of a shirt.
         
        let myShirt = Shirt(size: .xl, color: .blue)
        // Creates an instance of an individual shirt.
        let yourShirt = Shirt(size: .m, color: .red)
        // Creates a separate instance of an individual shirt.
      ```

  - Here’s another example of a structure definition, this time with functionality added. The structure defines the attributes and functionality of a Car object and describes firstCar and secondCar as two instances.

    - ```swift
        struct Car {
          var make: String
          var model: String
          var year: Int
          var topSpeed: Int
         
          func startEngine() {
            print(”The \(year) \(make) \(model)’s engine has started.”)
        }
         
          func drive() {
            print(”The \(year) \(make) \(model) is moving.”)
          }
         
          func park() {
            print(”The \(year) \(make) \(model) is parked.”)
          }
        }
         
        let firstCar = Car(make: “Honda”, model: “Civic”, year: 2010,
        topSpeed: 120)
        let secondCar = Car(make: “Ford”, model: “Fusion”, year: 2013,
        topSpeed: 125)
         
        firstCar.startEngine()
        firstCar.drive()
        Console Output:
        The 2010 Honda Civic’s engine has started.
        The 2010 Honda Civic is moving.
      ```

  - What did the cars in this code do? If you imagine firstCar and secondCar facing out of the same driveway, only firstCar has moved after executing this code, while secondCar hasn’t even started the engine.

- **Initializers**

  - All structures come with at least one initializer. An initializer is similar to a function that returns a new instance of the type. Many common types have a default initializer with no arguments, init().
  - Instances created from this initializer have a default value. The default String is “”, the default Int is 0, and the default Bool is false:

    - ```swift
        var string = String.init() // “”
        var integer = Int.init() // 0
        var bool = Bool.init() // false
      ```

  - But there's a shorthand syntax for initializers that's much more common. The code in the following snippet is more concise, but works the same as the example above:

    - ```swift
        var string = String() // “”
        var integer = Int() // 0
        var bool = Bool() // false
      ```

  - Whenever you define a new type, you must consider how you’ll create new instances. This lesson covers different approaches to initializing property values.

  - **Default Values**

    - During initialization of new instances, Swift requires you to set values for all instance properties.
    - One approach is to provide default property values in your type definition. Each instance is initialized with those values. This is useful when defining objects that have a consistent default state, such as a zero reading on an odometer.
    - If you provide default values for all instance properties of a structure, the Swift compiler will generate a default initializer for you.
    - In the previous section you saw default values for String, Int, and Bool. Using default property values, you can create a default state for each new instance of your custom types.

      - ```swift
          struct Odometer {
            var count: Int = 0
          }
           
          let odometer = Odometer()
          print(odometer.count)
          Console Output:
          0
        ```

    - Note that count is set to a default value of 0 when declaring the property. All new instances of Odometer will be created with that default value.

  - **Memberwise Initializers**

    - When you define a new structure and don't declare your own initializers, Swift creates special initializers, called memberwise initializers, that allow you to set initial values for each property of the new instance.

      - ```swift
          let odometer = Odometer(count: 27000)
          print(odometer.count)
          Console Output:
          27000
        ```

    - Memberwise initializers are the correct approach when there’s not a default state for new instances of your type.
    - Consider a Person structure with a name property. What would you assign as the default value for name?

      - ```swift
          struct Person {
            var name: String
          }
        ```

    - At first glance, you may say that the default value for name could be “”. But an empty String is not a name, and you don’t want to accidentally initialize a Person with an empty name.
    - To call a memberwise initializer, use the type name followed by parentheses containing parameters that match each property. In fact, you’ve seen memberwise initializers in the various code snippets throughout this lesson:

      - ```swift
          struct Person {
            var name: String
           
            func sayHello() {
              print(”Hello, there!”)
            }
          }
           
          let person = Person(name: “Jasmine”) // Memberwise initializer
           
          struct Shirt {
            var size: Size
            var color: Color
          }
           
          let myShirt = Shirt(size: .xl, color: .blue) // Memberwise
          Initializer
           
          struct Car {
            var make: String
            var model: String
            var year: Int
            var topSpeed: Int
          }
           
          let firstCar = Car(make: “Honda”, model: “Civic”, year: 2010,
          topSpeed: 120) // Memberwise initializer
        ```

    - You might define a structure for which some properties have reasonable default values, but others don't. For example, a bank account might start with a default zero balance, but require a unique account number.

      - ```swift
          struct BankAccount {
              var accountNumber: Int
              var balance: Double = 0
          }
        ```

    - In this case, you'll get two memberwise initializers: One that provides parameters for each property, and another that provides parameters only for the properties without default values.

      - ```swift
          var newAccount = BankAccount(accountNumber: 123)
          var transferredAccount = BankAccount(accountNumber: 456, balance: 1200)
        ```

    - Memberwise initializers are the most common way to create new instances of your custom structures. But there may be times when you want to define an initializer that completes some custom logic before assigning all of the properties. In those cases, you can define a custom initializer.

  - **Custom Initializers**

    - You can customize the initialization process by defining your own initializer. Custom initializers have the same requirement as default and memberwise initializers: All properties must be set to initial values before completing initialization.
    - Consider a Temperature struct with a celsius property. If you have access to a temperature in Celsius, you could initialize it using a memberwise initializer.
    - But if you have access to a temperature in Fahrenheit, you would need to convert that value to Celsius before using the memberwise initializer.

      - ```swift
          struct Temperature {
            var celsius: Double
          }
           
          let temperature = Temperature(celsius: 30.0)

          let fahrenheitValue = 98.6
          let celsiusValue = (fahrenheitValue - 32) / 1.8
           
          let temperature = Temperature(celsius: celsiusValue)
        ```

    - But the memberwise initializer required you to calculate the Celsius value before initializing a new Temperature object. Instead, you could create a custom initializer that takes a Fahrenheit value as a parameter, performs the calculation, and assigns the value to the celsius property.

      - ```swift
          struct Temperature {
            var celsius: Double
           
            init(celsius: Double) {
              self.celsius = celsius
            }
           
            init(fahrenheit: Double) {
              celsius = (fahrenheit - 32) / 1.8
            }
          }
           
          let currentTemperature = Temperature(celsius: 18.5)
          let boiling = Temperature(fahrenheit: 212.0)
           
          print(currentTemperature.celsius)
          print(boiling.celsius)
          Console Output:
          18.5
          100.0
        ```

    - You might notice that there's a memberwise initializer in the example above. When you add a custom initializer to a type definition, you must define your own memberwise initializers and default initializers; Swift no longer provides them for you.
    - You can add multiple custom initializers. The code below redefines Temperature to add a Kelvin initializer and a default initializer.

      - ```swift
          struct Temperature {
            var celsius: Double
           
            init(celsius: Double) {
              self.celsius = celsius
            }
           
            init(fahrenheit: Double) {
              celsius = (fahrenheit - 32) / 1.8
            }
           
            init(kelvin: Double) {
              celsius = kelvin - 273.15
            }
            init() {
              celsius = 0
            }
          }
           
          let currentTemperature = Temperature(celsius: 18.5)
          let boiling = Temperature(fahrenheit: 212.0)
          let absoluteZero = Temperature(kelvin: 0.0)
          let freezing = Temperature()
           
          print(currentTemperature.celsius)
          print(boiling.celsius)
          print(absoluteZero.celsius)
          print(freezing.celsius)
          Console Output:
          18.5
          100.0
          -273.15
          0
        ```

    - Each instance of Temperature is created using a different initializer and a different value, but each ends as a Temperature object with the required celsius property.

- **Instance Methods**

  - Instance methods are functions that can be called on specific instances of a type. They provide ways to access and modify properties of the structure, and they add functionality that relates to the instance’s purpose.
  - As you learned earlier, you add an instance method by adding a function within a type definition. You can then call that function on instances of the type. You may have noticed this syntax in the Person or Car structures earlier.
  - Consider a Size struct with an instance method area() that calculates the area of a specific instance by multiplying its width and height:

    - ```swift
        struct Size {
          var width: Double
          var height: Double
         
          func area() -> Double {
            width * height
          }
        }
         
        let someSize = Size(width: 10.0, height: 5.5)
        let area = someSize.area() // Area is assigned a value of 55.0
      ```

  - The `someSize` instance is of the `Size` type, and `width` and `height` are its properties. The `area()` is an instance method that can be called on all instances of the Size type.

- **Mutating Methods**

  - Occasionally you’ll want to update the property values of a structure within an instance method. To do so you’ll need to add the `mutating` keyword before the function.
  - In the following example, a simple structure stores mileage data about a specific Car object. Before looking at the code, consider what data the mileage counter needs to store and what actions it needs to perform.

    - Store the mileage count to be displayed on an odometer
    - Increment the mileage count to update the mileage when the car drives
    - Potentially reset the mileage count if the car drives beyond the number of miles that can be displayed on the odometer.

      - ```swift
          struct Odometer {
            var count: Int = 0 // Assigns a default value to the `count` property.

            mutating func increment() {
              count += 1
            }
           
            mutating func increment(by amount: Int) {
              count += amount
            }
           
            mutating func reset() {
              count = 0
            }
          }
           
          var odometer = Odometer() // odometer.count defaults to 0
          odometer.increment() // odometer.count is incremented to 1
          odometer.increment(by: 15) // odometer.count is incremented to 16
          odometer.reset() // odometer.count is reset to 0
        ```

    - The `odometer` instance is of the `Odometer` type, and `increment()` and `increment(by:)` are instance methods that add miles to the instance. The `reset()` instance method resets the mileage count to zero.

- **Computed Properties**

  - Swift has a feature that allows a property to perform logic that returns a calculated value.
  - Consider the Temperature example. While most of the world uses the Celsius scale of measurement for temperature, some places (such as the U.S.) use Fahrenheit, and certain professions use Kelvin. So it might be useful for the Temperature structure to support all three measurement systems.

    - ```swift
        struct Temperature {
          var celsius: Double
          var fahrenheit: Double
          var kelvin: Double
        }
      ```

  - Imagine that you’d used the memberwise initializer for this structure: `let temperature = Temperature(celsius: 0, fahrenheit: 32.0, kelvin: 273.15)`
  - Any time you would write code to initialize a Temperature object, you would need to calculate each temperature and pass all those values as parameters.
  - An alternative would be to add multiple initializers that handle the calculations.

    - ```swift
        struct Temperature {
          var celsius: Double
          var fahrenheit: Double
          var kelvin: Double
         
          init(celsius: Double) {
            self.celsius = celsius
            fahrenheit = celsius * 1.8 + 32
            kelvin = celsius + 273.15
          }
         
          init(fahrenheit: Double) {
            self.fahrenheit = fahrenheit
            celsius = (fahrenheit - 32) / 1.8
            kelvin = celsius + 273.15
          }
         
          init(kelvin: Double) {
            self.kelvin = kelvin
            celsius = kelvin - 273.15
            fahrenheit = celsius * 1.8 + 32
          }
        }
         
        let currentTemperature = Temperature(celsius: 18.5)
        let boiling = Temperature(fahrenheit: 212.0)
        let freezing = Temperature(kelvin: 273.15)
      ```

  - The approach above, using multiple initializers, involves managing a lot of state, or information. Any time the temperature changes, you would be required to update all three properties. This approach is error-prone, and would be frustrating for any programmer.
  - Swift provides a safer approach. With computed properties, you can create properties that can compute their value based on other instance properties or logic.

    - ```swift
        struct Temperature {
          var celsius: Double
         
          var fahrenheit: Double {
            celsius * 1.8 + 32
          }
         
          var kelvin: Double {
            celsius + 273.15
          }
        }
      ```

  - To add a computed property, you declare the property as a variable (because its value can change). You must also explicitly declare the type. Then you use an open curly brace ({) and closing curly brace (}) to define the logic that calculates the value to return.
  - You can access computed properties using dot syntax, just as you would with any other property.

    - ```swift
        let currentTemperature = Temperature(celsius: 0.0)
        print(currentTemperature.fahrenheit)
        print(currentTemperature.kelvin)
        Console Output:
        32.0
        273.15
      ```

  - The logic contained in a computed property will be executed each time the property is accessed, so the returned value will always be up to date.

- **Property Observers**

  - Swift allows you to observe any property and respond to the changes in the property’s value. These property observers are called every time a property’s value is set, even if the new value is the same as the property’s current value. There are two observer closures, or blocks of code, that you can define on any given property: `willSet`, and `didSet`.
  - In the following example, a `StepCounter` has been defined with a `totalSteps` property. Both the `willSet` and `didSet` observers have been defined. Whenever `totalSteps` is modified, `willSet` will be called first, and you’ll have access to the new value that will be set to the property value in a constant named `newValue`. After the property’s value has been updated, `didSet` will be called, and you can access the previous property value using `oldValue`.

    - ```swift
        struct StepCounter {
            var totalSteps: Int = 0 {
                willSet {
                    print(”About to set totalSteps to \(newValue)”)
                }
                didSet {
                    if totalSteps > oldValue  {
                        print(”Added \(totalSteps - oldValue) steps”)
                    }
                }
            }
        }
      ```

  - Here’s the output when modifying the totalSteps property of a new StepCounter:

    - ```swift
        var stepCounter = StepCounter()
        stepCounter.totalSteps = 40
        stepCounter.totalSteps = 100
        Console Output:
        About to set totalSteps to 40
        Added 40 steps
        About to set totalSteps to 100
        Added 60 steps
      ```

- **Type Properties and Methods**

  - You learned that instance properties are data about the individual instance of a type, and instance methods are functions that can be called on individual instances of a type.
  - Swift also supports adding type properties and methods, which can be accessed or called on the type itself. Use the static keyword to add a property or method to a type.
  - Type properties are useful when a property is related to the type, but not a characteristic of an instance itself.
  - The following sample defines a Temperature structure that has a static property named boilingPoint, which is a constant value for all Temperature instances.

    - ```swift
        struct Temperature {
          static var boilingPoint = 100
        }
      ```

  - You access type properties using dot syntax on the type name: `let boilingPoint = Temperature.boilingPoint`.
  - Type methods are similar to type properties. Use a type method when the action is related to the type, but not something that a specific instance of the type should perform.
  - The `Double` structure, defined in the Swift Standard Library, contains a static method named `minimum` that returns the lesser of its two parameters: `let smallerNumber = Double.minimum(100.0, -1000.0)`.

- **Copying**

  - If you assign a structure to a variable or pass an instance as a parameter into a function, the values are copied. Separate variables are therefore separate instances of the value, which means that changing one value doesn’t change the other.

    - ```swift
        var someSize = Size(width: 250, height: 1000)
        var anotherSize = someSize
         
        someSize.width = 500
         
        print(someSize.width)
        print(anotherSize.width)
        Console Output:
        500
        250
      ```

  - Note that the width property of someSize changed to have a value of 500, but the width property of anotherSize did not, because although we set anotherSize equal to someSize, this created a copy of someSize, and the copy’s width did not change when the original width was changed.

- **Self**

  - You may have noticed the word self in this section. In Swift, self refers to the current instance of the type. It can be used within an instance method or computed property to refer to its own instance.

    - ```swift
        struct Car {
          var color: Color
         
          var description: String {
            return “This is a \(self.color) car.”
          }
        }
      ```

  - Many languages require the use of self to refer to instance properties or methods within the type definition. The Swift compiler recognizes when property or method names exist on the current object, and makes using self optional.
  - This example is functionally the same as the previous example.

    - ```swift
        struct Car {
          var color: Color
         
          var description: String {
            return “This is a \(color) car.”
          }
        }
      ```

  - The use of self is required within initializers that have parameter names that match property names.

    - ```swift
        struct Temperature {
          var celsius: Double
         
          init(celsius: Double) {
            self.celsius = celsius
          }
        }
      ```

  - This concept is called shadowing, and you will learn more about it in a future lesson.

- **Variable Properties**

  - Did you notice that all of the structure examples in this lesson used variable properties instead of constants? Consider the Car definition used at the beginning of the lesson.

    - ```swift
        struct Car {
          var make: String
          var year: Int
          var color: Color
          var topSpeed: Int
        }
      ```

  - A car’s color could easily be changed with a paint job, and the top speed might get updated if the owner upgrades the engine. But the make and year of a car will never change, so why not define the properties using let?
  - Variable properties provide a convenient way to create new data from old data. In the following code, making a blue, 2010 Ford is as simple as making a copy of the 2010 Honda and modifying the make property. If the make property were constant, the second car would need to be created using the memberwise initializer.

    - ```swift
        var firstCar = Car(make: “Honda”, year: 2010, color: .blue, topSpeed: 120)
        var secondCar = firstCar
        secondCar.make = “Ford”
      ```

  - Earlier in this lesson, you learned that whenever an instance of a struct is assigned to a new variable, the values are copied. In the previous example, firstCar is still a Honda. If you want to explicitly prevent firstCar’s properties from ever changing, simply declare the instance using a let.

    - ```swift
        let firstCar = Car(make: “Honda”, year: 2010, color: .blue,
        topSpeed: 120)
        firstCar.color = .red // Compiler error!
      ```

  - Even if the properties are declared using var, the values of a constant cannot be changed. As a general rule, you should use let whenever possible to define an instance of a structure, use var if the instance needs to be mutated, and use var when defining the properties of a structure.

### Lesson 2.5 Classes and Inheritance

- Classes are very similar to structures. Among other similarities, both can define properties to store values, define methods to provide functionality, and define initializers to set up their initial state. The syntax for doing these things is almost always identical.
- You define a class using the class keyword along with a unique name. You then define properties as part of the class by listing the constant or variable declarations with the appropriate type annotation. As with structures, it’s best practice to capitalize the names of types and to use lowercase for the names of properties:
- You can add functionality to a class by adding functions to the class definition:

  - ```swift
      class Person {
        let name: String
       
        init(name: String) {
          self.name = name
        }

        func sayHello() {
          print(”Hello, there!”)
        }
      }
       
      let person = Person(name: “Jasmine”)
      print(person.name)
      person.sayHello()
      Console Output:
      Jasmine
      Hello, there!
    ```

- You’ve seen an almost-identical example in the previous lesson on structures. But how do classes differ from structures?

- **Inheritance**

  - The biggest difference between structures and classes is that classes can have hierarchical relationships. Any class can have parent and child classes. A parent class is called a superclass, and a child class is called a subclass.
  - Just as in family relationships, subclasses inherit properties and methods from superclasses. However, subclasses can augment or replace the implementation of superclass properties and methods.
  - In the sections below, you’ll read how to define a base class, which is a class that has no parent classes, how to define subclasses, and how to override properties or methods from the base class.

  - **Defining a Base Class**

    - A class that doesn’t inherit from a superclass is known as a base class. All the classes that you’ve seen so far are base classes.
    - Here’s an example of a base class for a Vehicle object:

      - ```swift
          class Vehicle {
              var currentSpeed = 0.0
           
              var description: String {
                  “traveling at \(currentSpeed) miles per hour”
              }
           
              func makeNoise() {
                  // do nothing - an arbitrary vehicle doesn’t necessarily make a noise
              }
          }

          let someVehicle = Vehicle()
          print(”Vehicle: \(someVehicle.description)”)
          Console Output:
          Vehicle: traveling at 0.0 miles per hour
        ```

    - The Vehicle class has a property called currentSpeed with a default value of 0.0. The currentSpeed property is used in the computed description variable that returns a human readable description of the vehicle. The class also has a method called makeNoise(). This method does not actually do anything for a base Vehicle instance, but will be customized by subclasses later.
    - The Vehicle class defines common characteristics, like properties and methods, for any type of vehicle – like cars, bicycles, or airplanes. It is not very useful on it’s own, but it will make it easier to define other more specific types.

  - **Create a Subclass**

    - Subclassing is the act of basing a new class on an existing class. The subclass inherits properties and methods from the superclass, which you can then refine and make more specific. You can also add new properties or methods to the subclass.
    - To define a new type that inherits from a superclass, write the type name before the superclass name, separated by a colon: `class SomeSubclass: SomeSuperclass { // subclass definition goes here }`
      - The following example defines a subclass called Bicycle, with a superclass of Vehicle: `class Bicycle: Vehicle { var hasBasket = false }`
      - The new Bicycle class automatically inherits all of the properties and methods of Vehicle, such as its currentSpeed and description properties and its makeNoise() method.
    - In addition to the inherited properties and methods, the Bicycle class defines a new boolean property hasBasket. By default, new instance of Bicycle will not have a basket. You can set the hasBasket property to true for a particular Bicycle instance after it has been created, or within a custom initializer for the type.
    - As you’d expect, you can also update the currentSpeed property, which will impact the description of the instance.

      - ```swift
          let bicycle = Bicycle()
          bicycle.hasBasket = true
          bicycle.currentSpeed = 15.0
          print(”Bicycle: \(bicycle.description)”)
          Console Output:
          Bicycle: traveling at 15.0 miles per hour
        ```

    - Subclasses can themselves be subclassed. For example, you can create a class that represents a two-seater TandemBike.

      - ```swift
          class Tandem: Bicycle {
              var currentNumberOfPassengers = 0
          }
        ```

    - Tandem inherits all of the properties and methods from Bicycle, which in turn inherits all of the properties and methods from Vehicle. The Tandom subclass also adds a new property called currentNumberOfPassengers, with a default value of 0.
    - If you create a new instance of Tandem, you’ll have access to all of the inherited properties and methods.

      - ```swift
          let tandem = Tandem()
          tandem.hasBasket = true
          tandem.currentNumberOfPassengers = 2
          tandem.currentSpeed = 22.0
          print(”Tandem: \(tandem.description)”)
          Console Output:
          Tandem: traveling at 22.0 miles per hour
        ```

  - **Override Methods and Properties**

    - One advantage of subclassing is that each subclass can provide its own custom implementation of a property or method. To override a characteristic that would otherwise be inherited, like writing a new implementation for a function, you prefix your new definition with the override keyword.
    - The following example defines a new Train class, which overrides the makeNoise() method that Train inherits from Vehicle:

      - ```swift
          class Train: Vehicle {
              override func makeNoise() {
                  print(”Choo Choo!”)
              }
          }

          let train = Train()
          train.makeNoise()
          Console Output:
          Choo Choo!
        ```

    - You can also override properties by providing a getter, or a block of code that returns the value, like a computed property. The following example defines a new class called Car, which is a subclass of Vehicle. The new class has a new gear property, with a default value of 1. The Car class also overrides the description property to provide a custom description that includes the current gear:

      - ```swift
          class Car: Vehicle {
              var gear = 1
              override var description: String {
                  super.description + “ in gear \(gear)”
              }
          }
        ```

    - Notice that the new implementation accesses the description from the superclass by calling super.description. The new implementation then adds some extra text onto the end of the description to provide information about the gear.

      - ```swift
          let car = Car()
          car.currentSpeed = 25.0
          car.gear = 3
          print(”Car: \(car.description)”)
          Console Output:
          Car: traveling at 25.0 miles per hour in gear 3
        ```

  - **Override Initializer**

    - Suppose you have a Person class with a name property. The initializer sets the name to the parameter specified.

      - ```swift
          class Person {
            let name: String
           
            init(name: String) {
              self.name = name
            }
          }
        ```

    - Now imagine you want to create a Student, which is a subclass of Person. Each Student includes an additional property, favoriteSubject.

      - ```swift
          class Student: Person {
            var favoriteSubject: String
          }
        ```

    - If you try to compile this code, Student will fail, because you haven’t provided an initializer that sets the favoriteSubject property to an initial value. Since the Person superclass already does the work of initializing the name property, the Student initializer can call the superclass's initializer using super.init(). You should call this initializer after you’ve provided values for any properties added within your subclass.

      - ```swift
          class Student: Person {
            var favoriteSubject: String
           
            init(name: String, favoriteSubject: String) {
              self.favoriteSubject = favoriteSubject
              super.init(name: name)
            }
          }
        ```

    - By calling the superclass's initializer, the Student class doesn’t have to duplicate the work that was already written in the Person initializer.

- **References**

  - A special feature of classes is their ability to reference values assigned to a constant or variable. When you create an instance of a class, Swift picks out a region in the device's memory to store that instance. That region in memory has an address. Constants or variables that are assigned the instance store that address to refer to the instance.
  - So the constant or variable does not contain the value itself, it points to the value in memory.
  - When you assign a class to multiple variables, each variable will reference, or point to, the same address in memory. So if you update one of the variables, both variables will be updated.

    - ```swift
        class Person {
          let name: String
          var age: Int
         
          init(name: String, age: Int) {
            self.name = name
            self.age = age
          }
        }
         
        var jack = Person(name: “Jack”, age: 24)
        var myFriend = jack
         
        jack.age += 1
         
        print(jack.age)
        print(myFriend.age)
        Console Output:
        25
        25
      ```

  - In contrast, when you create an instance of a structure, you’re assigning a literal value to that variable. If you create a variable that’s equal to another structure variable, the value is copied. Any operations you perform on either variable will be reflected only on the modified variable.

    - ```swift
        struct Person {
          var name: String
          var age: Int
        }
         
        var jack = Person(name: “Jack”, age: 24)
        var myFriend = jack
         
        jack.age += 1
         
        print(jack.age)
        print(myFriend.age)
        Console Output:
        25
        24
      ```

- **Memberwise Initializers**
  - You’ve learned that all property values must be set when you create an instance of a class. Unlike for structures, Swift does not create a memberwise initializer for classes. However, it’s common practice for developers to create their own memberwise initializer for classes they define, ensuring that all initial values are set for each instance of any object.
- **Class or Structure?**

  - Because classes and structures are so similar, it can be hard to know when to use classes and when to use structures for the building blocks of your program.
  - As a basic rule, you should start new types as structures until you need one of the features that classes provide.
  - Start with a class when you’re working with a framework that uses classes or when you want to refer to the same instance of a type in multiple places.
  - **Working with Frameworks That Use Classes**
    - You’ll often work with resources that you didn’t write, such as frameworks like Foundation or UIKit. In these situations, you may start with a base class, then create a subclass to add your own specific functionality. For example, when you’re working with UIKit and want to create a custom view, you create a subclass of UIView.
    - When working with frameworks, it’s often an expectation that you’ll pass around class instances. Many frameworks have method calls that expect certain things to be classes. So in these cases, you’ll always choose to use a class over a structure.
  - **Stable Identity**

    - There are times when you want to use a single instance of an object in multiple places, but it doesn’t make sense to copy the instance. Because each class constant or variable is an address that points to the same data, the data has a stable identity.
    - Consider a UITableViewCell subclass MessageCell that represents a row in a table view. The cell is designed to display information about an email message. Each instance of a MessageCell will be accessed in many places in code, as you will see.

      - ```swift
          class MessageCell: UITableViewCell {
           
            func update(message: Message) {
              // Update `UITableViewCell` properties with information about the message

              textLabel.text = message.subject
              detailTextLabel.text = message.previewText
            }
          }
        ```

    - When a table view is preparing to display cells, it calls a function cellForRow(at: IndexPath) to request the cell it should display at each position in the list. All cells for a table view are initialized (and put into memory) during this function call.

      - ```swift
          override func tableView(_ tableView: UITableView, cellForRowAt indexPath: IndexPath) -> UITableViewCell {
            let cell = MessageCell(style: .default, reuseIdentifier: “MessageCell”)
            cell.update(message: message)
            return cell  // Returns the cell to the table view that called this method to request it
          }
        ```

    - When the user scrolls through the list of messages in the table view, a method is called that allows your program to set up, update, or modify the cell as it is about to be displayed. The function passes a reference to the cell as a parameter.

      - ```swift
          override func tableView(_ tableView: UITableView, willDisplay cell: UITableViewCell, forRowAt indexPath: IndexPath) {
            // Perform any operations you want to take on the cell here
          }
        ```

    - There’s some unfamiliar syntax here, which you’ll learn more about later. For now, focus on the fact that the function is called for each cell that’s about to appear on the table view. Also notice that the function passes three parameters: a reference to the tableView, which already exists; the cell that already exists but is about to be displayed; and something called indexPath.
    - Because tableView and cell are both classes, the parameters are references to the tableView and cell in memory. If you update the cell parameter, you’re updating the same cell that was initialized in the cellForRow function, the same cell that’s about to be displayed.
    - Consider how a class works differently from a structure. If cell were a structure, or a value type, the parameter would be a new copy of the cell that’s about to be displayed. So if you updated cell, you wouldn’t see your changes, because you updated the copy and not the cell that’s about to be displayed.

### Lesson 2.6 Collections

- Swift defines two collection types you will frequently work with: arrays and dictionaries. Each type provides a unique method for interacting with multiple objects. As you progress through learning the different types, you’ll notice that they share certain functionality: adding/removing items, accessing individual items, and providing type information about the data within the collection.

- **Arrays**

  - The most common collection type in Swift is an array, which stores an ordered list of same-typed values. When you declare an array, you can specify what type of values will be held in the collection, or you can let the type inference system discover the type.
  - An array is often initialized using a literal, similar to an Int or String literal. To declare an array literal, surround the collection of values with brackets, with commas separating the values: `[value1, value2, value3]`
  - You’ll use similar syntax to declare an array that stores strings. Notice in the following example that the variable’s type, String, is surrounded by brackets: `var names: [String] = [”Anne”, “Gary”, “Keith”]`
  - Since type inference can determine that “Anne”, “Gary”, and “Keith” are strings, you could actually skip a step and declare the array without specifying the array’s type: `var names = [”Anne“, “Gary”, “Keith”]`
  - But there might be situations when you want to specify the array’s type even though type inference can discover it. Imagine, for example, you want a collection of 8-bit integers (numbers between -127 and 128). You begin by assigning a variable to the following collection of numbers: `var numbers = [1, -3, 50, 72, -95, 115]`
  - Swift will infer all the values to be of type Int and set numbers to be an array of integers, or [Int]. While this inference is certainly correct, there’s a problem: An Int can hold positive and negative numbers that exceed beyond the range from -127 to 128. To help Swift understand that you want to restrict the array to smaller integers, you can specify the type as [Int8], an array of 8-bit integers whose values are restricted to the aforementioned range: `var numbers: [Int8] = [1, -3, 50, 72, -95, 115]`
  - What if you tried to include a larger number, such as 300, in an array literal of type [Int8]? Swift will return an error because 300 is greater than the maximum number for an Int8. You should specify the type if the inferred type is not specific enough, and it will help to restrict the values that you don’t want to allow.
  - It’s often useful to check if a certain value exists in an array. To do so, you can use the `contains(_:)` method, passing in the desired value. If the array contains the value, the expression is true; otherwise, it’s false:

    - ```swift
        let numbers = [4, 5, 6]
        if numbers.contains(5) {
          print(”There is a 5”)
        }
      ```

  - Early in this course, you learned that constants can’t be modified once they’re declared. It’s the same when you assign a collection to a constant using `let`: You can’t add, remove, or modify any items within the collection. However, if you store the collection within a variable using `var`, you’ll be able to add to, remove from, or modify items in the collection. In addition, you’ll be able to empty the collection or set the variable to a different collection entirely.

- **Array Types**

  - An array is like a basket: It can start out empty and you can fill it with values at a later time. But if an array literal doesn’t contain any values, how can its type be inferred?
  - You can declare the type of an array using type annotation, collection type annotation, or an array initializer.
  - This example defines an array with traditional type annotation: `var myArray: [Int] = []`
  - This example defines an array using a special collection type annotation. This is a less common practice you should be familiar with in case you run across it in code you’re working with: `var myArray: Array<Int> = []`
  - Just like all objects can be initialized by adding a () after the type name, you can add a () after [Int] to initialize an empty array of Int objects. You should also be familiar with this code in case you run across it in the future: `var myArray = [Int]()`

- **Working With Arrays**

  - You may find some situations when it’s tedious or error-prone to use array literals. For example, say you want an array filled with 100 zeros. In array literal form, you’d have to enter all 100 zeros, and it would be easy to miscount them.
  - That’s OK. Swift has a solution. Instead of counting out the 100 zeros, you can use the following initializer to create an array of count 100 with repeating default values: `var myArray = [Int](repeating: 0, count: 100)`
  - To find out the number of items within an array, you can use its `count` property. What if you wanted to check if the array is empty? Rather than comparing count to 0, you can check the array’s isEmpty property, which returns a Bool:

    - ```swift
        let count = myArray.count
        if myArray.isEmpty { }
      ```

  - Once you’ve defined an array, you can use various methods and properties to access or modify it. You can also use an array’s subscript syntax. Subscript syntax uses square brackets after a collection to refer to a specific element or range inside the collection. To retrieve a particular value from a collection, specify inside square brackets the index of the value you wish to access. An array’s values are always zero-indexed, meaning that the first element of an array has an index of zero. The following example will retrieve the first value in a collection of first names: `let firstName = names[0]`
  - You can also use subscript syntax to change a value at a given index. By putting the subscript on the left side of the = sign, you can set a particular value rather than access the current one. In the example, you’re changing the second name in the collection to “Paul”.\: `names[1] = “Paul”`
  - When subscripting an array, you need to be sure that the index you specify exists in the array. For example, if you specify 3 as the index, the array must have at least four elements. If it doesn’t, your program will crash when that line of code is executed.
  - After defining an array and setting some values, you’ll often want to append new values. You can use a variable array’s append function to add a new element at the end of the array. To append multiple elements at once, use the += operator.

    - ```swift
        var names = [”Amy”]
        names.append(”Joe”)
        names += [”Keith”, “Jane”]
        print(names) // [”Amy”, “Joe”, “Keith”, “Jane”]
      ```

  - What if you didn’t want the new element to show up at the end of the array? A variable array also has an `insert(_:at:)` function that allows you to specify the value and the index. In this scenario, as with subscripting, you’ll need to be sure that you supply a valid index.
  - Because an array is zero-indexed, the first element always has an index of 0, and the last element’s index is equal to count – 1. In the following example, “Bob” is inserted at the beginning of the array: `names.insert(”Bob”, at: 0)`
  - Similarly, the `remove(at:)` function works to remove an item at a specified index. Unlike `insert(_:at:)`, you don’t need to enter the value; the function returns the removed item by default, as in the example below. Another method is `removeLast()`, which removes the last item from the array, eliminating the need to calculate the index. Finally, the `removeAll()` method will remove all elements from the array.

    - ```swift
        var names = [”Amy”, “Brad”, “Chelsea”, “Dan”]
        let chelsea = names.remove(at: 2)
        let dan = names.removeLast()
        names.removeAll()
      ```

  - Swift also allows you to create a new array by adding together two existing arrays of the same type. You can specify which array comes first within the resulting array: `var myNewArray = firstArray + secondArray`
  - What about arrays within an array? Use the array literal syntax to place two arrays inside another containing array. You can then use subscript syntax on the container array to access one of the nested arrays. To access a particular element within one of the nested arrays, you can use two sets of subscripts.

    - ```swift
        let array1 = [1,2,3]
        let array2 = [4,5,6]
        let containerArray = [array1, array2] // [ [1,2,3], [4,5,6] ]
        let firstArray = containerArray[0]  // [1,2,3]
        let firstElement = containerArray[0][0] // 1
      ```

- **Dictionaries**

  - The second type of collection in Swift is a dictionary. Like a real-world dictionary that contains a list of words and their definitions, a Swift dictionary is a list of keys, each with an associated value. Each key must be unique, just like each word in the dictionary is unique. And just as an English dictionary is in alphabetical order to make the words easy to look up, a Swift dictionary is optimized to make key lookups very fast.
  - You can set up a dictionary using a dictionary literal: a list of comma-separated key/value pairs surrounded by square brackets. A colon separates each key and its resulting value: `[key1: value1, key2: value2, key3: value3]`
  - Just as with an array, the dictionary’s type can be inferred based on the types used in the dictionary literal. Say you want to store a list of high scores in a game. You’ll use the player’s name as the key and the player’s score as the corresponding value. The dictionary’s type will be inferred as a dictionary where the keys are of type String and the values are of type Int. This can be represented as either `[String: Int]` or `Dictionary<String, Int>`: `var scores = [”Richard”: 500, “Luke”: 400, “Cheryl”: 800]`
  - As with other collection types, a dictionary has a count property to determine the number of key-value pairs and an isEmpty property to determine whether the dictionary has no key-value pairs. The syntax for creating an empty dictionary is probably familiar by now:

    - ```swift
        var myDictionary = [String: Int]()
         
        var myDictionary = Dictionary<String, Int>()
         
        var myDictionary: [String: Int] = [:]
      ```

  - All of these examples result in the same type of empty dictionary. You'll likely have a preferred method you use regularly, but you should be familiar with all of them. Take note of the syntax for an empty dictionary literal in the last example.

- **Add/Remove/Modify a Dictionary**

  - Subscript syntax is particularly handy with a dictionary. Since the order in a Swift dictionary doesn’t matter, there’s no index and there’s no risk of subscripting errors associated with indices.
  - The following example adds a new score to the dictionary of high scores. If the key “Oli” already exists in the dictionary, this code will replace the old value with the new one: `scores[”Oli”] = 399`
  - But what if you want to know if there’s an old value in the dictionary before replacing it? You can use `updateValue(_:, forKey:)` to update the dictionary, and the value returned from the method will be equal to the old value, if one existed. In the following example, oldValue will be equal to Richard’s old value before the update. If there was no value, oldValue will be `nil`. You’ll learn more about the `nil` keyword later. It’s a special way of representing the absence of a value: `let oldValue = scores.updateValue(100, forKey: “Richard”)`
  - Swift uses if-let syntax to let you run code only if a value is returned from the method. If there wasn’t an existing value, the code within the braces wouldn’t be executed:

    - ```swift
        if let oldValue = scores.updateValue(100, forKey: "Richard") {
          print("Richard's old value was \(oldValue)")
        }
      ```

  - To remove an item from a dictionary, you can use subscript syntax, setting the value to `nil`. Similar to updating a value, dictionaries have a `removeValue(forKey:)` method if you need the old value returned before removing it:

    - ```swift
        var scores = [”Richard”: 100, “Luke”: 400, “Cheryl”: 800]
        scores[”Richard”] = nil // [”Luke”: 400, “Cheryl”: 800]

        if let removedValue = scores.removeValue(forKey: “Luke”) {
          print(”Luke’s score was \(removedValue) before he stopped playing”)
        }
      ```

- **Accessing a Dictionary**

  - Swift dictionaries provide two properties not included in other collection types. You can use keys to return a list of all the keys within a dictionary and values to return a list of all the values. If you want to use these collections subsequently, you’ll need to convert them to arrays:

    - ```swift
        var scores = [”Richard”: 500, “Luke”: 400, “Cheryl”: 800]
         
        let players = Array(scores.keys) // [”Richard”, “Luke”, “Cheryl”]
        let points = Array(scores.values) // [500, 400, 800]
      ```

  - To look up a particular value within a dictionary, use if-let syntax. If the key you specify is in the dictionary, the result will be the key’s corresponding value. However, if the key isn’t in the dictionary, the code within the brackets won’t be executed.

    - ```swift
        if let lukesScore = scores[”Luke”] {
          print(lukesScore)
        }
         
        if let henrysScore = scores[”Henry”] {
          print(henrysScore) // not executed; “Henry” is not a key in the dictionary
        }
        Console Output:
        400
      ```

### Lesson 2.7 Loops

- Computer programs are great at repeating things. Developers often write code to perform the same work across multiple objects, perform a task many times, or continue to perform work until specific conditions have been met. Swift provides three different ways to loop through, or repeat, blocks of code.

- **For Loops**

  - The first loop you'll learn is the for loop, also known more specifically as a for-in loop. A for loop is useful for repeating something a set number of times or for performing work across a collection of values.
  - A for-in loop executes a set of statements for each item within a range, sequence, or collection. Suppose you have a range of numbers between 1 and 5, and you want to print each value within the range. Rather than writing out five print statements, you can use for-in over the range and write one print statement. The syntax looks like this:

    - ```swift
        for index in 1...5 {
          print(”This is number \(index)”)
        }
        Console Output:
        This is number 1
        This is number 2
        This is number 3
        This is number 4
        This is number 5
      ```

  - The `...` is known as the closed range operator, which is how you define a range of values that runs from x up to y and includes both x and y in the range. There's a companion operator (`..<`) known as the half-open range operator. These ranges run from x up to y, but don’t include y.
  - In the code above, index is a constant that’s available to customize the work performed within the braces (the for-in loop). The first time the statement within the braces is executed, index has a value of 1, the first value in the range. When execution is complete, the value of index is updated to 2, the next value in the range. As index is updated to each of the values, the print statement is executed five times. After the entire range has been exhausted, the loop is complete, and the code moves on to statements after the loop.
  - But let’s say your result doesn’t need to use the values in the range. If you just need a way to perform a series of steps a certain number of times, you can skip assigning a value to a constant and replace its name with a `_`:

    - ```swift
        for _ in 1...3 {
          print(”Hello!”)
        }
        Console Output:
        Hello!
        Hello!
        Hello!
      ```

  - You can use the same for-in syntax to iterate over each item in an array.

    - ```swift
        let names = [”Joseph”, “Cathy”, “Winston”]
        for name in names {
          print(”Hello \(name)”)
        }
        Console Output:
        Hello Joseph
        Hello Cathy
        Hello Winston
      ```

  - Because String is a collection type, it has similar functionality to an array. You can use a for-in loop to iterate over each character in a String:

    - ```swift
        for letter in “ABCD” {
          print(”The letter is \(letter)”)
        }
        Console Output:
        The letter is A
        The letter is B
        The letter is C
        The letter is D
      ```

  - What if you need the index of each element in addition to its value? You can use the `enumerated()` method of an array or string to return a tuple — a special type that can hold an ordered list of values wrapped in parentheses — containing both the index and the value of each item:

    - ```swift
        for (index, letter) in “ABCD”.enumerated() {
          print(”\(index): \(letter)”)
        }
        Console Output:
        0: A
        1: B
        2: C
        3: D
      ```

  - Alternatively, you could use the half-open range operator to do the same thing:

    - ```swift
        let animals = ["Lion", "Tiger", "Bear"]
        for index in 0..<animals.count {
          print("\(index): \(animals[index])")
        }
        Console Output:
        0: Lion
        1: Tiger
        2: Bear
      ```

  - If you use a for-in loop with a dictionary, the loop generates a tuple that holds the key and value of each entry. Because a dictionary is typically accessed by specifying a key, the loop doesn't guarantee any particular order of the items as it works through the dictionary:

    - ```swift
        let vehicles = [”unicycle”: 1, “bicycle”: 2, “tricycle”: 3, “quad bike”: 4]
        for (vehicleName, wheelCount) in vehicles {
          print(”A \(vehicleName) has \(wheelCount) wheels”)
        }
        Console Output:
        A unicycle has 1 wheels
        A bicycle has 2 wheels
        A tricycle has 3 wheels
        A quad bike has 4 wheels
      ```

- **While Loops**

  - A while loop will continue to loop until its specified condition is no longer true. Imagine you want to keep playing a game until you run out of “lives.” The condition under which you continue looping is that the number of lives is greater than 0:

    - ```swift
        var numberOfLives = 3
         
        while numberOfLives > 0 {
          playMove()
          updateLivesCount()
        }
      ```

  - Swift checks the condition before each loop is executed, which means it’s possible to skip the loop entirely if the condition is never satisfied. If numberOfLives had been initialized to 0 in the above example, the while loop would determine that 0 > 0 is false and would never proceed to the body of the loop.
  - For this reason, the body of the while loop should perform work that will eventually change the condition. In the example below, nothing is updating the value of numberOfLives, so the condition always resolves to true and continues forever.

    - ```swift
        var numberOfLives = 3
         
        while numberOfLives > 0 {
          print(”I still have \(numberOfLives) lives.”)
        }
      ```

  - Instead, the body should execute statements that will, at some point, result in a false condition:

    - ```swift
        var numberOfLives = 3
        var stillAlive = true
        while stillAlive {
          numberOfLives -= 1
          if numberOfLives == 0 {
            stillAlive = false
          }
        }
      ```

- **Repeat-While Loops**

  - A repeat-while loop is similar to the while loop, but this syntax executes the block once before checking the condition.

    - ```swift
        var steps = 0
        let wall = 2 // there's a wall after two steps

        repeat {
          print("Step")
         
          steps += 1
         
          if steps == wall {
            print("You've hit a wall!")
            break
          }
        } while steps < 10 // maximum in this direction
        Console Output:
        Step
        Step
        You've hit a wall!
      ```

- **Control Transfer Statements**

  - You may have situations when you want to stop execution of a loop from within the loop's body. The Swift keyword break will break the code execution within the loop and start executing any code defined after the loop (you may recognize this from the switch statement).
  - In the code below, the loop breaks if the counter reaches 0:

    - ```swift
        // Prints -3 through 0
        for counter in -3...3 {
          print(counter)
          if counter == 0 {
            break
          }
        }
        Console Output:
        -3
        -2
        -1
        0
      ```

  - There may also be situations in which you want to skip to the next iteration in a loop. While the `break` keyword will end the loop entirely, `continue` will move onto the next iteration. For example, you may have an array where each element is of type Person, and you want to loop through the array and send an email to everyone 18 years of age and older:

    - ```swift
        for person in people {
          if person.age < 18 {
            continue
          }
         
          sendEmail(to: person)
        }
      ```

  - Computers are incredibly good at performing tasks as many times as requested. Whether you need to iterate through a collection or repeat a series of steps until a condition is met, loops are an important concept to understand well. You’ll use them frequently throughout your programming career.

### Lesson 2.8 Introduction to UIKit

- The UIKit framework provides the crucial pieces you need to build and manage iOS apps. It includes definitions for all user interface objects, the event-handling system that responds to user input, and the entire model that allows apps to run in iOS.

#### Common System Views\*\*

- The foundational class for all visual elements defined in UIKit is the UIView, or view. A view defines a rectangular shape that can be customized to display anything on the screen. Text, images, lines, and graphics all depend on UIView as the base.
- UIKit defines dozens of special UIView subclasses that perform specific tasks. For example, UILabel displays text, UIImageView displays an image, and UIScrollView allows you to put scrollable content onto the screen.
- Almost all screens in an app consist of many views, which together make up a view hierarchy.

  - <img src="./resources/view_hierarchy.png" alt="View Hierarchy" width="500" />

  - Views are often nested, as in the the previous view hierarchy diagram. A view that’s contained in another view is called a child view. A view that contains one or more views is called a parent view. In this example, each cell in the list is a child view of a table view, and each cell is a parent to three views: a label that displays a city name, another label that displays how the time zones are related, and an image view that displays an image of a clock.

- To display a view onscreen, you need to give it a frame — which consists of a size and a position — and add it to the view hierarchy. The area within the view is its bounds. When adding a view in Interface Builder, its background color is white by default. When creating a view in code, the background is transparent by default. You can set a new background color in either scenario.

  - Here are some of the attributes you can change when working with views:

    - <img src="./resources/attributes_1.png" alt="View Attributes" width="400" />

      - Tag: Integer that you can use to identify view objects
      - Alpha: Transparency of the view
      - Background Color: Background color that will be displayed

- Next, take a look at some of the most common views defined in UIKit.
- This section covers some common views you’ll work with using UIView. As you learn about the different views, think about apps you use and which views might be used to create their interfaces.
- **Label (UILabel)**

  - Labels use static text to relay information to the user.
  - Configuration

    - <img src="./resources/attributes_2.png" alt="Label Attributes" width="400" />

      - Text: Text displayed on the label
      - Color: Color of the text
      - Font: Font of the text
      - Alignment: Technique to use for aligning the text
      - Number of Lines: Maximum number of lines to use for rendering text

  - [UILabel Developer Documentation](https://developer.apple.com/documentation/uikit/uilabel)

- **Image View (UIImageView)**

  - An image view displays an image or an animated sequence of images. Some people confuse the image view with the image itself. Think of it this way: Just like a label displays text, an image view displays an image.
  - Configuration

    - <img src="./resources/attributes_3.png" alt="Image View Attributes" width="400" />

      - Image: Image displayed by the image view
      - Highlighted Image: Optional image to display when the image view is being tapped by the user

  - [UIImageView Developer Documentation](https://developer.apple.com/documentation/uikit/uiimageview)

- **TextView (UITextView)**

  - A text view allows the user to input text in your app. Text views accept and display multiple lines of text, with support for scrolling and editing. You’ll typically use a text view to display a large amount of text, such as the body of an email message.
  - Configuration

    - <img src="./resources/attributes_4.png" alt="Text View Attributes" width="400" />

      - Text: Starting text displayed by the text view
      - Color: Color of the text
      - Font: Font of the text
      - Alignment: Technique to use for aligning the text
      - Editable: Whether the user can edit the text

  - [UITextView Developer Documentation](https://developer.apple.com/documentation/uikit/uitextview)

- **Scroll View (UIScrollView)**

  - A scroll view allows the user to see content that runs beyond the boundaries of the view. You’ll typically use a scroll view when the information you want to display is larger than the device’s screen.
  - When the user interacts with a scroll view, a vertical or horizontal scroll indicator briefly appears to indicate there’s more content to view.
  - Configuration

    - <img src="./resources/attributes_5.png" alt="Scroll View Attributes" width="400" />

      - Indicators(style): Style of the scroll indicator - Default style, black, or white
      - Show Indicator: Whether to display a horizontal or vertical scroll indicator
      - Scrolling Enabled: Whether the user can scroll the content in the view
      - Paging Enabled: Whether the scrolling is fluid or jumps to the next page
      - Bounces: Whether the content bounces (horizontally and/or vertically) upon reaching the limits of the scrollable or zoomable area

  - [UIScrollView Developer Documentation](https://developer.apple.com/documentation/uikit/uiscrollview)

- **Table View (UITableView)**

  - A table view presents data in a single scrollable column of rows and sections, allowing users to navigate easily through groups of information. Table views are an excellent format for displaying and editing hierarchical lists of information.
  - For example, the Mail app uses a table view to display email messages in the user’s inbox, and the Messages app uses a table view to display message threads organized by contacts.
  - Configuration

    - Table views are interesting because you can customize the look and feel of the table view itself, as well as the look and feel of the rows (or cells) that it displays.

    - <img src="./resources/attributes_6.png" alt="Table View Attributes" width="400" />

  - [UITableView Developer Documentation](https://developer.apple.com/documentation/uikit/uitableview)

- **Toolbars (UIToolbar)**

  - A toolbar usually appears at the bottom of a screen and displays one or more buttons, called bar button items. Users can select a button, or tool, to perform an action within a given view.
  - Configuration

    - You can configure the toolbar itself, or the bar items it displays. Each bar item consists of a title and an image, and can be enabled or disabled programmatically.

    - <img src="./resources/attributes_7.png" alt="Toolbars Attributes" width="200" />

  - [UIToolBar Developer Documentation](https://developer.apple.com/documentation/uikit/uitoolbar)

- **Navigation Bars (UINavigationBar)**

  - You’ll use the navigation bar to present your app’s primary content in an organized way, one that you hope will be intuitive to the user. Navigation bars are typically displayed at the top of the screen, with bar buttons for navigating through a hierarchy of screens. They’ll most likely include a title and a back button.
  - Configuration

    - <img src="./resources/attributes_8.png" alt="Toolbars Attributes" width="400" />

      - Style: Default (gray) or Black
      - Translucent: Whether the navigation bar should be slightly translucent
      - Bar Tint: The tine color to apply to the navigation bar background
      - Title Font: The font of the title displayed by the navigation bar
      - Title Color: The color of the title displayed by the navigation bar

  - [UINavigationBar Developer Documentation](https://developer.apple.com/documentation/uikit/uinavigationbar)

- **Tab Bars (UITabBar)**
  - A tab bar provides easy access to different views in an app. It displays multiple tab bar items, each made up of an icon image and text. You’ll use tab bars in your app to organize information by a specific feature or task. The most common way to use a tab bar is with a tab bar controller, which holds a property of each view controller that represents each scene you want presented in the tab bar. When the user taps an item, a new view related to the new task is displayed.
  - Tab bars are frequently used in apps that present multiple workflows or courses of action. For example, the App Store app has separate tabs to browse featured apps, search for a specific app, or check for available updates.
  - Configuration
    - Because you’ll most often use the tab bar in conjunction with a tab bar controller, you’ll add scenes to be displayed to the controller. The view controller for each scene has a UITabBarItem property that defines the text and optional image that will be displayed by the tab bar. To add a scene to a tab bar controller, and the tab bar view, you link it to the tab bar controller's viewControllers property in a storyboard.
  - [UITabBar Developer Documentation](https://developer.apple.com/documentation/uikit/uitabbar)

#### Controls

- In the previous section, you learned about common views that display information to the user. What about responding to user input? You'll use tools in UIKit, known as controls, to tell the app what to do.
- Think of a control as a communication tool between the user and the app. When the user interacts with a control, the control triggers a control event. Different controls trigger different control events.
- After setting up a control in Interface Builder, you set up an @IBAction that responds to a specific control event and allows you to execute a block of code. Most often you will use the Primary Action Triggered (UIControl.Event.primaryActionTriggered) control event. This control event is triggered when a button is tapped or when the value of a control changes.
- Controls are simple, straightforward, and familiar to users because they appear throughout most iOS apps. As you learn about some of the different subclasses of UIControl, on the following pages, think about your favorite apps and how you use controls to interact with to them.
- **Buttons (UIButton)**
  - Users of iOS devices can initiate a control event with the tap of a button. When you set up a button, you give it a title or an image that conveys what the button will do when tapped. The appearance of the button changes with different states of being tapped: tapping down and lifting up.
  - The primary control event is triggered when the user releases a button after tapping it. Buttons can also execute code at different stages of a tap, such as when the user first touches the button, holds down the button, or cancels the tap by dragging their finger outside of the frame of the button before lifting their finger.
  - [UIButton Developer Documentation](https://developer.apple.com/documentation/uikit/uibutton)
- **Segmented Controls (UISegmentedControl)**
  - A segmented control is a horizontal set of multiple segments. Each segment functions as a discrete button, allowing the user to choose from a limited, compact set of options. This example, from Maps, allows the user to change the display mode, with three choices: Map, Transit, or Satellite.
  - Segmented controls execute code when the control’s value changes. The value represents which segment of the control is selected.
  - [UISegmentedControl Developer Documentation](https://developer.apple.com/documentation/uikit/uisegmentedcontrol)
- **Text Fields (UITextField)**

  - Text fields allow the user to input a single line of text into an app. You’ll use them to gather a small amount of text and to perform some action based on that text.
  - Configuration

    - <img src="./resources/configuration_textfield.png" alt="Text Field" width="300" />

      - Text: Text that's displayed by the text field
      - Placeholder Text: Text that's displayed when the text field is empty
      - Capitalization: Setting that controls how the keyboard deals with capitalization
      - Correction: Setting that enables or disables autocorrect
      - Keyboard Type: Setting that controls which keyboard is displayed, for example: email, web, or default
      - Auto-Enable Return Key: Return key disabled until text is entered
      - Secure: Specify that the text field shouldn't display its contents; commonly used for passwords

  - Text fields execute code when the user presses the ‘Return’ or ‘Done’ key on the keyboard, or when the user edits the text.
  - [UITextField Developer Documentation](https://developer.apple.com/documentation/uikit/uitextfield)

- **Sliders (UISlider)**

  - Sliders allow users to make smooth and gradual adjustments to a value—useful for controls that modify things like speaker volume, screen brightness, or color values. The user controls a slider by moving from a starting value along a continuous range between minimum and maximum values.
  - Configuration

    - <img src="./resources/configuration_slider.png" alt="Sliders" width="300" />

      - Value: Starting number value the slider will represent
      - Minimum: Lowest number value the slider may represent
      - Maximum: Highest number value the slider may represent
      - Min Image: Optional image on the minimum end of the slider
      - Max Image: Optional image on the maximum end of the slider

  - Sliders execute code as the user changes the value of the slider.
  - [UISlider Developer Documentation](https://developer.apple.com/documentation/uikit/uislider)

- **Switches (UISwitch)**

  - A switch lets the user turn an option on or off. You’ve probably noticed — and used — switches throughout the Settings app.
  - Configuration

    - <img src="./resources/configuration_switches.png" alt="Switches" width="300" />

      - State: A Boolean value that determines the on/off state of the switch

  - Switches execute code as the user toggles the control.
  - [UISwitch Developer Documentation](https://developer.apple.com/documentation/uikit/uiswitch)

- **Date Pickers (UIDatePicker)**

  - Date pickers provide a straightforward interface for managing date and time selection, allowing users to specify a particular date quickly and efficiently.
  - Configuration

    - <img src="./resources/configuration_datepickers.png" alt="Date Pickers" width="300" />

      - Mode: Setting that controls whether the picker should choose a date, or a date and time
      - Locale: Information for how the date should be displayed, varies by language or culture, defaults to the device's current locale
      - Interval: Controls granularity of the picker segments, for example, whether there should be an option for each minute, or every five minutes, fifteen minutes, etc.
      - Date: The starting date when the picker is first displayed
      - Minimum Date: The earliest the date picker allows the user to choose
      - Maximum Date: The latest the date picker allows the user to choose

  - Date pickers execute code whenever the value of the selected date or time is changed.
  - [UIDatePicker Developer Documentation](https://developer.apple.com/documentation/uikit/uidatepicker)

#### View Controllers

- UIKit defines a special class that controls a view, sets up child views, controls what they display, and responds to user interaction. This class is called the UIViewController.
- Most commonly, each screen in an app is represented by a scene in a storyboard, and each scene in a storyboard is associated with a subclass of UIViewController. The associated UIViewController subclass is defined in a .swift file that holds all of the logic that controls the scene. Each UIViewController class has a view property that represents the parent view of the scene.
- Think back to the Light project you built in the first unit. The project has a single storyboard with a single scene. That scene was linked to a UIViewController subclass called ViewController. The light was toggled by adjusting the view property of ViewController. That view property is the same instance of UIView as the parent view of the scene in the storyboard.
- When you added a button to the screen, the button became a child view of the scene’s main view. When you wired up actions and outlets, you linked them to the ViewController file, which defined the view controller for that scene.
- You’ll learn how to make complex view controllers in later lessons. But for now, it’s enough to understand that each different type of screen you see in an app is managed by a different type of view controller.

#### Where to Learn More

- You’ve just learned about the most common views and controls in UIKit. But where would you go to find out more about these and other UIKit tools? As you learned earlier, Apple has large teams dedicated to writing documentation to help developers like you learn more about the system tools for building apps.
- Most of the information for this section is from a set of guidelines called the [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/designing-for-ios), which was written and maintained by one of those teams. When you want to learn more about UIKit, you can go to developer.apple.com and search for more information about the topics in this lesson.
