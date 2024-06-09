# Jenkins-integration-with-GIT
This repository demonstrates a Jenkins pipeline for automating tasks with Python and JavaScript scripts. <br />
The pipeline includes stages to check the build environment, execute a Python script, read a JavaScript file, <br /> and send a Slack notification upon completion.

## Pipeline Overview
**Agent:** Any available agent. <br />
**Environment Variables:** <br />
  - PYTHON_FILE: Specifies the Python script to run (helloworld.py). <br />
  - JAVASCRIPT_FILE: Specifies the JavaScript file to read (helloworld.js).

## Pipeline Stages
**Check:**
  - Outputs the current date, GIT branch, build ID, and build URL.

**Run Python Script:**
  - Executes the specified Python script.

**Read JavaScript File:**
  - Displays the content of the specified JavaScript file.

**Slack Notification:**
  - Sends a Slack message indicating the completion of the testing stages.

## Requirements
Jenkins <br />
Python 3.x <br />
Node.js <br />
Slack (for notifications)
