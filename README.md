# Computational Theory Assessment

**Student Name:** Hammad Mubarik
**Student ID:** G00414448
**Module:** Computational Theory
**Lecturer:** Ian McLoughlin

---


### Prerequisites
To run the notebook locally, you will need **Python** installed along with the following libraries:
* `jupyter` (to run the notebook)
* `numpy` (for 32-bit integer operations)
* `pandas` (for data formatting)

### Installation & Usage
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/](https://github.com/)[YourUsername]/computational-theory-assessment.git
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd computational-theory-assessment
    ```
3.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
4.  Open `problems.ipynb` to view the code and explanations.

---

##  Problem Summaries

The assessment is divided into five distinct problems, each focusing on a different aspect of the SHA-256 algorithm.

### [Problem 1: Binary Words and Operations](problems.ipynb)
**Objective:** Implement the core logical functions used in SHA-256 logic using `numpy`.
* Defined functions for `Ch` (Choose), `Maj` (Majority), `ROTR` (Rotate Right), and `SHR` (Shift Right).
* Implemented the specific Sigma functions: $\Sigma_0$, $\Sigma_1$, $\sigma_0$, and $\sigma_1$.
* Ensured all operations utilize strict 32-bit integer arithmetic to match the Secure Hash Standard.

### [Problem 2: Fractional Parts of Cube Roots](problems.ipynb)
**Objective:** Generate the initial hash constants ($K_t$) defined in the SHA-256 standard.
* Implemented a prime number generator to find the first 64 prime numbers.
* Calculated the cube root of each prime.
* Extracted the first 32 bits of the fractional parts to verify they match the standard constants.

### [Problem 3: Padding](problems.ipynb)
**Objective:** Implement the message padding scheme (Merkle-Damgård construction).
* Created a `block_parse` function to preprocess inputs.
* Ensured messages are padded with a `1` bit, followed by `0` bits, and finished with the 64-bit length of the original message.
* Verified that all outputs are multiples of 512 bits (64 bytes).

### [Problem 4: Hashing](problems.ipynb)
**Objective:** Simulate the SHA-256 compression function.
* Implemented the message schedule ($W_t$) generation.
* Wrote the main loop that updates the working variables ($a$ through $h$) using the logical functions from Problem 1 and constants from Problem 2.
* Verified the output against known hash values.

### [Problem 5: Passwords (Rainbow Table Attack)](problems.ipynb)
**Objective:** Reverse-engineer SHA-256 hashes to find original passwords.
* **Context:** Provided with three SHA-256 hashes of common passwords.
* **Method:** Implemented a **Dictionary Attack** (Simulated Rainbow Table) by pre-computing hashes for a list of common passwords and performing a reverse lookup.
* **Security Analysis:** Discussed the vulnerability of unsalted hashes and how **salting** and **key stretching** (e.g., bcrypt) can prevent such attacks.

---

## References
* **NIST FIPS 180-4:** [Secure Hash Standard (SHS)](https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf) - The official documentation for the SHA-256 algorithm.
* **Python Documentation:** [hashlib — Secure hashes and message digests](https://docs.python.org/3/library/hashlib.html)
* **NumPy Documentation:** [NumPy v1.26 Manual](https://numpy.org/doc/stable/)

---

*This repository was created for educational purposes as part of the GMIT/ATU Computational Theory module.*