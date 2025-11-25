Online Compiler (UI)
A simple static frontend for an online code compiler — built with HTML and CSS. This repository contains the UI (pages and styles) for an online-compiler project. It is intended to be used as the client-side interface; a backend service is required to safely compile and run code.

Features
Clean, responsive HTML/CSS interface
Code editor layout and input/output areas (UI only)
Ready to plug into a compilation/execution API
Lightweight and easy to customize
Demo / Preview
To preview locally:

Open index.html in a browser
Or use a local dev server (e.g., VS Code Live Server or python3 -m http.server)
Installation / Run Locally
Clone the repository git clone https://github.com/shivranjan0/online-compiler_project.git
Open the project folder and open index.html in your browser, or run a static server:
python3 -m http.server 8000
or use Live Server in VS Code
How to connect a backend
This repo contains only frontend assets (HTML/CSS). To actually compile and run code, integrate a secure backend service that:

Accepts source code, language selection, stdin, and compilation flags
Runs the code in a sandboxed environment (e.g., Docker, firejail, gVisor, or a managed execution service)
Returns stdout/stderr and exit code to the UI Be careful to implement strict sandboxing and resource limits to avoid security risks.
Suggested file structure
index.html — main UI
css/ or styles.css — stylesheet(s)
assets/ — images/fonts (if any)
README.md — this file
Adjust names above if your repo uses different paths.

Contributing
Contributions are welcome. Typical workflow:

Fork the repo
Create a branch: git checkout -b feature/your-feature
Make changes and commit
Open a pull request with a description of your changes
If you plan to add a backend, please include instructions and any environment variables in the new README section.

Roadmap / Ideas
Add a proper code editor (Monaco, CodeMirror)
Add language selection and theme support
Add example templates for C/C++, Python, JavaScript
Implement a secure backend API for compilation and execution
Add tests and CI for linting / accessibility checks
