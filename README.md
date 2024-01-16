# TwinCAT XTS Framework

## Contents

1. [Background](#Background})
2. [Project Description](#Description)
3. [System Design](#System-Design)
4. [Tests](#Tests)
5. [Support](#Support)
6. [Requirements](#Requirements)
7. [Documents](#Document-List)

## Background

This project is an attempt to use good programming practice to create a standard project to run a Beckhoff XTS unit, there is currently not a standard implementation for XTS so developers are able to design and implement their own system, however this leads to a lot of duplication of effort. Hopefully this will remove some of that process, even if only providing a basis for others to copy. Also its a good bit of fun :-)

## Description

The system has classes for XTS hardware and management, a mover class is implemented for each physical mover and each has a sequence controller. PackML is used as a global state machine, with each class running local state machines based on this. This allows the system to fit seemlessly in a standard packaging environment. Operations of classes are implemented as wrapped classes implementing a Task interface.

## System Design

The MAIN program instances a class Machine, this contains the Xts Manager and Hardware classes. it also instances an array of a mover type, these get a movement class that can be editted depending on operation requirements.

## Tests

Tests will be performed using a testing framework **[Tc3_UnitTest](https://github.com/PeterZerlauth/Tc3_UnitTest)** by Peter Zerlauth. Being Honest testing was not done at the start, but at least Unit Tests will be rolled out to the older components. Refactoring components will allow TDD to be used on some elements. To keep it clean any additions must now have a test.

## Support

code was developed/modified by:

1. Chris Knight

## Requirements: 

TwinCAT 3 4024.7   
XTS Extension TF5850 3.21.703.0  
Advanced Motion TF5410 3.1.10.44

## Document List

Documentation for the repo starts **[here](./Documentation.md)**









