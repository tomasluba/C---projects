# C---projects
# Digit Recognition in Pure C

This project implements a simple digit recognition system written entirely in C, without using any external machine learning libraries.

The program works with 28x28 grayscale images (784 values) and supports multiple execution scenarios for testing, debugging, and evaluation.

---

## 📂 Project Structure

.
├── include/            # Header files  
├── src/                # Source files (z2.c, functions.c, data.c)  
├── test_cases/         # stdin / stdout test scenarios  
│   ├── stdin/  
│   └── stdout/  
├── CMakeLists.txt  
├── test.sh             # Automated testing script  

---

## ⚙️ Compilation

### Using GCC

    gcc -Iinclude src/z2.c src/functions.c src/data.c -lm -o program

### Using CMake

    mkdir build
    cd build
    cmake ..
    cmake --build .

---

## ▶️ Running the Program

The program expects input from standard input (stdin).

Example:

    ./program < test_cases/stdin/scenario1.txt

---

## 🧪 Supported Scenarios

The program supports 7 different execution scenarios:

Scenario 1  
Prints the input image (28x28) as ASCII visualization.

Scenario 2  
Prints a specific weight value from the trained model.

Scenario 3  
Computes raw scores (logits) for digits 0–9 based on input image.

Scenario 4  
Applies softmax function to 10 input values.

Scenario 5  
Finds the index of the maximum value (argmax).

Scenario 6  
Performs digit recognition for a single image.

Scenario 7  
Evaluates multiple images and computes prediction accuracy.

---

## 🤖 Automated Testing

All prepared test cases can be executed automatically:

    ./test.sh

The script will:
- Compile the program
- Run all test cases from test_cases/stdin
- Compare outputs with expected results in test_cases/stdout
- Display pass/fail summary

---

## 🧠 Technical Highlights

- Pure C implementation
- Manual memory handling
- Matrix-style linear computation
- Softmax implementation
- Argmax logic
- Batch evaluation with accuracy calculation
- Automated stdin/stdout testing

---
