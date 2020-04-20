# Xorg

## AMDGPU

### TearFree

You will have to create a file in `/etc/X11/xorg.conf.d/` and enable the `TearFree` option. To do so, follow the example:

```
/etc/X11/xorg.conf.d/99-amdgpu.conf
―――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――――
Section "Device"
     Identifier "AMD"
     Driver "amdgpu"
     Option "TearFree" "true"
  EndSection
```

Then, log back in, and enjoy the tear free rendering!


### FreeSync

#### Requirements

- For desktops, your must ensure that your [**monitor is compatible with FreeSync**](https://www.amd.com/en/products/freesync-monitors), as well that your [**GPU is compatible with FreeSync**](https://www.amd.com/en/technologies/free-sync-faq#faq-Which-products-support-AMD-FreeSync%E2%84%A2-technology?).

- For laptops, you must ensure that your [**laptop is compatible with FreeSync**](https://www.amd.com/en/products/freesync-laptops).

If you have the requirements, you can simply enable the `VariableRefresh` option. To do so, follow the example:

```
/etc/X11/xorg.conf.d/99-amdgpu.conf
Section "Device"
     Identifier "AMD"
     Driver "amdgpu"
     Option "VariableRefresh" "true"
  EndSection
```

Then, log back in, and enjoy your FreeSync enabled gaming!
