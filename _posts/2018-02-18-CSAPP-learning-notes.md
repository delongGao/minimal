---
layout: default
title:  "CSAPP learning notes"
date:   2018-02-18 15:10:01 -0600
categories: learning_notes CSAPP
---
========================== 2018/02/18 ===========================
- shift operations
  - left: drop left bits, padding right bits with `0`
  - right:
    - logical: padding left with `0`
    - arithmetical: padding left with `MSB(most significant bit)`
  - General approach for dealing with shifting greater than word size, example 35 or 66: __doing modulo on word size__.
- Common data types
  - __1 byte = 8 bits = 2 hex__
  - char type: 1 byte
  - short type: 2 bytes
  - int: 4 bytes
  - long: 4 bytes / 8 bytes
  - 32t: 4 bytes
  - 64t: 8 bytes
  - NOTE: be aware of the difference on word size: 32 vs. 64

========================== 2018/02/25 ===========================
- unsigned numbers
  - Umin: 0b0000...0000 (all zeros)
  - Umax: 0b1111...1111 (all ones)
- signed numbers (two's complement)
  - MSB is sign bit, has negative weight
  - Tmin: 0b10000...0000 (all zeros EXCEPT first / sign bit)
  - Tmax: 0b01111...1111 (all ones EXCEPT first / sign bit)
- casting(type conversion between the two)
  - At least in C, the conversion happens at bit level
  - For both U2T and T2U, it converts to bit patterns first and use target way of interpreting bits