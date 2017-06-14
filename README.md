# elixir-packages
Idiomatic elixir packages

# What is an idiomatic Elixir package?

This is a complex answer. Here are the hard-and-fast rules. There will be exceptions, but when in doubt, these are likely to all be true:

1. It fulfills a clear function, too complex to warrant building within one's own system
2. It prefers returning `{:error, :description_of_error` over raising an exception
3. It does not provide `use MyPackage`
4. It limits the amount of macros that leak into the system outside of the package's API
5. It provides support for the relevant Elixir `Protocol`, such as `Inspect`
