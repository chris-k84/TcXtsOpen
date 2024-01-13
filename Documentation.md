# TwinCAT XTS Framework Documentation

## Contents

1. [Framework Structure](#framework-structure)

## Framework Structure

The framework contains a number of elements that allow the user to implement an XTS system. It contains several other elements that implement core features of its operation, event messaging and PackML state machine functionality. These features will eventually need to be removed leaving the core XTS elements in this library. As a result refactoring going forward will be made to pull references to these as libraries inverting the dependanices. 