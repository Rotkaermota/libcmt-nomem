Just include this file in your project to use dlmalloc anywhere<br />
also, don't forget to activate "Ignore Specific Default Libraries" "libcmt" in linker options (Configuration Properties->Linker->Input)<br />
to obtain libcmt_nomem.lib<br />
- download grep from unix tools
- run **make_libcmt_nomem.cmd**
- wait
- put libcmt_nomem.lib to your project

bonus: spin lock instead of CriticalSection for crt syncronizations

example (in any cpp file of your project):

\#ifdef _USE_DLMALLOC_ANYWHERE<br />
\#include "crtfunc.h"<br />
\#endif<br />
