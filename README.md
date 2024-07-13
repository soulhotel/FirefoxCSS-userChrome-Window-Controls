## This Repository serves as a resource file for the FirefoxCSS community.
###### Specifically for theme creators who attempt to create one-line navigation bars by removing the titlebar, thus losing access to Window Control Buttons.

### `return-window-controls.css`

The premise, is a 1 file solution to return Window Controls through one management file; With additional compatibility for linux and mac users.

To use this resource file, simply `import` it within the `userchrome.css` of your theme. And place the return-window-controls.css in an appropriate directory.

### Key notes.
- Mac OS compatibility is automatically handled through an OS media query.
- Linux compatibility should require the user to apply a `user.js` file.
  - Linux compatibility is dependant on several factors such as DE and window decoration/theme application.
  - To treat this, they have 3 options within `user.js` + `about:config` to select what their DE is, and filter through different positioning setups.
  - Linux users should be comfortable enough with this process, due to the terminal centric nature of the OS.
  - Or the theme creator can supply seperate modified return-window-control.css files for the linux users, but this approach is work for the creator.
- The #navigator-toolbox element is enforced to be the --toolbar-bgcolor variable.
  - For creators that alter the navigation bar color, you can simple add that main background color to --toolbar-bgcolor.
  - If you alter the navigation bar to be rgb(15,15,15) or to be var(--my-custom-variable), simply set --toolbar-bgcolor as `--toolbar-bgcolor: var(--my-custom-variable) !important` or `--toolbar-bgcolor: rgb(15,15,15) !important`.

