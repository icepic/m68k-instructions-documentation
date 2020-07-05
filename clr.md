## CLR Clear an operand

## Operation
[destination] ← 0

## Syntax
```assembly
CLR <ea>
```
## Sample syntax
```assembly
CLR (A4)+
```

## Attributes
Size = byte, word, longword

## Description
The destination is cleared ó loaded with all zeros. The CLR in-
struction can't be used to clear an address register. You can use
SUBA.L A0,A0 to clear A0. Note that a side effect of CLRís imple-
mentation is a read from the specified effective address before the
clear (i.e., write) operation is executed. Under certain circum-
stances this might cause a problem (e.g., with write-only memory).

## Condition codes
|X|N|Z|V|C|
|--|--|--|--|--|
|-|0|1|0|0|

## Source operand addressing modes
|Dn|An|(An)|(An)+|-(An)|(d,An)|(d,An,Xi)|ABS.W|ABS.L|(d,PC)|(d,PC,Xn)|imm|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|✓||✓|✓|✓|✓|✓|✓|✓||||