# FatFS file system, CMake version
## Feature introduction
 - Supports all MCUs with sufficient available memory
 - Follow official updates and modify to the CMake version
## Content to be implemented
 * Implement the following functions yourself
   ```bash
   DSTATUS SDCard_status(void);
   DSTATUS SDCard_initialize(void);
   DRESULT SDCard_read(BYTE *buff, LBA_t sector, UINT count);
   DRESULT SDCard_write(const BYTE *buff, LBA_t sector, UINT count);
   DRESULT SDCard_ioctl(BYTE cmd, void *buff);
   DWORD   get_fattime(void);
   ```
## How to use CMake
 - You can use submodules to associate with this repository
   ```bash
   git submodule add https://github.com/nczyw/fatfs.git fatfs
   ```
 - Add to the top-level CMake
   ```bash
   add_subdirectory("fatfs")
   ```