
# 🅿️ Parking Management System

A simple and practical Command-Line Interface (CLI) application for managing vehicle entry, exit, and searching in a parking lot, built with Python.

## 📋 Table of Contents

- [Features](#-features)
- [Architecture](#️-architecture)
- [Technologies Used](#️-technologies-used)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Main Functions](#-main-functions)
- [Testing](#-testing)
- [Contributing](#-contributing)
- [License](#-license)

---

## ✨ Features

### Core Functionalities

- 🚗 **Register Vehicle Entry:** Collects vehicle information (name, color, plate, and entry time) and adds it to the parking list.
- 🚫 **Duplicate Prevention:** Checks license plates to prevent registering the same vehicle twice.
- 📋 **View Parking List:** Displays all vehicles currently in the parking lot along with their details.
- 🔍 **Search by Plate:** Finds vehicle information using its license plate number.
- 🚪 **Exit Program:** Safely closes the application.

### User Interface

- 💻 **Command-Line Interface (CLI):** Provides a simple and readable text-based menu.
- ⚠️ **Error Handling:** Displays appropriate messages for duplicate plates, vehicles not found, and invalid options.

---

## 🏗️ Architecture

This project follows the **Separation of Concerns** principle to keep the code organized, readable, and maintainable.

```text
┌─────────────────────┐
│      main.py        │
│   User Interface    │
└──────────┬──────────┘
           │
           ↓
┌─────────────────────┐
│  parking_module.py  │
│   Business Logic    │
└──────────┬──────────┘
           │
           ↓
┌─────────────────────┐
│      Data List      │
│   Storage Layer     │
└─────────────────────┘
```

### Architecture Layers

- **User Interface Layer:** Handles the menu and user interactions.
- **Business Logic Layer:** Processes vehicle information and performs operations.
- **Storage Layer:** Stores vehicle information in an in-memory Python list.

---

## 🛠️ Technologies Used

- **Language:** Python 3.x
- **Libraries:** Only built-in Python modules are used. No external packages are required.
- **Testing:** Python's built-in `unittest` module.

---

## 📦 Installation

### Prerequisites

- Python 3.7 or higher
- Git

### Setup Steps

**1. Clone the repository:**

```bash
git clone https://github.com/Nazanin-Montazeri/ParkingAppPython.git
```

**2. Navigate to the project directory:**

```bash
cd ParkingAppPython
```

**3. Run the application:**

```bash
python main.py
```

No external dependencies are required.

---

## 🚀 Usage

After running the application, the main menu will appear:

```text
1) Enter to parking
2) Parking list
3) Search car by plate
0) Exit

Enter an option:
```

### Main Operations

- **Option 1 (Register Vehicle):** Collects the vehicle's name, color, plate number, and entry time. It also checks for duplicate license plates.
- **Option 2 (Parking List):** Displays all registered vehicles and their information.
- **Option 3 (Search):** Finds and displays vehicle information based on the entered plate number.
- **Option 0 (Exit):** Closes the application.

---

## 📁 Project Structure

```text
ParkingAppPython/
│
├── main.py               # Main entry point (menu and while loop)
├── parking_module.py     # Business logic functions
├── parking_test.py       # Unit tests
│
└── README.md             # Project documentation
```

---

## 📚 Main Functions

### parking_module.py

This file contains the main business logic of the application:

- **parking_list:** A global list that stores vehicle information as dictionaries.
- **show_menu():** Displays the main menu and gets the user's choice.
- **get_car_info():** Collects vehicle information and returns it as a dictionary.
- **print_parking_list(parking_list):** Displays vehicle information with formatted output using f-strings.
- **find_car_by_plate(parking_list, plate):** Searches for a vehicle by its license plate number.

---

## 🧪 Testing

The project uses Python's built-in `unittest` module for testing.

To run the tests, execute:

```bash
python parking_test.py
```

---

## 👥 Contributing

Contributions and suggestions for improving this project are welcome.

If you would like to contribute:

1. Fork the repository.
2. Create a new branch:

```bash
git checkout -b feature/AmazingFeature
```

3. Commit your changes:

```bash
git commit -m "Add some AmazingFeature"
```

4. Push your branch:

```bash
git push origin feature/AmazingFeature
```

5. Open a Pull Request.

### Code Style

- Follow the PEP 8 style guide.
- Use descriptive and readable names for variables and functions.
- Keep the code clean and organized.

---

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more information.

---

**Made with ❤️ by Nazanin Montazeri**
