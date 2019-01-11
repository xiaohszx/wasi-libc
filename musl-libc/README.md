This code is based on musl revision de7dc1318f493184b20f7661bc12b1829b957b67
from git://git.musl-libc.org/musl.

Whole files which are unused are omitted. Changes to upstream code are wrapped
in preprocessor directives controlled by the macro `__wasm_musl_unmodified_upstream__`.

Some major known missing areas include:
 - random
 - locales
 - threads
 - setjmp
 - signals
 - ipc
 - getenv
 - regex (because locales)
 - TIOCGWINSZ (because cloudabi lacks it; affects isatty, line buffering for stdout)
 - O\_CLOEXEC, O\_NOCTTY (because cloudabi lacks them)