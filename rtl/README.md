## Hardware RTL Sources

### [`core`](https://github.com/stnolting/neorv32/tree/main/rtl/core)

This folder contains the core VHDL files for the NEORV32 CPU and the NEORV32 Processor.
When creating a new synthesis/simulation project make sure that all `*.vhd` files from this
folder are added to a **new design library** called `neorv32`.

:warning: The sub-folder [`core/mem`](https://github.com/stnolting/neorv32/tree/main/rtl/core/mem)
contains the _platform-agnostic_ VHDL architectures of the processor-internal memories.
These files can be replaced by platform-specific memory modules.

### [`legacy`](https://github.com/stnolting/neorv32/tree/main/rtl/legacy)

This folder contains RTL modules that were used in older versions of the processor and have
been deprecated or were never actually used. However, they might still be useful for building
custom processor setups.

### [`processor_templates`](https://github.com/stnolting/neorv32/tree/main/rtl/processor_templates)

Contains pre-configured "SoC" templates that instantiate the processor's top entity from `core`.
These templates can be instantiated directly within a FPGA-specific board wrapper.

### [`system_integration`](https://github.com/stnolting/neorv32/tree/main/rtl/system_integration)

Top entities in this folder provide the same peripheral/IO signals and configuration generics as
the default processor top entity from `core`, but featuring a different interface.

### [`test_setups`](https://github.com/stnolting/neorv32/tree/main/rtl/test_setups)

Minimal processor test setups (FPGA- and board-independent. See the
[README](https://github.com/stnolting/neorv32/tree/main/rtl/test_setups)
in that folder for more information. Note that these test setups are used in the
[NEORV32 User Guide](https://stnolting.github.io/neorv32/ug).
