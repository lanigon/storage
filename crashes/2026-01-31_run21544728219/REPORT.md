# Fuzzing Crash Report

- **Date**: 2026-01-31 16:56:34 UTC
- **Repository**: lanigon/goeth
- **Branch**: main
- **Commit**: f38d3aad0adf5699830bc7745d76a40372a19e53
- **Run ID**: [21544728219](https://github.com/lanigon/goeth/actions/runs/21544728219)
- **Sanitizer**: address
- **Fuzz Duration**: 14400s

## Crashes Found

### rangeproof / crash-91ec98552831623b18d1d349c4ed4ea0666c5b74

```
/github/workspace/build-out/fuzz_rangeproof -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmp26r8frhf/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_rangeproof >fuzz-0.log 2>&1
/github/workspace/build-out/fuzz_rangeproof -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmp26r8frhf/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_rangeproof >fuzz-1.log 2>&1
/github/workspace/build-out/fuzz_rangeproof -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmp26r8frhf/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_rangeproof >fuzz-2.log 2>&1
/github/workspace/build-out/fuzz_rangeproof -timeout=25 -rss_limit_mb=2560 -len_control=0 -artifact_prefix=/tmp/tmp26r8frhf/ -max_total_time=464 -print_final_stats=1 /github/workspace/cifuzz-corpus/fuzz_rangeproof >fuzz-3.log 2>&1
================== Job 2 exited with exit code 77 ============
INFO: Running with entropic power schedule (0xFF, 100).
INFO: Seed: 416417057
INFO: Loaded 1 modules   (23195 inline 8-bit counters): 23195 [0x55affc9bbbc0, 0x55affc9c165b), 
INFO: Loaded 1 PC tables (23195 PCs): 23195 [0x10c000080000,0x10c0000da9b0), 
INFO:      899 files found in /github/workspace/cifuzz-corpus/fuzz_rangeproof
INFO: -max_len is not provided; libFuzzer will not generate inputs larger than 4096 bytes
INFO: seed corpus: files: 899 min: 1b max: 4092b total: 933463b rss: 52Mb
#128	pulse  cov: 1060 ft: 2718 corp: 93/9254b exec/s: 42 rss: 58Mb
#256	pulse  cov: 1102 ft: 3588 corp: 187/19Kb exec/s: 51 rss: 60Mb
#512	pulse  cov: 1126 ft: 4719 corp: 347/69Kb exec/s: 42 rss: 64Mb
#903	INITED cov: 1136 ft: 5626 corp: 511/362Kb exec/s: 14 rss: 75Mb
#936	NEW    cov: 1136 ft: 5627 corp: 512/362Kb lim: 4096 exec/s: 15 rss: 75Mb L: 872/4092 MS: 3 CopyPart-ChangeASCIIInt-CrossOver-
#938	NEW    cov: 1136 ft: 5641 corp: 513/366Kb lim: 4096 exec/s: 14 rss: 75Mb L: 3907/4092 MS: 2 CrossOver-EraseBytes-
#1024	pulse  cov: 1136 ft: 5645 corp: 514/367Kb lim: 4096 exec/s: 14 rss: 78Mb
#1328	RELOAD cov: 1136 ft: 5651 corp: 518/374Kb lim: 4096 exec/s: 13 rss: 78Mb
#1336	NEW    cov: 1136 ft: 5652 corp: 519/376Kb lim: 4096 exec/s: 13 rss: 78Mb L: 1395/4092 MS: 3 CrossOver-InsertByte-CopyPart-
#1397	NEW    cov: 1136 ft: 5653 corp: 520/378Kb lim: 4096 exec/s: 14 rss: 78Mb L: 2445/4092 MS: 1 EraseBytes-
runtime: g2: frame.sp=0x10c000050788 top=0x10c0000507e0
	stack=[0x10c000050000-0x10c000050800
fatal error: traceback did not unwind completely

runtime stack:
runtime.throw({0x55affb63fed3?, 0x0?})
	runtime/panic.go:1094 +0x4a fp=0x7b7e129fea20 sp=0x7b7e129fe9f0 pc=0x55affbaff10a
runtime.(*unwinder).finishInternal(0x0?)
	runtime/traceback.go:566 +0x12a fp=0x7b7e129fea60 sp=0x7b7e129fea20 pc=0x55affbaedd0a
runtime.(*unwinder).next(0x7b7e129feb10?)
	runtime/traceback.go:447 +0x232 fp=0x7b7e129fead8 sp=0x7b7e129fea60 pc=0x55affbaedb12
runtime.scanstack(0x10c000002e00, 0x10c000045e50)
	runtime/mgcmark.go:924 +0x2c9 fp=0x7b7e129febf0 sp=0x7b7e129fead8 pc=0x55affbaaf869
runtime.markroot.func1()
	runtime/mgcmark.go:248 +0xb1 fp=0x7b7e129fec40 sp=0x7b7e129febf0 pc=0x55affbaae191
runtime.markroot(0x10c000045e50, 0x18, 0x1)
	runtime/mgcmark.go:222 +0x1a5 fp=0x7b7e129fecf0 sp=0x7b7e129fec40 pc=0x55affbaadde5
runtime.gcDrain(0x10c000045e50, 0x7)
	runtime/mgcmark.go:1206 +0x3d3 fp=0x7b7e129fed58 sp=0x7b7e129fecf0 pc=0x55affbab02d3
runtime.gcDrainMarkWorkerIdle(...)
	runtime/mgcmark.go:1120
runtime.gcBgMarkWorker.func2()
	runtime/mgc.go:1560 +0x67 fp=0x7b7e129feda8 sp=0x7b7e129fed58 pc=0x55affbaac447
runtime.systemstack(0x55affbb09445)
	runtime/asm_amd64.s:513 +0x47 fp=0x7b7e129fedb8 sp=0x7b7e129feda8 pc=0x55affbb04947

goroutine 35 gp=0x10c000202540 m=0 mp=0x55affc985d00 [GC worker (active)]:
runtime.systemstack_switch()
```

