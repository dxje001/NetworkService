# Simulator of Infrastructure System  

## Project Overview  
This project implements a **WPF MVVM application** named **NetworkService** for monitoring measured values across entities in a system. Measurements are provided by an external application, **MeteringSimulator**, which sends data to the NetworkService at random intervals. The application is designed for **CG4 target users** who require precise and clear numerical data, graphs, and undo functionalities for error prevention.

---

## Features  

### Key Functionalities  
1. **Data Logging**  
   - Logs received measurement values with timestamps and associated entity IDs into a `.txt` log file.

2. **Network Entities View**  
   - Add, remove, and list entities in a table with their properties.
   - Apply filtering and search functionalities based on:
     - Entity type.
     - Numeric comparisons (`<`, `>`, `=`).
     - Latest measured value's validity within expected ranges.
   - Undo all actions with a detailed history view.

3. **Network Display View**  
   - Drag & drop visualization of entities on a grid.
   - Display entities' properties (ID, latest measurement) alongside their icons.
   - Highlight entities when measurements are outside valid ranges.
   - Link entities visually and ensure connections update dynamically during movement.
   - Save grid state and maintain view consistency during navigation.

4. **Measurement Graph View**  
   - Real-time graph updates for the last five received values of a selected entity.
   - Visualization of invalid measurements (e.g., out-of-range values) with distinct colors.
   - Additional pie chart representation of entity type distribution.

5. **Entity Management**  
   - Entities modeled as **roads** with attributes:  
     - `ID` (unique integer).  
     - `Name`.  
     - `Type` (IA or IB with different measurement thresholds).  
   - Entities' types are predefined and selected via ComboBox during creation.

---

## Technologies  
- **.NET Framework**  
- **WPF (Windows Presentation Foundation)**  
- **MVVM Design Pattern**  
- **C# Programming Language**  
- **DataBinding and Validation**  

---

## System Components  

### 1. **NetworkService Application**  
   - **Frontend**:  
     - Graphical User Interface (GUI) designed for user interaction with tables, graphs, and drag & drop elements.  
     - Data filtering, visualization, and undo capabilities.

   - **Backend**:  
     - Processes real-time data streams from the **MeteringSimulator**.  
     - Implements logic for managing entities and their relationships.

### 2. **MeteringSimulator**  
   - Simulates measurement data streams.  
   - Communicates with **NetworkService** to provide real-time updates.

### 3. **Logging System**  
   - Writes all received data into a log file for persistence and reference.

### 4. **Graphical Visualization**  
   - Displays entity measurement history as graphs (circle graph for values over time).  
   - Pie chart for entity type distribution.

---

## Additional Notes  
- **User Experience Enhancements**:  
  - Shortcut keys for navigation and common actions.  
  - Tooltips and cursor feedback for interaction clarity.  

- **Design Consistency**:  
  - Uniform color palettes, fonts, and icons across the UI.  
  - Validation with clear, field-specific error messages.  

- **Error Prevention**:  
  - Confirmations for critical actions (e.g., deletions).  
  - Notifications for successful operations.

---

## Inspiration  
This project draws inspiration from **SCADA software** systems commonly used for monitoring and controlling infrastructure networks.

---

### Wireframe  
A low-fidelity prototype of the solution is required for review and iteration.
