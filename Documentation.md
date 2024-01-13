# TwinCAT XTS Framework Documentation

## Contents

1. [Framework Structure](#framework-structure)
2. [XTS Class](#xts-class)

## Framework Structure

The framework contains a number of elements that allow the user to implement an XTS system. It contains several other elements that implement core features of its operation, event messaging and PackML state machine functionality. These features will eventually need to be removed leaving the core XTS elements in this library. As a result refactoring going forward will be made to pull references to these as libraries inverting the dependanices. 

## XTS Class

The XTS class is the handler class for the hardware and collision group elements of the XTS. The XTS Class holds the Xts hardware class, which is responsible for managing the hardware elements of the XTS via the Xts Environment Variable. These include the Track class and the Part class, which are able to provide status information and diagnostics information of all the elements of the system. These class combine to provide all control and informaiton on the track hardware.