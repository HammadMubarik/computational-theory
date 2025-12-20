# computational-theory

# SHA-256 Implementation

These Problems focus on different aspects of the Secure Hash Standard

## In this notebook you will find 5 Probelems

**Problem 1** - Basic SHA functions (Ch, Maj, Parity, Sigma, ROTR, SHR)

**Problem 2** - Generate K constants from cube roots of first 64 primes

**Problem 3** - Message padding and block parser (yields 512-bit blocks)

**Problem 4** - Main hash compression function

**Problem 5** -

## Running It

You need Python 3 and NumPy. Open the Jupyter notebook and run cells in order.

## Notes

- Uses 32-bit math with modulo 2³² (overflow warnings are normal)
- Big-endian everywhere
- Test cases verify against known SHA-256 outputs

## References

FIPS 180-4 Secure Hash Standard
Claude was used to Generate some of the more Challenging parts of code
