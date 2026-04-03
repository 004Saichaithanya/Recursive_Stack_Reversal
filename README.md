Recursive Stack Reversal Simulation
Overview
This project is a web-based simulation designed to visualize the process of recursively reversing a stack. It provides an interactive way to understand how recursion works by showing the main stack's state and the call stack frames as the reversal algorithm executes.

Features
Main Stack Visualization: See the elements of the primary stack as they are manipulated.
Call Stack Visualization: Observe the creation and destruction of call stack frames, including their local variables, during the recursive calls.
Step-by-Step Logging: A dedicated log window provides textual updates on the simulation's progress and actions.
Interactive Controls: (Implied from simulationRunning, resolveNextStep variables) The simulation likely includes controls to start, pause, and step through the execution.
How to Use
To run this simulation, simply open the index.html file in any modern web browser. No server or additional setup is required.

Project Structure
The entire application is contained within a single index.html file, which includes all the HTML, CSS, and JavaScript necessary for the simulation.

.
└── index.html
Technical Details
The simulation is built using standard web technologies:

HTML5: Provides the structure and layout of the application.
CSS3: Styles the application, creating a clean and intuitive user interface.
JavaScript: Implements the recursive stack reversal logic and handles the dynamic updates to the UI.
Key JavaScript Variables and DOM Elements:
The core logic revolves around these JavaScript variables and their corresponding DOM elements:

// Source: index.html
let mainStack = [];
let callStackFrames = [];
let resolveNextStep = null;
let simulationRunning = false;
let frameCounter = 0;

// --- UI Updaters ---
const mainStackDom = document.getElementById('mainStackDom');
const callStackDom = document.getElementById('callStackDom');
const logWindow = document.getElementById('logWindow');
Styling Highlights:
The application uses a dark theme with distinct visual cues for different parts of the simulation.

Root CSS Variables: Define a consistent color scheme for the entire application.

/* Source: index.html */
:root {
    --bg-color: #0d1117;
    --text-color: #c9d1d9;
    --border-color: #30363d;
    --btn-bg: #238636;
    --btn-hover: #2ea043;
    --stack-bg: #21262d;
    --frame-reverse: #1f6feb;
}
Panel Styling: Main sections of the UI (e.g., main stack, call stack, log window) are styled as distinct panels.

/* Source: index.html */
.panel {
    flex: 1;
    background-color: #161b22;
    border: 1px solid var(--border-color);
    border-radius: 8px;
    padding: 20px;
    display: flex;
    flex-direction: column;
    overflow-y: auto;
}
Call Stack Frame Styling: Different states or types of recursive calls are visually distinguished. For instance, frames related to the "reverse" operation have a specific background and border.

/* Source: index.html */
.frame.reverse { background-color: rgba(31, 111, 235, 0.2); border-left: 4px solid var(--frame-reverse); }
.frame.insert { background-color: rgba(35, 134, 54, 0.2); border-left: 4px solid var(--frame-insert); }
.frame-header { font-weight: bold; margin-bottom: 5px; font-family: monospace; font-size: 15px;}
.frame-vars { color: #a5d6ff; font-family: monospace; }
