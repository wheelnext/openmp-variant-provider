# openmp-variant-provider

This is a plugin for the proposed [wheel variants implementation](
https://github.com/wheelnext/pep_xxx_wheel_variants) that provides
OpenMP library selection.

This plugin always returns a fixed list of supported variants, and so
can be used as a build-time plugin.

## Usage

Namespace: `openmp`

Plugin API: `openmp_variant_provider` (can be inferred from `requires`)

Example use in `pyproject.toml`:

```toml
[variant.providers.openmp]
requires = ["openmp-variant-provider"]
plugin-use = "build"
```

## Provided properties
### openmp :: provider

Values: `gomp`, `iomp`, `llvmomp`

Indicates which OpenMP implementation is used.
