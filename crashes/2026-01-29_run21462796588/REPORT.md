# Fuzzing Crash Report

- **Date**: 2026-01-29 06:10:36 UTC
- **Repository**: lanigon/goeth
- **Branch**: main
- **Commit**: f38d3aad0adf5699830bc7745d76a40372a19e53
- **Run ID**: [21462796588](https://github.com/lanigon/goeth/actions/runs/21462796588)
- **Sanitizer**: address
- **Fuzz Duration**: 14400s

## Crashes Found

### bls12381_cross_pairing / crash-a7194d54c7a7d9bcae3c8aecb8edc38bd62364df

```
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpu5ypbf26/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-1.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpu5ypbf26/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-0.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpu5ypbf26/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-2.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpu5ypbf26/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-3.log 2>&1
================== Job 2 exited with exit code 77 ============
INFO: Running with entropic power schedule (0xFF, 100).
INFO: Seed: 2672138834
INFO: Loaded 1 modules   (25703 inline 8-bit counters): 25703 [0x5559612ad580, 0x5559612b39e7), 
INFO: Loaded 1 PC tables (25703 PCs): 25703 [0x10c000080000,0x10c0000e4670), 
INFO:      136 files found in /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing
INFO: -max_len is not provided; libFuzzer will not generate inputs larger than 4096 bytes
INFO: seed corpus: files: 136 min: 1b max: 2984b total: 33746b rss: 52Mb
#137	INITED cov: 637 ft: 1467 corp: 134/32Kb exec/s: 137 rss: 56Mb
#787	NEW    cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 787 rss: 60Mb L: 1124/2984 MS: 5 ChangeByte-ChangeByte-ChangeByte-ChangeBinInt-InsertRepeatedBytes-
#1024	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 512 rss: 63Mb
#2048	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 682 rss: 63Mb
#4096	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 682 rss: 64Mb
#8192	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 682 rss: 66Mb
#16384	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 682 rss: 71Mb
#32768	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 682 rss: 75Mb
#65536	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 689 rss: 76Mb
#115731	REDUCE cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 697 rss: 76Mb L: 54/2984 MS: 5 ChangeByte-InsertByte-EraseBytes-CopyPart-ChangeBinInt-
#131072	pulse  cov: 637 ft: 1468 corp: 135/33Kb lim: 4096 exec/s: 700 rss: 76Mb
runtime: marked free object in span 0x7b596ccb1dc0, elemsize=32 freeindex=0 (bad use of unsafe.Pointer or having race conditions? try -d=checkptr or -race)
0x10c000408000 free  unmarked
0x10c000408020 alloc marked  
0x10c000408040 alloc marked  
0x10c000408060 alloc marked  
0x10c000408080 free  unmarked
0x10c0004080a0 alloc marked  
0x10c0004080c0 alloc marked  
0x10c0004080e0 alloc marked  
0x10c000408100 free  unmarked
0x10c000408120 alloc marked  
0x10c000408140 alloc marked  
0x10c000408160 alloc marked  
0x10c000408180 free  unmarked
0x10c0004081a0 alloc marked  
0x10c0004081c0 alloc marked  
0x10c0004081e0 alloc marked  
0x10c000408200 free  unmarked
0x10c000408220 alloc marked  
0x10c000408240 alloc marked  
0x10c000408260 alloc marked  
0x10c000408280 free  unmarked
0x10c0004082a0 alloc marked  
0x10c0004082c0 alloc marked  
0x10c0004082e0 alloc marked  
0x10c000408300 free  unmarked
0x10c000408320 alloc marked  
```

