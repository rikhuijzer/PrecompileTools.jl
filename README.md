# PrecompileTools

[![Stable](https://img.shields.io/badge/docs-stable-blue.svg)](https://JuliaLang.github.io/PrecompileTools.jl/stable/)
[![Build Status](https://github.com/JuliaLang/PrecompileTools.jl/actions/workflows/CI.yml/badge.svg?branch=main)](https://github.com/JuliaLang/PrecompileTools.jl/actions/workflows/CI.yml?query=branch%3Amain)
[![Coverage](https://codecov.io/gh/JuliaLang/PrecompileTools.jl/branch/main/graph/badge.svg)](https://codecov.io/gh/JuliaLang/PrecompileTools.jl)

PrecompileTools allows you to reduce the latency of the first execution of Julia code.
**It is applicable for package developers and for "ordinary users" in their personal workflows.**

To learn how to use PrecompileTools, see the [documentation](https://JuliaLang.github.io/PrecompileTools.jl/stable/).

## PrecompileTools and PackageCompiler

Particularly on Julia 1.9 and higher, PrecompileTools allows dramatic reduction in "time to first execution" (TTFX).
In this respect, it shares goals with (and performs similarly to) [PackageCompiler](https://github.com/JuliaLang/PackageCompiler.jl).
Nevertheless, the two are not identical:

- only PrecompileTools can be used by *package developers* to ensure a better out-of-box experience for your users
- only PrecompileTools allows you to update your packages without needing to rebuild Julia
- only PackageCompiler dramatically speeds up loading time (i.e., `using ...`) for all the packages

## History (origins as SnoopPrecompile)

PrecompileTools is the successor to [SnoopPrecompile](https://github.com/timholy/SnoopCompile.jl/tree/master/SnoopPrecompile).
PrecompileTools differs in naming and in how one disables precompilation, but is otherwise a drop-in replacement.
