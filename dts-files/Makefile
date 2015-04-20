
DTC=../../zynq-boot/bin/dtc

zynq-zed-fmcomms2-df.dtb:
	arm-linux-gnueabi-gcc -E -nostdinc -I. -undef -D__DTS__ -x assembler-with-cpp -o zynq-zed-fmcomms2-df.dts.tmp zynq-zed-fmcomms2-df.dts
	$(DTC) -I dts -O dtb -o zynq-zed-fmcomms2-df.dtb zynq-zed-fmcomms2-df.dts.tmp
	cp zynq-zed-fmcomms2-df.dtb ../zynq-zed-fmcomms2-df/devicetree.dtb
