# Mega Man X Password Generator

A single-file HTML application that generates valid Mega Man X (SNES) passwords based on user-selected game progress flags.

## Features

- **Interactive UI**: Click tiles to toggle game progress flags
- **Real-time Password Generation**: Password updates immediately when flags change
- **Responsive Design**: Works on desktop and mobile devices
- **Correct Algorithm**: Implements Password Set #1 from MMHP Password Crack documentation
- **24 Game Progress Flags**:
  - 8 Mavericks Defeated
  - 8 Heart Tanks Collected
  - 4 Sub-Tanks Collected
  - 4 X Armor Upgrades

## Usage

Simply open `pwgen.html` in any modern web browser. Click on tiles to toggle them on/off, and the password will update automatically.

## Password System

The password generator implements Password Set #1 based on the [MMHP Password Crack](https://www.mmhp.net/Passwords/PassCrackX1.html) documentation. The algorithm uses:

- **Base Password** (all flags false): `1768-5858-3884`
- Group-based item counting for conditional logic
- Odd/even counting for hearts, bosses, and capsules/subtanks
- 12 squares with specific conditional rules per the MMHP specification

## Password Format

Passwords are displayed in a 4x3 grid (12 digits total), formatted as:
```
XXXX-XXXX-XXXX
```

## Validation

The base password `1768-5858-3884` has been verified against the MMHP Password Crack documentation. For complex flag combinations, cross-reference with the [MMHP Interactive Generator](https://www.mmhp.net/Passwords/MMX1/).

## Technical Notes

- Single HTML file with inline CSS and JavaScript
- No external dependencies
- Gracefully handles missing image assets
- Algorithm directly implements MMHP Password Set #1 specification

## License

See LICENSE file for details.
