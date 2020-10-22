---
title: "Arbitrary Precision Integers"
created: September-October 2020
collection: portfolio
order: 1040
---
Arbitrary Precision Integers is a small C library for arbitrary precision positive integers. In C, integers are restricted to a maximum size of 64-bits. For storing integers greater than 2<sup>64</sup>-1, types with higher capacities are needed. The arbitary precision integer type in this library is virtually unrestricted in size. Supported operations on this type are addition, subtraction, left bitwise shift, and comparison.

These are the supported functions for the arbitrary precision integer type (ApInt):

`ApInt *apint_create_from_u64(uint64_t val);`

`ApInt *apint_create_from_hex(const char *hex);`

`void apint_destroy(ApInt *ap);`

`uint64_t apint_get_bits(ApInt *ap, unsigned n);`

`int apint_highest_bit_set(ApInt *ap);`

`ApInt *apint_lshift(ApInt *ap);`

`ApInt *apint_lshift_n(ApInt *ap, unsigned n);`

`char *apint_format_as_hex(ApInt *ap);`

`ApInt *apint_add(const ApInt *a, const ApInt *b);`

`ApInt *apint_sub(const ApInt *a, const ApInt *b);`

`int apint_compare(const ApInt *left, const ApInt *right);`

`apint_create_from_u64`: Returns a pointer to an ApInt instance whose value is specified by the val parameter, which is a 64-bit unsigned value.

`apint_create_from_hex`: Returns a pointer to an ApInt instance whose value is specified by the hex parameter, which is an arbitrary sequence of hexadecimal (base 16) digits. This function should accept both the lower-case letters a through f and the upper-case letters A through F as the hex digits with values 10 through 15.

`apint_destroy`: Deallocates the memory used by the ApInt instance pointed-to by the ap parameter.

`apint_get_bits`: Returns a uint64_t value containing 64 bits of the binary representation of the ApInt instance pointed to by ap. The parameter n indicates which bits to return. If n is 0, bits 0..63 are returned, if n is 1 bits 64..127 are returned, etc. The function should be prepared to handle arbitrarily large values of n.

`apint_highest_bit_set`: Returns the position of the most significant bit set to 1 in representation of the ApInt pointed to by ap. As a special case, returns -1 if the ApInt instance pointed to by ap represents the value 0.

`apint_lshift`: Returns a pointer to an ApInt instance formed by shifting each bit of the ApInt instance pointed to by ap one bit position to the left.

`apint_lshift_n`: Returns a pointer to an ApInt instance formed by shifting each bit of the ApInt instance pointed to by ap n bit positions to the left.

`apint_format_as_hex`: Returns a pointer to a dynamically-allocated C character string containing the hexadecimal (base 16) digits of the representation of the ApInt instance pointed to by ap. Note that the hex digits representing the values 10 through 15 should be lower-case a through f. The string returned should not have any leading zeroes, except in the special case of the ApInt instance representing the value 0, in which case the returned string should consist of a single 0 digit.

`apint_add`: Computes the sum a plus b, and returns a pointer to an ApInt instance representing the sum.

`apint_sub`: Computes the difference a minus b, and returns a pointer to an ApInt instance representing the difference. As a special case, if b is greater than a, returns NULL (since the ApInt data type cannot represent a negative value.)

`apint_compare`: Compares the values represented by the ApInt instances pointed-to by the parameters left and right. Returns a negative value if left is less that right, a positive value if left is greater than right, and 0 if the values are equal.
