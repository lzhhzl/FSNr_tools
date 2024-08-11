# Usage
> only tested on windows

> remember to put SomeKey.bin along with main.exe

> **Work in progress**

```shell
g++ --std=c++20 -O2 main.cpp -o main.exe
g++ --std=c++20 -O2 env_main.cpp -o enc_main.exe

./main.exe "[path to epk]"
./enc_main.exe "[path to epk.epk_dec]"

# example
# ./main.exe root#data#locale#ck#epk#uistring.epk
# and find the dec file in the same folder: root#data#locale#ck#epk#uistring.epk_dec

# ./enc_main.exe root#data#locale#ck#epk#uistring.epk_dec
# and find the dec file in the same folder: root#data#locale#ck#epk#uistring.epk_enc
```

## Note
**Alert** I still can't figure out what the last 0x30 bytes in dec file means, though encrypt the unmodified epk_dec to epk_enc is identical to the original epk.

I dont know if the epk is modified, the last 0x30 bytes should change according or not.

The epk encryption method can be found in `try_dec.h` and `strangefun1.h`, I simplified the original obfs code dumped from ida.

# Tips
SomeKey.bin dumps from 0x1409E6500

FDT file decrypt script can be found in scripts folder, (but badly written in python)
