# elixir-packages
Packages I recommend to get things done.

# How does an Elixir package qualify?

Here are the guidelines:

1. It fulfills a clear function, too complex to warrant building within one's own system
2. It prefers returning `{:error, :description_of_error}` over raising an exception
3. It does not provide `use MyPackage` unless there is a warranted use for it.
4. It limits the amount of macros that leak into the system outside of the package's API
5. [ Maybe NOT -- because only for opaques! We lose pastability otherwise! ] It provides support for the relevant Elixir `Protocol`, such as `Inspect`
6. It respects [semantic versioning](http://semver.org/)
8. It provides an introduction to the package in the hex-level top documentation
9. It has hex-level documentation for the public interface
10. The public interface is limited
11. The internal interface is not documented in hex
12. It has an up-to-date CHANGELOG
13. It has tests
14. It has a small set of dependencies
15. I found it usable.
