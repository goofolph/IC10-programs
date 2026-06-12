# Printer Vending

This will have multiple ICs working together to control the printers and a vending machine.

The Vending Machine will have a IC housing, this will allow printers to send reagents and quanties to be dispensed to the stack. The vending machine code will control the stackers and output to send the right reagents.

Each printer will have two ICs, one to manage printing count using the stacker for quantities, the other will be to request missing reagents by sending them to a stack of the vending machine's IC.

## Vending Stack

| Index | Purpose   | Type  |
| ----- | --------- | ----- |
| 0     | Mutex     | Bool  |
| 1     |           |       |
| 2     |           |       |
| 3     |           |       |
| 4     |           |       |
| 5     |           |       |
| 6     |           |       |
| 7     |           |       |
| 8     | Reagent 1 | Hash  |
| 9     | Reagent 2 | Count |
| 10    | Reagent 1 | Hash  |
| 11    | Reagent 2 | Count |

sp 0 will be a mutex of sorts, while this is true no other ICs can add/remove to the stack, this is to prevent race conditions of printers adding while the vending machine removes or two printers adding at the same time. This will be set during changes by both the vending machine and printers.

Each reagent will have it's hash and quantity sent as a pair. this will start at sp 8 leaving 0-7 for the mutex and other variables/settings.

## Printer Setup

Each printer will have two ICs. They will have the printer on d0 and one will have the output stacker on d1 and the other will have the input sorter on d2.

## Vending Setup

The vending machine will have an input and output stacker. The vending machine IC Housing for requests will be named "Vending IC Housing".
