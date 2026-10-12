ZMK configuration for all my keyboards.  
Many share one unified keymap (config/include/base_keymap.dtsi)—ravine, metasepia, & metasepia2.  
  
The way this works:  
1. `keyboard.keymap` imports `keyboard.dtsi`;
2. `keyboard.dtsi` imports `base_keymap`, a keymap for a theoretical 14x4 board;
3. `keyboard.dtsi` trims down the 14x4 layout to match `keyboard`'s real layout, such as 23332+2;
4. `keyboard.keymap` now contains a keymap that fits `keyboard`.  
This `.keymap` file is what gets processed when making the firmware.
