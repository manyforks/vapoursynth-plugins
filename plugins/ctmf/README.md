Description
================

Median filter for VapourSynth.

Ported from https://nomis80.org/ctmf.html

Usage
=====

    ctmf.CTMF(clip clip[, int radius=2, int memsize=1048576, int opt=0, int[] planes])

* clip: Clip to process. Any planar format with integer sample type of 8, 10, 12, 14 and 16 bit depth is supported.

* radius: Median filter radius. The kernel will be a 2\*radius+1 by 2\*radius+1 square. The maximum value is 127.

* memsize: Maximum amount of memory to use, in bytes. Set this to the size of the L2 or L3 cache, then vary it slightly and measure the processing time to find the optimal value. For example, a 512 KB L2 cache would have memsize=512*1024 initially.

* opt: Sets which cpu optimizations to use.
  * 0 = auto detect
  * 1 = use c
  * 2 = use sse2
  * 3 = use avx2

* planes: A list of the planes to process. By default all planes are processed.
