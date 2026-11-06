# Arduino board support package

The **EnviroDIY ATmega Boards** package contains Arduino board support files for AVR boards developed by EnviroDIY.
It is maintained by Stroud Water Research Center - EnviroDIY; contact [info@envirodiy.org](mailto:info@envirodiy.org).
See [https://www.envirodiy.org/](https://www.envirodiy.org/) for project information and [https://www.envirodiy.org/help/](https://www.envirodiy.org/help/) for help.

This package is version 2.2.1, built on 2026-11-06.
Its source is maintained at [https://github.com/EnviroDIY/EnviroDIYAVRBoards](https://github.com/EnviroDIY/EnviroDIYAVRBoards).
Package archives are published from [https://github.com/EnviroDIY/Arduino_boards/raw/master/EnviroDIYAVRBoards/](https://github.com/EnviroDIY/Arduino_boards/raw/master/EnviroDIYAVRBoards/).
The index for the Arduino Board Manager is available at [https://raw.githubusercontent.com/EnviroDIY/Arduino_boards/refs/heads/master/package_EnviroDIY_index.json](https://raw.githubusercontent.com/EnviroDIY/Arduino_boards/refs/heads/master/package_EnviroDIY_index.json).

All boards in this package compile with a compile-time package-version macro of  `ENVIRODIY_ATMEGA_BOARDS`.
You can use this macro in your sketches to check the package version at compile time, for example:

```cpp
#if defined(ENVIRODIY_ATMEGA_BOARDS)
  Serial.println(ENVIRODIY_ATMEGA_BOARDS);
#endif
```

You can also check the package version at runtime by using the the macro:

```cpp
#if ENVIRODIY_ATMEGA_BOARDS_VERSION >= ENVIRODIY_ATMEGA_BOARDS_VERSION_VAL(4, 0, 0)
  Serial.println(ENVIRODIY_ATMEGA_BOARDS_VERSION);
#endif
```

For each individual board, you can check the compiled variant version at compile time using the the same macro code with the board-specific define name in place of the package define name.

Boards included in this package:

| Board               | Version | Chip variant | `BOARD_DEFINE_NAME`    |
| ------------------- | ------- | ------------ | ---------------------- |
| EnviroDIY Mayfly    | 1.1.0-b | ATMEGA1284p  | `AVR_ENVIRODIY_MAYFLY` |
| EnviroDIY Mayfly v2 | 2.0.1   | ATMEGA1284p  | `AVR_ENVIRODIY_MAYFLY` |

> [!note]
> All versions of the EnviroDIY Mayfly prior to 1.1 rev B can be used identically with the 1.1 rev B version in the Arduino IDE.

This package was built using tools from [Sara Damiano's fork](https://github.com/SRGDamia1/AVR-custom-board) of [shurik179's SAMD-custom-board repository](https://github.com/shurik179/SAMD-custom-board).
