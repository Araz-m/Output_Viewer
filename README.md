# OpenFast_Output_Viewer

# Real-Time/None Real-time Data Plotter for Wind Turbine Simulation with OpenFast

This Python script reads simulation data from the `.out` file from OpenFast and dynamically plots various wind turbine parameters in real-time and non real time.

## 📌 Features
- **Real-time animation** of selected parameters
- **Customizable** plotting groups
- **Automatic file loading** (waits for file to be available)
- **Scalable** - Easily extend with new plot groups

---

## 🚀 Installation & Setup
### 1️⃣ Install Dependencies
Make sure you have **Python 3.10+** installed. Then, install the required libraries:

```bash
pip install pandas matplotlib numpy
```

---
## ⚙️ Usage
###Configuring Plots
You can define different plot groups in the script by modifying:

```bash
plot_groups_1 = {
    "Optimus 20MW-295": (["Wind1VelX", "BldPitch1", "RotSpeed", "RotTorq", "RotPwr", "GenPwr"], 
                [1, 1, 1, 0.001, 0.001, 0.001]),
    "Tip Clearance": (["Tip2Twr1", "Tip2Twr2", "Tip2Twr3"], 
                [0.001, 0.001, 0.001, 0.001])
}
#==============================================================================
# plot_groups_2 = {
#     "Loads on blade Root_I": (["RootFxb1", "RootFyb1", "RootFzb1", "RootMEdg1", "RootMFlp1", "RootMzb1"], 
#                 [0.001, 0.001, 0.001, 0.001, 0.001, 0.001]),
#     "Loads on blade Root_II": (["RootFxc1", "RootFyc1", "RootFzc1", "RootMzc1", "RootMzc2", "RootMzc3"], 
#                 [0.001, 0.001, 0.001, 0.001, 0.001, 0.001])
# }



#==============================================================================
#uncomment plot_groups_3 if you need to plot more groups
# if you did remember to add , plot_groups_3 in the plot_multiple_groups function at the end
#==============================================================================
# plot_groups_3 = {
#     "Loads on Tower Top_I": (["YawBrFxp", "YawBrFyp", "YawBrFzp"], 
#                 [0.001, 0.001, 0.001]),
#     "Loads on Tower Top_II": (["YawBrMxp", "YawBrMyp", "YawBrMzp"], 
#                 [0.001, 0.001, 0.001])
# }
#==============================================================================
```


you have to add the exact column name from your .out file and also you have to choose the scale that you need for the respected data in the list.

if you are running real time simulation make sure that 
```bash
real_time=True
```
Run the OpenFast_Output_Viewer Script (I used VSCode Terminal)

## 📸 Sample Output
https://github.com/Araz-m/OpenFast_Output_Viewer/blob/main/Figure_1_Example.png

