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
