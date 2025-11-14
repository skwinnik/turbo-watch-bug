# Description
This is a minimal reproduction of a bug I'm seeing in my real project.

When running `pnpm turbo watch web#build`, the `web` package should rebuild when the `external.json` file changes, but it doesn't.
At the same time `pnpm turbo run web#build` works as expected. It rebuilds the `web` package when the `external.json` file changes upon running the command after changing the file.

# Steps to reproduce

1. Run `pnpm turbo watch web#build`
2. Change the `external.json` file
3. The `web` package should rebuild

# Expected behavior
`pnpm turbo watch web#build` should rebuild the `web` package when the `external.json` file changes.

# Actual behavior
`pnpm turbo watch web#build` does not rebuild the `web` package when the `external.json` file changes.