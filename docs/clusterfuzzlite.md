---
layout: default
title: ClusterFuzzLite
has_children: true
nav_order: 1
permalink: /
---

# ClusterFuzzLite
ClusterFuzzLite is a continuous [fuzzing] solution that runs as part of
[Continuous Integration (CI)] workflows to find vulnerabilities faster than ever
before.
With just a few lines of code, GitHub users can integrate ClusterFuzzLite into
their workflow and fuzz pull requests to catch bugs before they are committed.

ClusterFuzzLite is based on [ClusterFuzz].

## Features

- Quick code change (pull request) fuzzing to find bugs before they land
- Downloads of crashing testcases
- Continuous longer running fuzzing (batch fuzzing) to asynchronously find
   deeper bugs missed during code change fuzzing and build a corpus for
   use in code change fuzzing
- Coverage reports showing which parts of your code are fuzzed
- Modular funtionality, so you can decide which features you want to use

## Supported Languages
- C
- C++
- Java (and other JVM-based languages)
- Go
- Python
- Rust
- Swift

## Supported CI Systems
- [GitHub Actions]
- [Google Cloud Build]
- [Prow]
- Support for more CI systems is in-progess, and [extending support to other CI
  systems] is easy

## Supported Fuzzing Engine and Sanitizers

- [libFuzzer] for coverage-guided testing
- [AddressSanitizer] for finding memory safety issues
- [MemorySanitizer] for finding use of uninitialized memory
- [UndefinedBehaviorSanitizer] for finding undefined behavior (e.g. integer
  overflows)

## Getting Started

If you're new to using libFuzzer and sanitizers, start with the [Overview] for
an explanation of terms and the fuzzing process.

If you're already familiar with using libFuzzer and sanitizers, start with [Step
1: Build Integration].

## Staying in touch

Join our [mailing list] for announcements and discussions.

If you use ClusterFuzzLite, please fill out [this form] so we know who is using
it.
This gives us an idea of the impact of ClusterFuzzLite and allows us to
justify future work.

Please [file an issue] if you experience any trouble or have feature
requests.

[Continuous Integration (CI)]: https://en.wikipedia.org/wiki/Continuous_integration
[fuzzing]: {{ site.baseurl }}/overview.md#fuzzing
[ClusterFuzz]: https://google.github.io/clusterfuzz/
[GitHub Actions]: {{ site.baseurl }}/running-clusterfuzzlite/github-actions/
[Prow]: {{ site.baseurl }}/running-clusterfuzzlite/prow/
[Overview]: {{ site.baseurl }}/overview/
[Google Cloud Build]: {{ site.baseurl }}/running-clusterfuzzlite/google-cloud-build/
[extending support to other CI systems]:{{ site.baseurl }}/developing-clusterfuzzlite/new-platform/
[libFuzzer]: https://llvm.org/docs/LibFuzzer.html
[AddressSanitizer]: https://clang.llvm.org/docs/AddressSanitizer.html
[UndefinedBehaviorSanitizer]: https://clang.llvm.org/docs/UndefinedBehaviorSanitizer.html
[Step 1: Build Integration]: {{ site.baseurl }}/build-integration/
[Running ClusterFuzzLite]: {{ site.baseurl }}/running-clusterfuzzlite/
[Configuring ClusterFuzzLite to run in your CI]: {{ site.baseurl }}/running-clusterfuzzlite/
[MemorySanitizer]: https://clang.llvm.org/docs/MemorySanitizer.html
[mailing list]: https://groups.google.com/g/clusterfuzzlite-users
[this form]: https://docs.google.com/forms/d/e/1FAIpQLSdAKB03YM4HjMwNe1K4T6Yr16OE4lCMj-VzThuUOrZUc3ytWw/viewform?usp=sf_link
[file an issue]: https://github.com/google/clusterfuzzlite/issues/new
