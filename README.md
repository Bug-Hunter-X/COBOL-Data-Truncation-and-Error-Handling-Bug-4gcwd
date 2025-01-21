# COBOL Data Truncation and Error Handling Bug

This repository demonstrates a common but easily overlooked bug in COBOL programs: data truncation and insufficient error handling.  The `bug.cob` file contains the erroneous code. The `bugSolution.cob` file provides a corrected version with improved error handling and data validation.

**Bug Description:**
The original code snippet attempts to move data from `WS-INPUT-DATA` to `WS-OUTPUT-DATA`. If `WS-INPUT-DATA` is longer than `WS-OUTPUT-DATA`, data will be silently truncated, leading to incorrect results.  Additionally, no error handling exists for non-numeric data input. 

**Solution:**
The solution involves adding explicit checks for data length and handling potential errors.  This includes a thorough check for input validity before any data movement takes place.