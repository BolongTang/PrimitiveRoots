Topics: Number Theory, modulo arithmetics

Express the given quotient as the power of some primitive root using the given modulus. 

To find integer solutions of x^15 = 7 mod 19 requires sieving the primitive roots of mod 19, which are 2,3,10,13,14, and 15. This tool rewrites the 7 (quotient) as a root raised to some power, and rewrites x = root^y. (Next, proceed by equating the exponents mod (19 - 1), solving for y, and then solving for x.)

## Usage

### Web Interface (GitHub Pages)

Visit the [GitHub Pages site](https://BolongTang.github.io/PrimitiveRoots/) to use the tool directly in your browser without installing Python.

The web interface provides the same functionality as the command-line version with an easy-to-use form interface. It uses [Pyodide](https://pyodide.org/) to run Python code directly in your browser.

**Features:**
- No installation required
- Same algorithm as the command-line version
- Pre-filled example values
- Clean, intuitive interface
- Works on any device with a web browser

See [SETUP.md](SETUP.md) for instructions on enabling GitHub Pages for this repository.

### Command Line

`sampleRun.txt` shows a sample run. 

Run `python PrimitiveRoots.py` and follow the input prompts for results. 

Run `python TestPrimitiveRoots.py` to see the unit tests passing. 



