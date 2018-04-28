# ion-win32
Ion bindings for win32 functions

# Usage

Copy the 'win32' folder to your `$IONHOME/system_packages` directory or add it to your `$IONPATH`

Then in your .ion file:

```
import win32 { ... };

func init_vt_console()
{
	out: HANDLE = GetStdHandle(STD_OUTPUT_HANDLE);
	mode: DWORD = 0;
	GetConsoleMode(out, &mode);

	mode |= ENABLE_VIRTUAL_TERMINAL_PROCESSING;
	SetConsoleMode(out, mode);
}

```
