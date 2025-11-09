# ZMK Cradio Configuration

Miryoku-inspired ZMK firmware configuration for the Sweep keyboard with native mouse support, home row mods, and 6 functional layers optimized for a 34-key split layout.

## Features

- **Home Row Modifiers**: Optimized timing (170ms tap, 300ms quick-tap) for comfortable typing
- **Native Mouse Support**: Full mouse movement and scrolling with acceleration via urob's ZMK fork
- **6 Functional Layers**: Base, Symbols, Numbers, Navigation/Mouse, Function keys, and System settings
- **Multi-Device Bluetooth**: Support for up to 5 paired devices with quick switching
- **Low Latency**: Aggressive debouncing (1ms press, 5ms release) for responsive input
- **Power Optimized**: Deep sleep after 30 minutes, increased BT transmission power

## Hardware

- **Keyboard**: Sweep - 34-key split ergonomic keyboard
- **Controller**: nice!nano v2 (wireless Bluetooth)
- **Layout**: 3x5 column-staggered + 2 thumb keys per hand

## Keymap

### Layer 0: BASE (QWERTY)

```
┌───┬───┬───┬───┬───┐       ┌───┬───┬───┬───┬───┐
│ Q │ W │ E │ R │ T │       │ Y │ U │ I │ O │ P │
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│ A │ S │ D │ F │ G │       │ H │ J │ K │ L │ ' │
│GUI│ALT│CTL│SFT│   │       │   │SFT│CTL│ALT│GUI│
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│ Z │ X │ C │ V │ B │       │ N │ M │ , │ . │ / │
└───┴───┴───┼───┼───┤       ├───┼───┼───┴───┴───┘
            │ESC│BSP│       │SPC│ENT│
            │ L3│ L4│       │ L1│ L2│
            └───┴───┘       └───┴───┘
```

Home row modifiers on A-S-D-F (left) and J-K-L-' (right).
Thumb keys: tap for key, hold for layer access.

### Layer 1: SYM (Symbols)

```
┌───┬───┬───┬───┬───┐       ┌───┬───┬───┬───┬───┐
│ { │ ( │ * │ ) │ } │       │   │   │   │   │   │
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│ : │ $ │ % │ ^ │ + │       │   │   │   │   │   │
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│ ~ │ ! │ @ │ # │ | │       │   │   │   │   │   │
└───┴───┴───┼───┼───┤       ├───┼───┼───┴───┴───┘
            │ & │ _ │       │ X │ X │
            └───┴───┘       └───┴───┘
```

Accessed by holding Space (right thumb). Right side keys are transparent.

### Layer 2: NUM (Numbers)

```
┌───┬───┬───┬───┬───┐       ┌───┬───┬───┬───┬───┐
│ [ │ 7 │ 8 │ 9 │ ] │       │   │   │   │   │   │
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│ ; │ 4 │ 5 │ 6 │ = │       │   │   │   │   │   │
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│ ` │ 1 │ 2 │ 3 │ \ │       │   │   │   │   │   │
└───┴───┴───┼───┼───┤       ├───┼───┼───┴───┴───┘
            │ 0 │ - │       │ X │ X │
            └───┴───┘       └───┴───┘
```

Accessed by holding Enter (right thumb). Numpad-style arrangement on left hand.

### Layer 3: NAV (Navigation + Mouse + Media)

```
┌────┬────┬───┬────┬────┐       ┌───┬───┬───┬───┬───┐
│MB4 │MB5 │   │SCR↓│SCR↑│       │M← │M↓ │M↑ │M→ │DEL│
├────┼────┼───┼────┼────┤       ├───┼───┼───┼───┼───┤
│GUI │ALT │CTL│SFT │    │       │ ← │ ↓ │ ↑ │ → │TAB│
├────┼────┼───┼────┼────┤       ├───┼───┼───┼───┼───┤
│PLY │PRV │NXT│VOL-│VOL+│       │MCK│PD │PU │   │CAP│
└────┴────┴───┼────┼────┤       ├───┼───┼───┴───┴───┘
              │    │    │       │RC │LC │
              └────┴────┘       └───┴───┘
