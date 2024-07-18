## This Repository serves as a resource file for the FirefoxCSS community.

The premise of this repository, is a solution - for theme creators who attempt to create one-line navigation-bar themes. These themes typically remove the titlebar, thus losing access to Window Control Buttons. We can solve this through the use of a management file; With additional compatibility for linux and mac users.

### <ins>return-window-controls.css</ins>

To use this in your theme:
>
1 - Import the file into your theme's userChrome.css
>
2 - Place return-window-controls.css in an appropriate directory.

![2024-07-13_16-09](https://github.com/user-attachments/assets/9e041cb3-e560-477f-b4d3-5e10a5849761)


### <ins>Additional Information</ins>
- Mac OS compatibility is automatically handled through an OS media query.
- Linux compatibility should require the user to apply a `user.js` file.
  - Linux compatibility is dependant on several factors such as DE and window decoration/theme application.
  - To treat this, they have 3 options within `user.js` + `about:config` to select what their DE is, and filter through different positioning setups.
  - Linux users should be comfortable enough with this process, due to the terminal centric nature of the Operating Systems.
  - The theme creator could also supply seperate modified return-window-control.css files for the linux users, but this approach is unnecesary work for the creator.
- The #navigator-toolbox element is enforced to use the --toolbar-bgcolor variable as it's background color.
  - For creators that alter the navigation bar color, you can simply apple the color to --toolbar-bgcolor as well.
  - Example: If you alter the navigation bar to be rgb(15,15,15) or to be var(--my-custom-variable), simply set --toolbar-bgcolor as `--toolbar-bgcolor: var(--my-custom-variable) !important` or `--toolbar-bgcolor: rgb(15,15,15) !important`.
