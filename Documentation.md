# TwinCAT XTS Framework Documentation

## Contents

1. [Framework Structure](#framework-structure)
2. [XTS Class](#xts-class)
3. [Mover Class](#mover-class)

## Framework Structure

The framework contains a number of elements that allow the user to implement an XTS system. It contains several other elements that implement core features of its operation, event messaging and PackML state machine functionality. These features will eventually need to be removed leaving the core XTS elements in this library. As a result refactoring going forward will be made to pull references to these as libraries inverting the dependanices. 

## XTS Class

The XTS class is the handler class for the hardware and collision group elements of the XTS. The XTS Class holds the Xts hardware class, which is responsible for managing the hardware elements of the XTS via the Xts Environment Variable. These include the Track class and the Part class, which are able to provide status information and diagnostics information of all the elements of the system. These class combine to provide all control and informaiton on the track hardware.

## Mover Class

The movers are provided by a Mover Class, this class takes a sequence class that controls its movement. The Mover Class contains all the motion operations of the system, the XTS class is repsonsible for all detection features assigning to collision avoidance groups. The Movers handle the motion functions and error handling. 

## Mover Sequence Class

The movers only hold the functionality of the mover itself and the XTS calss the track. There are options for how you control the motion in an XTS system, Station centric and Mover centric. In the station centric model the XTS system is given a set of station, these stations control the mover, as the mover arrives it joins a virtual queue on the station, when the station is complete the mover moves on. 

In a mover centric model the motion is controlled by a mover sequence, you create a motion profile and give it to each mover, the mover then holds the location information and required destination. You can provide station class as an array, a simple indexing sequence would then simply iterate through the array. 
