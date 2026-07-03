# tempdoc
# Promt 1 
Role: You are an expert Principal Frontend Architect.
Context: I need to write a comprehensive README.md for a React micro-frontend (microview) application. This application uses Webpack/Vite Module Federation.
Project Configuration:
[Paste your Module Federation plugin config here]
Directory Structure:
[Paste your directory tree here]
Task: Generate a README.md that includes:

Project Overview: What this microview does based on the file names.

Module Federation Architecture: Clearly document its role (Host or Remote), what it exposes to the network, and what remotes it consumes.

Local Development Setup: Steps to run it locally, highlighting any specific environment variables or port dependencies required by Module Federation.

#prompt 2



Context: I am exposing the following React components/hooks via Module Federation to other host applications. They need clear documentation so external teams know how to consume them safely.
Source Code:
[Paste the code of your exposed components here, e.g., Button.jsx, UserProfile.tsx]
Task: Create technical API documentation for these exposed items. Include:

Clear explanation of the component's purpose.

A Markdown table detailing all Props (Name, Type, Required/Optional, Default Value, Description).

A code snippet demonstrating exactly how a Host application should dynamically or statically import and use this exposed module.

# Prompt 3: For Deployment & Shared Dependency Gotchas

Module Federation issues usually happen during deployment or runtime dependency mismatches.

Context: This React app runs in a Module Federation mesh. We need a CONTRIBUTING.md or a DEPLOYMENT.md section handling runtime risks.
Shared Config: [Paste the shared object from your config, e.g., singleton: true]
Task: Write a guide for developers on:

How changing shared dependencies (like upgrading React or a state management library) impacts the host and other remotes.

The deployment order (e.g., why remotes should generally be deployed before or independently of hosts).

How to verify the remoteEntry.js file is properly generated and accessible after a build.


# Single prompt Agent mode
Activate Agent Mode. I need you to build a comprehensive, multi-file documentation suite for this React Microview application. 

Context: 
This repository is a micro-frontend utilizing Module Federation. Please look at our module federation configuration file (e.g., webpack.config.js, vite.config.js, or rspack.config.js) and the package.json to understand our architecture.

Task:
Please autonomously create and write the following files directly into my repository:

1. Create/Update `README.md` at the root:
   - Provide a project overview based on our code structure.
   - Document the Module Federation layout: Is this a Host or Remote? What does it expose, and what does it consume? Include a clear architecture summary.
   - Document the local development setup, explicitly stating the port it runs on and required env variables.
   - Add a "Documentation Index" linking to the files below.

2. Create `docs/EXPOSED_API.md`:
   - Scan our exposed components/hooks (defined in our federation config).
   - For each exposed module, generate a technical API contract table detailing all Props (Name, Type, Required/Optional, Default, Description).
   - Provide clean code snippets showing exactly how an external Host application should import and consume these exposed modules.

3. Create `docs/DEPLOYMENT.md`:
   - Document our shared dependencies strategy (singletons, version matching).
   - Detail the deployment considerations (e.g., independent remote deployment, verifying the remoteEntry.js path).

Please create these directories and files directly. Let me know when the architecture suite is fully generated.
