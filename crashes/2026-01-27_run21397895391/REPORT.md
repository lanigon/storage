# Fuzzing Crash Report

- **Date**: 2026-01-27 16:59:54 UTC
- **Repository**: lanigon/goeth
- **Branch**: main
- **Commit**: f38d3aad0adf5699830bc7745d76a40372a19e53
- **Run ID**: [21397895391](https://github.com/lanigon/goeth/actions/runs/21397895391)
- **Sanitizer**: address
- **Fuzz Duration**: 14400s

## Crashes Found

### bls12381_cross_pairing / crash-5e4b3ca0d62e9f80bbeec73723d4493e66303796

```
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpgt0vpgyk/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-2.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpgt0vpgyk/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-3.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpgt0vpgyk/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-1.log 2>&1
/github/workspace/build-out/fuzz_bls12381_cross_pairing -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmpgt0vpgyk/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing >fuzz-0.log 2>&1
================== Job 2 exited with exit code 77 ============
INFO: Running with entropic power schedule (0xFF, 100).
INFO: Seed: 1951756097
INFO: Loaded 1 modules   (25703 inline 8-bit counters): 25703 [0x5646a5527580, 0x5646a552d9e7), 
INFO: Loaded 1 PC tables (25703 PCs): 25703 [0x10c000080000,0x10c0000e4670), 
INFO:      157 files found in /github/workspace/cifuzz-corpus/fuzz_bls12381_cross_pairing
INFO: -max_len is not provided; libFuzzer will not generate inputs larger than 4096 bytes
INFO: seed corpus: files: 157 min: 1b max: 2984b total: 41429b rss: 50Mb
#158	INITED cov: 637 ft: 1467 corp: 134/32Kb exec/s: 158 rss: 55Mb
#632	NEW    cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 632 rss: 59Mb L: 465/2984 MS: 4 ChangeByte-CopyPart-CrossOver-EraseBytes-
#1024	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 512 rss: 62Mb
#2048	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 512 rss: 62Mb
#4096	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 585 rss: 63Mb
#8192	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 630 rss: 65Mb
#16384	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 655 rss: 69Mb
#32768	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 682 rss: 73Mb
#65536	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 689 rss: 74Mb
#131072	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 693 rss: 74Mb
#262144	pulse  cov: 637 ft: 1468 corp: 135/32Kb lim: 4096 exec/s: 688 rss: 75Mb
runtime: marked free object in span 0x7f2b9bf0d7d0, elemsize=32 freeindex=0 (bad use of unsafe.Pointer or having race conditions? try -d=checkptr or -race)
0x10c00029e000 alloc marked  
0x10c00029e020 free  unmarked
0x10c00029e040 alloc marked  
0x10c00029e060 free  unmarked
0x10c00029e080 alloc marked  
0x10c00029e0a0 free  unmarked
0x10c00029e0c0 alloc marked  
0x10c00029e0e0 free  unmarked
0x10c00029e100 alloc marked  
0x10c00029e120 free  unmarked
0x10c00029e140 alloc marked  
0x10c00029e160 free  unmarked
0x10c00029e180 alloc marked  
0x10c00029e1a0 free  unmarked
0x10c00029e1c0 alloc marked  
0x10c00029e1e0 free  unmarked
0x10c00029e200 alloc marked  
0x10c00029e220 free  unmarked
0x10c00029e240 alloc marked  
0x10c00029e260 free  unmarked
0x10c00029e280 alloc marked  
0x10c00029e2a0 free  unmarked
0x10c00029e2c0 free  marked   zombie
0x000010c00029e2c0:  0xf8b2f47577922da4  0x49c37c46f4fa97b6 
0x000010c00029e2d0:  0xead42bc5207ce75b  0x1e6197b9dc74448b 
0x10c00029e2e0 free  unmarked
```

