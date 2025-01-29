# KnightOS Toolchain

This is the KnightOS toolchain.

## Overview

> Note:
> This is still heavily work in progress, most is just planning and hasn't actually been started.
>
> Currently I'm working on a Swift version of the package manager (used to be Python) to get a better understanding of the required internals.
> I'll migrate to C libraries and CLI tools once its done.

The philosphy (purely for fun) is that the toolchain ***can*** be self-contained.
That means the eventual goal is that no tools outside of it would be required for the entire development process -- be it developing the toolchain, kernel, OS or app.

### Applications

- term `KnightOS Studio`:
	This is a development environment for the KnightOS toolchain.
	
	I plan to only support macOS natively, possibly also iPadOS.
	You can use other IDEs, text editors and the CLI tools for cross-platform development.

- term `KnightOS Simulator`:
	This is the simulator for Ti calculators.
	
	I plan to only support macOS natively, possibly also iPadOS and iOS.
	You can use `ksim` (*formely `z80e`*) for cross-platform development.

### Command Line Tools

- term `ksdk` `kpm`? `knightos`?:
	This is the package manager for the toolchain, it lets you develop and install packages.
	
	It lets you develop and test using your installed KnightOS SDKs.

	- Templating (`init`)
	- Manifest Editing (`install`, `uninstall`)
	- Development (`build`, `test`, `docs`, `run`)
	- Dependency Management (`resolve`, `update`)
	- Publishing (`pack`, `publish`)
	- Manage KnightOS SDKs/toolchains (`sdk`/`toolchain`?)

- term `klib`:
	This is a library with shared functionality.
	
	The C toolchain includes `klibcmd`.
	
	The Swift toolchain includes `BinaryCodable` and `Json`.

- term `kas`:
	*Formerly saas or scas.*
	
	Assembler for Ti calculators.
	
- term `kcc`:
	C compiler for Ti calculators.
	
- term `kcppc`:
	C++ compiler for Ti calculators.
	
- term `kpy`:
	Python compiler for Ti calculators.
	
- term `kfc`:
	Functional language compiler for Ti calculators.

- term `kdoc`:
	*Formerly generated documentation from assembly projects.*

	Compiles (`build`) and manipulates documentation archives (`merge`, `augment`, `strip`, `publish`).
	Supports multiple modules, projects and languages (both programming and regular).

- term `kfs`:
	*Formerly genkfs*
	
	Specialized tool to manipulate KnightOS file systems.

- term `kimg`:
	Specialized tool to convert images to a format optimized for the target calculator.

- term `kpkg`:
	*Formerly kpack*
	
	Specialized tool to manipulate packages with commands such as `describe`, `extract`, `pack` and `stub`.

- term `krom`:
	*Formerly mkrom and patchrom*

	Specialized tool to create and manipulate roms with commands such as `create` and `patch`.

- term `ksign`:
	*Formerly mktiupgrade*
	
	Specialized tool to produce and sign OS upgrades for Ti calculators.

- term `ksim`:
	*Formerly z80e*
	
	Simulator for the supported Ti calculators.

## Help, Bugs, Feedback

If you need help with KnightOS, want to keep up with progress, chat with
developers, or ask any other questions about KnightOS, you can hang out in the
IRC channel: [#knightos on irc.freenode.net](http://webchat.freenode.net/?channels=knightos).
 
To report bugs, please create [a GitHub issue](https://github.com/KnightOS/KnightOS/issues/new) or contact us on IRC.
 
If you'd like to contribute to the project, please see the [contribution guidelines](http://www.knightos.org/contributing).
