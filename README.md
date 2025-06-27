# Access Card Data Converter

A single page tool to do some basic access card / swipe card / RFID data conversion for access control systems
#### Access live at: https://joshua1909.github.io/accesscardconverter/main.html

## What it does

Takes messy card data and converts it between formats. Attempts to handle preambles, parity errors, and different bit structures.

## Features

- **Format Detection** - Automatically identifies card format from binary/hex data
- **Multi-format Support** - 26-bit, 32-bit, etc
- **Preamble Handling** - Strips and adds preambles of any length
- **Parity Validation** - Calculates and validates parity bits with error reporting
- **Bidirectional Conversion** - Convert between binary, hex, facility codes, and card numbers
- **Smart Padding** - Automatically pads hex data to correct bit lengths

## Issues

**Wrong output values?**
- Check preamble length (18 bits for 26-bit, 12 bits for 32-bit are common)
- Verify you selected the right format
- Some real-world data has parity errors

**Format not detected?**
- Try the Format Validator first
- Check if your data includes a preamble
- Consider custom format for unusual bit lengths

## Technical Notes

- Uses client-side JavaScript only - no server required
- Handles leading zero padding automatically
- Validates parity bits but doesn't require them to be correct
- Supports bit lengths up to 128 bits for custom formats

## Contributing

Found a bug or want to add a format? Pull requests welcome. 

