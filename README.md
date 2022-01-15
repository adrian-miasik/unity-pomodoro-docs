<h1 align="center">Unity Pomodoro Documentation</h1>

<h2 align="center">https://adrian-miasik.github.io/unity-pomodoro-docs/</h2>

### How to generate & publish the most up-to-date docs
1. Update the unity-pomodoro submodule using command: `git submodule update --remote --merge`.
2. Navigate into the `.\docfx_project\` directory. 
3. Run command `docfx` to build the latest docs. If you'd like to preview the docs locally run this command with the `--serve` option as such: `docfx --serve`. You will be able to preview the docs via local host, see console output.
4. Stage and push your updated submodule and `docs` folder to git. (Ideally follow gitflow, only changes to the `\master` get uploaded to our site via GitHub pages)
