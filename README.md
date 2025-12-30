# TaskGlitch — SDE Assignment Bug Fixes

TaskGlitch is a React + TypeScript task management application designed for sales teams to prioritize tasks based on ROI (Return on Investment).

As part of this assignment, I identified and fixed five critical bugs related to:
- Double API fetch on page load
- Undo snackbar state not clearing correctly
- Unstable task sorting when ROI and priority are equal
- Multiple dialogs opening due to event bubbling
- ROI calculation errors with invalid or zero values

The application is now stable, deterministic, and user-friendly.  
All edge cases are handled, build issues are fixed, and the app is successfully deployed using **Vercel**.


This repository contains fixes for all mandatory bugs described in the SDE Assignment for the TaskGlitch application.

##  Bugs Fixed

###  Bug 1 — Double Fetch Issue
- Prevented duplicate API/data fetch on page load
- Ensured fetch runs exactly once even in React StrictMode

###  Bug 2 — Undo Snackbar Bug
- Reset `lastDeletedTask` when snackbar closes
- Prevented old deleted tasks from reappearing incorrectly

###  Bug 3 — Unstable Sorting
- Added stable deterministic tie-breaker
- Tasks with same ROI & priority now sort alphabetically by title

###  Bug 4 — Double Dialog Opening
- Fixed event bubbling using `stopPropagation`
- Edit/Delete actions now open only their respective dialogs

###  Bug 5 — ROI Calculation Errors
- Added validation for zero/invalid time and revenue
- Prevented NaN, Infinity values
- Ensured safe ROI formatting


##  Tech Stack
- React + TypeScript
- Material UI
- Vite


##  Live Demo
https://task-glitch-nu.vercel.app/


##  Assignment Requirements
- All 5 mandatory bugs fixed
- Clean commit history
- Public GitHub repository
- Live deployed app (required)

##  Author
**Nithin Y M**
