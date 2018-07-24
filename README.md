# dt_ideas

## Tray Loading

### Splice Auto-Loading

There is some support for auto-loading trays into splices in the latest FTTH.

The core method here is `ftth_splice_and_load_mixin.load_pins(pins_to_load)`.  This input `pins_to_load` is a vector of two elements that is structured as `{pins_to_splice, trays}`.

The problem with this code is that it loads the trays sequentially.  The only customisation point is the method `ftth_splice_and_load_mixin.custom_get_tray_holders(tray)` that allows some of the trays to be left empty, but it is not sufficient for DT.



### Tray Loading API

There are a number of core methods that should be used when loading trays:

- 
