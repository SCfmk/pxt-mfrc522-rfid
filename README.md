# MFRC522 RFID for micro:bit — P0 version

This is a MakeCode extension for the MFRC522 RFID reader.

It is the same implementation as the supplied MFRC522 extension, except that the SPI chip-select / SS pin has been changed from **P16** to **P0**.

## Pin assignment

| MFRC522 signal | micro:bit pin |
|---|---|
| MOSI | P15 |
| MISO | P14 |
| SCK | P13 |
| SS / CS | **P10** |

The library configures SPI as:

```typescript
pins.spiPins(DigitalPin.P15, DigitalPin.P14, DigitalPin.P13)
```

and uses P10 for chip select.

## MakeCode blocks

The extension provides the same blocks as the original library:

- Initialize MFRC522 Module
- Read ID
- Read data
- Write Data
- Turn off antenna

## Installing from GitHub

1. Create a GitHub repository, for example `pxt-mfrc522-p10`.
2. Upload the files in this folder to the root of the repository.
3. In MakeCode for micro:bit, choose **Extensions**.
4. Paste the GitHub repository URL into the search box.
5. Select the extension.

## Change from the original

All occurrences of:

```typescript
DigitalPin.P16
```

have been changed to:

```typescript
DigitalPin.P10
```

No other functional changes have been made to `main.ts`.
