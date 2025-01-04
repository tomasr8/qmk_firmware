# Compile

(VIAL and VIA should be disabled or it fails to flash sometimes(??))

```sh
qmk compile -kb 6064 -km 6064
```

# Original source

https://drive.google.com/file/d/1ITLFKa0Kzlj4HhlbY98qWxQ7V3ojB_72/view?spm=a2g0s.imconversation.0.0.254d3e5fEsGe25&usp=sharing


# Flashing and debugging

This uses the tinyuf2 bootloader. First reset the keyboard with FN+ESC or by
shorting the pins close to the chip. This will add the keyboard as external
storage. Compile the firmware and rename it to `CURRENT.UF2`. Copy this to the
mass storage (replacing the old firmware). Reconnect the keyboard and everything
should work.

If the firmware gets borked short the reset pins and the boot0 pins (on the
other side of the board). This should load the original firmware from ROM. After
that, connect the board again and short the reset pins again for a few seconds
which should add the board as external storage.
