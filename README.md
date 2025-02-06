<div align="center">
  <h1><code>setup-rokit</code></h1>
  <p>
    <a href="https://github.com/raild3x/setup-rokit/actions?query=workflow%3Atest"><img src="https://github.com/raild3x/setup-rokit/workflows/test/badge.svg" alt="CI" /></a>
  </p>
</div>

GitHub action to install and run [rokit](https://github.com/rojo-rbx/rokit); a toolchain manager.

## Usage
Use the latest released version of `rokit` with default parameters:
```yaml
steps:
- uses: raild3x/setup-rokit@v0.1.0
```
For a list of default parameter values, [check here](https://github.com/raild3x/setup-rokit/blob/main/action.yml#L5-L20).

### Advanced Usage
For more advanced cases, use the parameters below.
```yaml
steps:
- uses: raild3x/setup-rokit@v0.1.0
  with:
    version: v1.0.0 # name of git tag in rokit (uses latest by default)
    path: some_dir/my_project # path to project dir containing `rokit.toml` (uses current dir by default)
    cache: "false" # whether to enable binary caching between runs (false by default)
    token: ${{ github.token }} # GitHub token to bypass rate limit (passed by default)
```

## Credits
[@ok-nick](https://github.com/ok-nick) - Writing the original aftman installer workflow

[@nezuo](https://github.com/nezuo) - Installing `rokit` using `gh`