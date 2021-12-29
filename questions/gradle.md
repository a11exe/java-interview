# Gradle Interview Questions

+ [Advantages of using Gradle.](#advantages-of-using-gradle)
+ [What is Gradle wrapper?](#what-is-gradle-wrapper)
+ [What is the Gradle build script file name?](#what-is-the-gradle-build-script-file-name)
+ [What are the core components of Gradle build script?](#what-are-the-core-components-of-gradle-build-script)
+ [How do I force Gradle to download dependencies always?](#how-do-i-force-gradle-to-download-dependencies-always)
+ [What is Gradle build language?](#what-is-gradle-build-language)


## Advantages of using Gradle.

Gradle provides support for multi-project builds.
It allows to use existing Maven/Ivy repositories.

## What is Gradle wrapper?

A wrapper is a batch script and it is one of the ways to perform Gradle build. 
When executed the first time, it automatically downloads Gradle and then initiate the build.

It helps to setup Gradle workspace quickly for first-time users (Zero installation) 
and also ensure all the developers use the same version of Gradle.

## What is the Gradle build script file name?

build.gradle.

## What are the core components of Gradle build script?

Project and task are the core compoents. Groovy organizes projects as a list of tasks.

To view the list of available projects, use the command gradle projects, for the tasks list the command is gradle tasks.

## How do I force Gradle to download dependencies always?

you may refresh dependencies in your cache using the command line option --refresh-dependencies. 
Also deleting the cached files under ~/.gradle/caches would get the next Gradle build to download them again.

## What is Gradle build language?

Gradle provides a domain specific language (DSL) for describing builds. 
This build language is available in Groovy and Kotlin.
It is build.gradle. Kotlin DSL script files use the .gradle.kts file name extension.