```

Accessed by holding Esc (left thumb).
- **Left side**: Mouse buttons (MB4/MB5), scroll wheel, media controls
- **Right side**: Mouse movement, arrow keys, page navigation
- **Thumbs**: Right/Left mouse click

Legend:
- MB4/MB5: Mouse back/forward buttons
- SCR↓/↑: Scroll down/up
- M←↓↑→: Mouse movement
- PLY/PRV/NXT: Play/Previous/Next track
- VOL-/+: Volume down/up
- MCK/RC/LC: Middle/Right/Left mouse click
- PD/PU: Page Down/Up
- CAP: Caps Lock

### Layer 4: FN (Function Keys)

```
┌───┬───┬───┬───┬───┐       ┌───┬───┬───┬───┬───┐
│   │   │   │   │   │       │F12│F7 │F8 │F9 │   │
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│   │   │   │   │   │       │F11│F4 │F5 │F6 │   │
├───┼───┼───┼───┼───┤       ├───┼───┼───┼───┼───┤
│   │   │   │   │   │       │F10│F1 │F2 │F3 │   │
└───┴───┴───┼───┼───┤       ├───┼───┼───┴───┴───┘
            │ X │ X │       │ L5│   │
            └───┴───┘       └───┴───┘
```

Accessed by holding Backspace (left thumb). Function keys F1-F12 on right hand.
Right inner thumb (hold) accesses Layer 5 (Accent layer - not configured).

### Layer 6: SETTINGS (System + Bluetooth)

```
┌────┬───┬───┬───┬───┐       ┌───┬───┬───┬───┬────┐
│RST │   │   │   │BT0│       │BT3│OUT│   │   │RST │
├────┼───┼───┼───┼───┤       ├───┼───┼───┼───┼────┤
│BOOT│   │   │   │BT1│       │BT4│   │   │   │BOOT│
├────┼───┼───┼───┼───┤       ├───┼───┼───┼───┼────┤
│    │   │   │   │BT2│       │CLR│   │   │   │    │
└────┴───┴───┼───┼───┤       ├───┼───┼───┴───┴────┘
             │   │   │       │ L0│   │
             └───┴───┘       └───┴───┘
```

Legend:
- **BT0-BT4**: Select Bluetooth profile (5 device slots)
- **OUT**: Toggle between USB/Bluetooth output
- **CLR**: Clear current Bluetooth profile
- **RST**: System reset (both halves)
- **BOOT**: Enter bootloader mode for firmware flashing
- **L0**: Return to base layer

## Mouse Configuration

Native mouse support with custom acceleration:
- **Movement**: Acceleration exponent 2, max speed 750ms, sensitivity 1600
- **Scrolling**: Acceleration exponent 1, max speed 5000ms, sensitivity 100
- **Buttons**: Left, right, middle, back (MB4), forward (MB5)

Mouse controls accessible on navigation layer (Layer 3).

## Installation

### Automated Build

Firmware is automatically built via GitHub Actions on every commit.

1. Go to the **Actions** tab in this repository
2. Select the latest successful workflow run
3. Download the firmware artifacts:
   - `cradio_left` - Left half firmware
   - `cradio_right` - Right half firmware
   - `settings_reset` - Factory reset utility

### Flashing

1. Connect nice!nano v2 via USB
2. Double-tap the reset button to enter bootloader mode (drive appears as `NICENANO`)
3. Copy the appropriate `.uf2` file to the drive
4. Drive will automatically disconnect when flashing completes
5. Repeat for the other half

### Initial Pairing

1. Power on both halves
2. On your device, scan for Bluetooth devices
3. Connect to "Cradio" (usually the left half advertises)
4. Both halves should automatically pair with each other

## Technical Specifications

### Timing Configuration

- **Debounce**: 1ms press, 5ms release (eager debouncing)
- **Home Row Mods**: 170ms tapping term, 300ms quick-tap-ms, tap-preferred flavor
- **Thumb Keys**: 170ms tapping term, balanced flavor

### Power Management

- **Deep Sleep**: Enabled after 30 minutes (1,800,000ms) of inactivity
- **BT Transmission Power**: +8dBm for extended range

### ZMK Configuration

- **Fork**: urob's ZMK with native mouse support
- **Branch**: `main-with-native-mouse`
- **Repository**: https://github.com/urob

## Build Targets

The build configuration produces three firmware images:
- **cradio_left**: Left half
- **cradio_right**: Right half
- **settings_reset**: Factory reset for both halves
