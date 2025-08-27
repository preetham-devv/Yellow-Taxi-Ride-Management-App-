# Yellow-Taxi-Ride-Management-App-
Yellow Taxi Ride Management App
This project implements a ride management system for a taxi service, named gatorTaxi, using a combination of a Red-Black Tree and a Min-Heap data structure to efficiently handle ride requests and assignments. The software is designed to manage ride requests based on their ride number, cost, and trip duration.

Problem Statement
The core goal is to efficiently manage all ride requests for gatorTaxi. This requires the use of a Red-Black Tree for searching and a Min-Heap for prioritizing rides. The system must handle a variety of functions, including insertion, deletion, and updates, while maintaining optimal time complexities.

A ride is defined by the triplet: (rideNumber, rideCost, tripDuration).

Data Structures
The application relies on two primary data structures:

Min-Heap
A min-heap is used to quickly retrieve the next available ride based on the lowest ride cost. If two rides have the same cost, the one with the lowest trip duration is selected.

Insert: O(
logn)

Get Minimum (GetNextRide): O(1)

Delete (arbitrary): O(
logn)

Red-Black Tree
A self-balancing binary search tree that stores ride information. It is used for efficient searching, printing a range of rides, and deleting specific rides.

Insert: O(
logn)

Delete: O(
logn)

Search: O(
logn)

These two data structures are interlinked within a HeapRBT class to ensure efficient operation. The Red-Black Tree holds a reference to the Min-Heap index, allowing for quick lookups and deletions.

Key Functions
The application is built around the following functionalities, with their corresponding time complexities:

Function

Description

Time Complexity

Print(rideNumber)

Prints the triplet for a specific ride.

O(
logn)

Print(rideNumber1, rideNumber2)

Prints all rides within a specified range.

O(
logn+S), where S is the number of rides in the range.

Insert(rideNumber, rideCost, tripDuration)

Adds a new ride request.

O(
logn)

GetNextRide()

Retrieves and removes the ride with the lowest cost and trip duration.

O(
logn)

CancelRide(rideNumber)

Deletes a ride from both data structures.

O(
logn)

UpdateTrip(rideNumber, new_tripDuration)

Modifies a ride's duration, potentially with a penalty to the ride cost.

O(
logn)

Implementation Details
The application is designed to process commands from an input text file. It uses a rideNode structure to store each ride's information, including its heap index and color for the Red-Black Tree. A switch statement is used to call the appropriate function based on the input string.

The project successfully meets all requirements and achieves the necessary time complexities for each operation.
