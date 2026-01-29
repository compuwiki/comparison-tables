
## Comparando Sistemas Operativos

| Column 1                            | Android                          | Linux (Desktop/Server + móvil)                                     | iOS/iPadOS              | Windows NT                     | macOS               | FreeBSD                   |
| ----------------------------------- | -------------------------------- | ------------------------------------------------------------------ | ----------------------- | ------------------------------ | ------------------- | ------------------------- |
| Número Estimado de Usuarios (aprox) | 3.9 B                            | 3.3 B                                                              | 1.6 B                   | 1.4 B                          | 0.4 B               | 0.05 B                    |
| Main Companies contributing         | Google                           | Linux F., Meta, Google, Huawei, Intel, Red Hat, Samsung, SUSE, IBM | Apple                   | Microsoft                      | Apple               | FreeBSD Core Team         |
| Kernel                              | Linux modificado                 | Linux monolítico                                                   | XNU híbrido             | NT híbrido                     | XNU híbrido         | FreeBSD monolítico        |
| Userland                            | Bionic libc                      | GNU                                                                | BSD                     | Win32/.NET                     | BSD                 | BSD                       |
| Gestión de Procesos                 | CFS+opt móvil                    | CFS                                                                | Mach                    | Scheduler NT                   | Mach+BSD            | ULE Scheduler             |
| Gestión de Memoria                  | LMK/zRAM                         | VM Linux                                                           | VM Mach agresiva        | VM NT                          | VM Mach             | VM BSD                    |
| Sistema de Archivos                 | ext4/F2FS                        | ext4/Btrfs/XFS                                                     | APFS                    | NTFS                           | APFS                | UFS/ZFS                   |
| Drivers                             | Kernel+HAL                       | Kernel modules                                                     | IOKit                   | WDM/KMDF                       | IOKit               | Kernel nativo BSD         |
| Seguridad                           | SELinux enforcing                | SELinux/AppArmor                                                   | Sandbox total           | ACL/UAC                        | SIP+sandbox         | Jails                     |
| Modelo de Apps                      | APK sandbox                      | Binarios nativos                                                   | Apps firmadas           | Ejecutables                    | Apps firmadas       | Ports/pkg                 |
| Entorno Gráfico                     | SurfaceFlinger                   | GNOME/KDE/Phosh/Lomiri                                             | UIKit                   | Explorer/WinUI                 | Quartz              | X11/Wayland               |
| Arquitecturas                       | ARM                              | x86/ARM/RISC-V                                                     | ARM                     | x86/ARM                        | ARM/x86             | x86/ARM                   |
| Compatibilidad Dispositivos         | Smartphone/Tablet/TV/Embedded    | Desktop/Smartphone/Tablet/TV/Embedded                              | Smartphone/Tablet       | Desktop/Laptop                 | Desktop/Laptop      | Desktop/Server/Embedded   |
| Gestor de Paquetes                  | Play Store/APK                   | apt/dnf/pacman                                                     | App Store               | Winget/Microsoft Store         | App Store           | pkg/ports                 |
| Bootloader                          | OEM bootloader/fastboot/recovery | GRUB/systemd-boot/LILO                                             | EFI+iBoot               | Windows Boot Manager/UEFI/BIOS | EFI+boot.efi/UEFI   | BIOS/UEFI/Boot0           |
| Áreas de Uso                        | Smartphones, tablets, TV         | Servidores, desktop, móvil alternativo                             | Smartphone/tablet Apple | Desktop, gaming, empresa       | Desktop profesional | Servidores, NAS, embedded |
| Número Variantes                    | ~10-15                           | ~300+~5-8                                                          | 1                       | 5                              | 1                   | 3                         |
| Versatilidad General                | 3/5                              | 5/5                                                                | 1/5                     | 3/5                            | 2/5                 | 2/5                       |
| Variantes                           |                                  |                                                                    |                         |                                |                     |                           |


## Tools

- [CSV to MD - ConvertCSV](https://www.convertcsv.com/csv-to-markdown.htm)