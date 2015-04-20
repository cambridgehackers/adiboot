
VIVADO=$(shell which vivado)
BOOTGEN=$(realpath $(shell dirname $(VIVADO))/../../../SDK/2014.4/bin/bootgen)

all: BOOT.BIN devicetree.dtb

devicetree.dtb: ../dts-files/zynq-zed-fmcomms2-df.dts
	(cd ../dts-files; make zynq-zed-fmcomms2-df.dtb)

BOOT.BIN: system_top.bit u-boot-zed.elf zynq_fsbl_0.elf
	ln -sf zynq_fsbl_0.elf fsbl.elf
	$(BOOTGEN) -image zynq.bif -o i BOOT.BIN -w on -log bootgen.log

