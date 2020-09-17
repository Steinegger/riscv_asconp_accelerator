Meta repo of the implementation of the Ascon-p[1][2] permutation as a hardware instruction for the CV32E40P/RI5CY RISC-V core. The paper is to be published at CARDIS2020 and also available on [eprint](https://eprint.iacr.org/2020/1083).

# Publication
>Abstract: Ascon-p is the core building block of Ascon, the winner in the lightweight category of the CAESAR competition. With ISAP, another Ascon-p-based AEAD scheme is currently competing in the 2nd round of the NIST lightweight cryptography standardization project. In contrast to Ascon, ISAP focuses on providing hardening/protection against a large class of implementation attacks, such as DPA, DFA, SFA, and SIFA, entirely on mode-level. Consequently, Ascon-p can be used to realize a wide range of cryptographic computations such as authenticated encryption, hashing, pseudorandom number generation, with or without the need for implementation security, which makes it the perfect choice for lightweight cryptography on embedded devices.
>
>In this paper, we implement Ascon-p as an instruction extension for RISC-V that is tightly coupled to the processors register file and thus does not require any dedicated registers. This single instruction allows us to realize all cryptographic computations that typically occur on embedded devices with high performance. More concretely, with ISAP and Ascon's family of modes for AEAD and hashing, we can perform cryptographic computations with a performance of about 2 cycles/byte,or about 4 cycles/byte if protection against fault attacks and power analysis is desired.
>
>As we show, our instruction extension requires only 4.7 kGE, or about half the area of dedicated Ascon co-processor designs, and is easy to integrate into low-end embedded devices like 32-bit ARM Cortex-M or RISC-V microprocessors. Finally, we analyze the provided implementation security of ISAP, when implemented using our instruction extension. 

You can cite us:
```
@misc{cryptoeprint:2020:1083,
    author = {Stefan Steinegger and Robert Primas},
    title = {A Fast and Compact Accelerator for Ascon and Friends},
    howpublished = {Cryptology ePrint Archive, Report 2020/1083},
    year = {2020},
    note = {\url{https://eprint.iacr.org/2020/1083}},
}
```

# Structure
**hw_core**: contains hardware design of the modified RI5CY/CV32E40P RISC-V core.  
**riscv-isa-sim**: contains a functional riscv-isa-sim model with the added Ascon-p instruction.  


# References:  
[1] https://ascon.iaik.tugraz.at/  
[2] https://isap.iaik.tugraz.at/
