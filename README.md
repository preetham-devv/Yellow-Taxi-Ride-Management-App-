# Yellow Taxi Ride Management App

This project implements a ride management system for a fictional taxi service, **gatorTaxi**, using a combination of a **Min-Heap** and a **Red-Black Tree** to efficiently manage ride requests.

## 📌 Problem Statement

Efficiently manage ride requests using:
- **Red-Black Tree** for fast search, insert, delete, and range queries.
- **Min-Heap** for quick access to the ride with the lowest cost (with tie-breaker on trip duration).

Each ride is represented as a triplet:


---

## 🧱 Data Structures

### 1. Min-Heap

Used to retrieve the ride with the **lowest cost**, breaking ties using **tripDuration**.

| Operation       | Time Complexity |
|----------------|------------------|
| Insert         | O(log n)         |
| Get Minimum    | O(1)             |
| Delete (any)   | O(log n)         |

### 2. Red-Black Tree

Self-balancing binary search tree to store and manage rides by `rideNumber`.

| Operation       | Time Complexity |
|----------------|------------------|
| Insert         | O(log n)         |
| Delete         | O(log n)         |
| Search         | O(log n)         |
| Range Query    | O(log n + S)     |

`S` = number of rides in the queried range.

Both structures are synchronized through a wrapper class (`HeapRBT`) that ensures integrity between the two.

---

## ⚙️ Key Functionalities

| Function                        | Description                                                                 | Time Complexity |
|---------------------------------|-----------------------------------------------------------------------------|------------------|
| `Print(rideNumber)`            | Prints details of a specific ride.                                          | O(log n)         |
| `Print(rideNumber1, rideNumber2)` | Prints all rides within the given ride number range.                     | O(log n + S)     |
| `Insert(rideNumber, rideCost, tripDuration)` | Adds a new ride.                                             | O(log n)         |
| `GetNextRide()`                | Retrieves and removes the ride with the lowest cost and trip duration.     | O(log n)         |
| `CancelRide(rideNumber)`       | Deletes a ride from both Min-Heap and Red-Black Tree.                      | O(log n)         |
| `UpdateTrip(rideNumber, new_tripDuration)` | Updates the duration and possibly cost of an existing ride.   | O(log n)         |

---

## 🛠️ Implementation Details

- The application reads commands from an input text file.
- Uses a custom `rideNode` structure to represent each ride.
  - Contains ride details, heap index, and color for RBT.
- A switch/case structure is used to call the corresponding function per input line.
- The program maintains synchronization between the Min-Heap and Red-Black Tree via cross-referencing.

---

## 📂 Example Input Format


---

## ✅ Project Highlights

- Achieves required time complexities for all core operations.
- Effectively combines Min-Heap and Red-Black Tree to balance performance and functionality.
- Modular, maintainable, and efficient.

---

## 📎 How to Run

1. Compile the source code (e.g., using `javac` or your preferred compiler).
2. Provide the input commands in a text file.
3. Run the program to process the commands and observe the output.

---

## 📧 Contact

For questions or collaboration:
- Author: Preetham
- Email: prreetham.20@gmail.com

---

