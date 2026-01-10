# Ninja Generator (`gen_ninja.py`)

A minimalist pre-processor for Ninja build files that adds support for Bash execution and file pattern expansion.

## Features
1. **Pure Bash:** `$(date)` -> Executes shell command and injects output.
2. **Custom Pattern (Non-Bash):** 
   - `$(for f in %.c; build %.o: cc %.c))`
   - This is a **special generator syntax**, not a standard shell loop.
   - `%`: Captured the filename.

## Usage
- **Generate:** `python3 gen_ninja.py build.ninja.in`
- **Build:** `ninja` (auto-updates itself).

## Example
Example `build.ninja.in` for repo [clibs](https://github.com/oscarpaa/clibs).