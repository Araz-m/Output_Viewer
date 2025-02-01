# OpenFast_Output_Viewer

# Real-Time/None Real-time Data Plotter for Wind Turbine Simulation with OpenFast

This Python script reads simulation data from a `.out` file from OpenFast and dynamically plots various wind turbine parameters in real-time and non real time.

## 📌 Features
- **Real-time animation** of selected parameters
- **Customizable** plotting groups
- **Automatic file loading** (waits for file to be available)
- **Scalable** - Easily extend with new plot groups

---

## 🚀 Installation & Setup
### 1️⃣ Install Dependencies
Make sure you have **Python 3.7+** installed. Then, install the required libraries:

```bash
pip install pandas matplotlib numpy
```

---
## ⚙️ Usage
Configuring Plots
You can define different plot groups in the script by modifying:
plot_groups_1 = {
    "Optimus 20MW-295": (["Wind1VelX", "BldPitch1", "RotSpeed", "RotTorq", "RotPwr", "PtfmTDxt"], 
                [1, 1, 1, 0.001, 0.001, 0.001]),
    "Tip Clearance": (["Tip2Twr1", "Tip2Twr2", "Tip2Twr3"], 
                [0.001, 0.001, 0.001, 0.001])
}
you have to add the exact column name from your .out file and also you have to choose the scale that you need for the respected data in the list.

if you are real time simulation make sure that real_time=True 
Run the Real-Time Plotting Script (I recommend VSCode Terminal)

📸 Sample Output


