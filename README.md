
# Catalyst-JS

Catalyst-JS is a basic virtual machine, implemented in JavaScript, based on Alan L. Bryan's "How to create your own virtual machine! Part I"

### Hardware Features

  - 60 KB for program memory
  - 16-bit processor
  - Custom clock speeds
  - 4 KB for graphics memory
  - 80 column x 25 row screen

### Software Features

Translation from Catalyst's custom Assembler Language Implementation (ALI) into byte-code. Example .ALI file:

```sh
Start:
 LDA #65
 LDX #$A000
 STA ,X
 LDA #76
 LDX #$A002
 STA ,X
 LDA #73
 LDX #$A004
 STA ,X
 END Start
```

This ALI program will push the letters "A," "L," and "I," to the memory allocated for the screen (0xA000 - 0xAFA0).

### Bytecode

Dillinger is currently extended with the following plugins. Instructions on how to use them in your own application are linked below.

| Mnemonic | Bytecode | Purpose |
| ------ | ------ | ------ |
| LDA | 0x01 | Assigns a value to our A register |
| LDX | 0x02 | Assigns a value to our X register |
| STA | 0x03 | Stores the value of the A register to a memory location |
| END | 0x04 | Terminates the ALI program |


### Development

Want to contribute? Great! 

Catalyst-JS is just a simple passion project, feel free to clone or fork as you wish.