# LCR Circuit Simulation

A simple simulation of an LCR (Inductor-Capacitor-Resistor) circuit using [insert language/platform here — e.g., Python with matplotlib, MATLAB, C++, etc.]. This project models and visualizes the time-domain behavior of a series LCR circuit based on differential equations derived from Kirchhoff's Voltage Law (KVL).

## 📘 Features

- Models a **series LCR circuit** using second-order differential equations
- Simulates **underdamped**, **critically damped**, and **overdamped** cases
- Plots voltage and/or current over time
- Allows custom input for component values (L, C, R)
- Interactive or command-line configuration

## 🧪 Theory

The governing differential equation for a series LCR circuit:
```

L \* (d²q/dt²) + R \* (dq/dt) + (1/C) \* q = V(t)

````

Where:
- `L` is inductance in Henrys (H)
- `C` is capacitance in Farads (F)
- `R` is resistance in Ohms (Ω)
- `q(t)` is the charge on the capacitor
- `V(t)` is the applied voltage (can be a constant or function)

The system is numerically solved using ODE solvers.

## 🚀 Getting Started

### Prerequisites

- [Python 3.x](https://www.python.org/downloads/) (if applicable)
- `matplotlib`, `numpy`, `scipy` (for numerical simulation and plotting)

Install dependencies:

```bash
pip install -r requirements.txt
````

### Running the Simulation

```bash
python lcr_simulation.py
```

You will be prompted to input:

* Resistance (R)
* Inductance (L)
* Capacitance (C)
* Type of input voltage (DC, sinusoidal, step, etc.)
* Duration and time step of the simulation

### Example

```bash
Enter Resistance (Ohms): 50
Enter Inductance (Henrys): 0.1
Enter Capacitance (Farads): 0.001
Input type: DC
```

The script will plot the resulting current/voltage waveforms and save the output.

## 📂 Project Structure

```
lcr-circuit-simulation/
│
├── lcr_simulation.py         # Main simulation script
├── utils.py                  # Helper functions (optional)
├── README.md                 # This file
├── requirements.txt          # Python dependencies
└── output/                   # Generated plots and data (optional)
```

## 📊 Output

Plots of:

* Current vs Time
* Voltage across components vs Time
* Phase plots (optional)

All outputs can be saved as PNG/PDF/CSV based on user input.

## ✅ TODO

* [ ] Add support for parallel LCR configuration
* [ ] Add GUI (Tkinter/Streamlit)
* [ ] Export data as CSV
* [ ] Add support for frequency domain analysis

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.

## 📄 License

[MIT](LICENSE)

## 💡 Acknowledgements

* Based on fundamental circuit theory from textbooks
* Numerical solving using SciPy's `odeint`
