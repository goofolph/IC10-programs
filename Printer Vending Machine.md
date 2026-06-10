Place one vending machine for all printing stations. This will hold the ingots and allows.

Per Printing machine place the following:
- Printer on d0
- Stacker on d1
- Sorter on d2

Connect to same vending machine on d3 for all printer's housing.

The sorters will have the right output connect to the input side of each printer. Recommended to use a junction to allow both manual and automatic refilling of the printer.

The output of the printer should be connect to a stacker for ease of use and combinded with the "Printer Stacker" program.

The front of the vending machine should have a chute tunnel that connects to a printer's sorter input. The output of each printer's sorter should be connected to the next printer's sorter or the vending machine's input if no more printers are connected in the line.

Each printer's program will retry after a given number of attempts (60) before giving up and going back to the start. This can manually be reset by exporting the program again or pulling the chip out and putting it back in.