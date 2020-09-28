# peta_linux_commnads
petalinux commands

# Create Project
``` petalinux-create --type project --template zynq --name peta_lnx_final```


# Import hardware config
```petalinux-config --get-hw-description=petalinux-config --get-hw-description=/home/chaitusvk/Documents/final_testing/petalinux_int_base/petalinux_int_base.sdk/design_1_wrapper_hw_platform_0 ```

# Build
 petalinux-build
 petalinux-build -c rootfs
 petalinux-build -c kernel 

# create Module
petalnux-create -t modules -n simmod --enable

# Create App
```petalinux-create -t apps --template c --name hellosim```

# Package
``` petalinux-package --boot --fsbl images/linux/zynq_fsbl.elf --fpga project-spec/hw-description/design_1_wrapper.bit --uboot --force ```
