# mechanical-arm

调试的时候时刻记得 需要把路径添加到检索中

//#########################################

F2802x_Headers_nonBIOS.cmd
F28027.cmd
28027_RAM_Ink.cmd

当烧录到flash中时需要

extern Uint16 RamfuncsLoadStart;
extern Uint16 RamfuncsLoadEnd;
extern Uint16 RamfuncsRunStart;
extern Uint16 RamfuncsLoadSize;

 memcpy(&RamfuncsRunStart, &RamfuncsLoadStart, (size_t)&RamfuncsLoadSize);
       InitFlash();


****************************************************************
