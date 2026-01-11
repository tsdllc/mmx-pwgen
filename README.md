# Mega Man X Password Generator

A single-file HTML application that generates valid Mega Man X (SNES) passwords based on user-selected game progress flags.

## Features

- **Interactive UI**: Click tiles to toggle game progress flags
- **Real-time Password Generation**: Password updates immediately when flags change
- **Responsive Design**: Works on desktop and mobile devices
- **24 Game Progress Flags**:
  - 8 Mavericks Defeated
  - 8 Heart Tanks Collected
  - 4 Sub-Tanks Collected
  - 4 X Armor Upgrades

## Usage

Simply open `pwgen.html` in any modern web browser. Click on tiles to toggle them on/off, and the password will update automatically.

## Implementation

The password generator implements the Mega Man X password algorithm using:
- Binary flags for all 24 game progress items
- Position-based calculation with X/Y altering factors
- Even/odd main factor counting to select password digits

## Password Format

Passwords are displayed in a 4x3 grid (12 digits total), formatted as:
```
XXXX-XXXX-XXXX
```

## Technical Notes

The implementation follows the password algorithm specification with:
- All flags initialized to `false` (skip intro state)
- Dynamic password recalculation on flag changes
- Visual feedback for selected/unselected states
- Graceful handling of missing image assets

## License

See LICENSE file for details.
