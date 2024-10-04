# tsk_tracker_cli
a solution to the project [Task Tracker CLI](http://roadmap.sh/projects/task-tracker)

# Main language
  C (GNU v2.35)

# Compiler
  GCC 4.7

# The Main Logic
```mermaid
  graph TD
  A[Command Line Get the command and Send to the Analyzer]
  B{Read the command, is it legal for the program?}
  B --> |No| C[error dealing]
  B --> |Yes| D{analyze the command}
  C --> F{want to end?}
  F --> |No| A
  F --> |Yes| E[end]
  D --> |List| M[read the JSON file]
  D --> |Task Operation| N[edit the JSON file]
  D --> |Termination| F
  M --> P[new and clean command line]
  N --> P
  P --> B
```

# The Main  API
   
