# Sublime Syntax highlighting for RISC OS CMHG files

A Sublime syntax definition for RISC OS CMHG to enable syntax highlighting.
This is suitable for use with CMHG files used by CMunge; it is a superset of the original CMHG file format.

## Colouring

The syntax colouring recognises the CMHG directives and their field names, as well
as the preprocessor directives (which must be enabled using the `-p` switch when invoking the
CMunge tool).

The coloured features are:

* Comments, prefixed by `;` at the start of a line.
* Preprocessor directives.
* CMHG directive names.
* CMHG directive field names.
* RISC OS style hex numbers (`&xxx`).


## File recognition

CMHG files usually live in the `cmhg` directory, and do not have any extension when filenames
are encoded on non-RISC OS filesystems. This is not supported by the Sublime Text extensions syntax, so it is recommended that the ApplySyntax package (or similar) be used to select the syntax mode.

The following configuration is suitable for use within `ApplySyntax.sublime-settings`:

```
        {
            // RISCOS CMHG files
            "syntax": "RISCOSCMHG/RISCOSCMHG",
            "rules": [
                {"file_path": ".*(\\\\|/)cmhg(\\\\|/)[^./]+$"},
            ]
        },
```


## Install manually

* Place the `RISCOSCMHG.sublime-syntax` file inside the Sublime Text packages User folder (`Preferences | Browse Packages...`)
* Restart Sublime Text


## Install with Package Control

* Install [Package Control](http://wbond.net/sublime_packages/package_control)
* Run “Package Control: Install Package” command, find and install `RISCOSCMHG` plugin.
* Restart Sublime Text if necessary

## License
This package is licensed under the MIT License.
