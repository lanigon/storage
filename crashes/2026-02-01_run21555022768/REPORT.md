# Fuzzing Crash Report

- **Date**: 2026-02-01 06:35:18 UTC
- **Repository**: lanigon/goeth
- **Branch**: main
- **Commit**: f38d3aad0adf5699830bc7745d76a40372a19e53
- **Run ID**: [21555022768](https://github.com/lanigon/goeth/actions/runs/21555022768)
- **Sanitizer**: address
- **Fuzz Duration**: 14400s

## Crashes Found

### bls12381_cross_pairing / crash-38aee02949d2a5fa2207bd2429ff58687b18aea1

```
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmppvqxu50y/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-0.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmppvqxu50y/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-3.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmppvqxu50y/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-2.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmppvqxu50y/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-1.log 2>&1
================== Job 0 exited with exit code 77 ============
INFO: Running with entropic power schedule (0xFF, 100).
INFO: Seed: 1372502407
INFO: Loaded 1 modules   (25703 inline 8-bit counters): 25703 [0x56248a4a0580, 0x56248a4a69e7), 
INFO: Loaded 1 PC tables (25703 PCs): 25703 [0x10c000080000,0x10c0000e4670), 
INFO:      134 files found in /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing
INFO: -max_len is not provided; libFuzzer will not generate inputs larger than 4096 bytes
INFO: seed corpus: files: 134 min: 1b max: 2984b total: 31333b rss: 54Mb
#135	INITED cov: 637 ft: 1467 corp: 133/30Kb exec/s: 135 rss: 58Mb
#649	NEW    cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 649 rss: 61Mb L: 2218/2984 MS: 4 ShuffleBytes-ShuffleBytes-CrossOver-ShuffleBytes-
#1024	pulse  cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 512 rss: 64Mb
#2048	pulse  cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 682 rss: 64Mb
#4096	pulse  cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 682 rss: 65Mb
#8192	pulse  cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 682 rss: 67Mb
#16384	pulse  cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 682 rss: 71Mb
#32768	pulse  cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 697 rss: 76Mb
#65536	pulse  cov: 637 ft: 1468 corp: 134/32Kb lim: 4096 exec/s: 697 rss: 77Mb
runtime: marked free object in span 0x7b8764323fe0, elemsize=32 freeindex=0 (bad use of unsafe.Pointer or having race conditions? try -d=checkptr or -race)
0x10c000322000 free  unmarked
0x10c000322020 alloc marked  
0x10c000322040 free  unmarked
0x10c000322060 alloc marked  
0x10c000322080 free  unmarked
0x10c0003220a0 alloc marked  
0x10c0003220c0 free  unmarked
0x10c0003220e0 alloc marked  
0x10c000322100 free  unmarked
0x10c000322120 alloc marked  
0x10c000322140 free  unmarked
0x10c000322160 alloc marked  
0x10c000322180 free  unmarked
0x10c0003221a0 alloc marked  
0x10c0003221c0 free  unmarked
0x10c0003221e0 alloc marked  
0x10c000322200 free  unmarked
0x10c000322220 alloc marked  
0x10c000322240 free  unmarked
0x10c000322260 alloc marked  
0x10c000322280 free  unmarked
0x10c0003222a0 alloc marked  
0x10c0003222c0 free  unmarked
0x10c0003222e0 alloc marked  
0x10c000322300 free  unmarked
0x10c000322320 alloc marked  
0x10c000322340 free  unmarked
0x10c000322360 alloc marked  
```

