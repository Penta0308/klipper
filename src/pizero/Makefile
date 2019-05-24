# Additional pizero build rules

dirs-y += src/pizero src/generic

src-y += pizero/main.c pizero/timer.c pizero/console.c pizero/watchdog.c
src-y += pizero/pca9685.c pizero/spidev.c pizero/analog.c pizero/hard_pwm.c
src-y += generic/crc16_ccitt.c generic/alloc.c

lnk-y += bcm2835

CFLAGS_klipper.elf += -lutil

flash: $(OUT)klipper.elf
	@echo "  Flashing"
	$(Q)sudo ./scripts/flash-pizero.sh
