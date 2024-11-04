# iVim

This a repository with a sample config that provides all features required to develop iOS and macOS apps in Neovim, forked from [wojciech-kulik/ios-dev-starter-nvim](https://github.com/wojciech-kulik/ios-dev-starter-nvim).

## Requirements

- [codelldb](https://github.com/vadimcn/codelldb/releases) - download latest release for DARWIN and unzip `vsix` file. Then make sure that the path in `nvim-dap.lua` points to this folder
- [Xcodeproj](https://github.com/CocoaPods/Xcodeproj) - to manage Xcode project file
- [xcode-build-server](https://github.com/SolaWing/xcode-build-server) - build your project in Xcode, clone the repository, unzip, and run this tool for your project
- [pymobiledevice3](https://github.com/doronz88/pymobiledevice3) - to debug on physical devices and/or run apps on devices below iOS 17
- [SwiftLint](https://github.com/realm/SwiftLint) - code linter
- [SwiftFormat](https://github.com/nicklockwood/SwiftFormat) - code formatter
- [xcbeautify](https://github.com/cpisciotta/xcbeautify) - Xcode logs formatter
- [luarocks](https://luarocks.org) - Lua package manager

## Installation

Please make sure to install all dependencies and get familiar with [xcodebuild.nvim](https://github.com/wojciech-kulik/xcodebuild.nvim):

```
brew install xcode-build-server
brew install xcbeautify
brew install swiftlint
brew install luarocks
brew install swiftformat
brew install ruby
gem install xcodeproj
python3 -m pip install -U pymobiledevice3
```

Then, you will need to clone this repository:
```
git clone https://github.com/thigcampos/ivim ˜/.config/ivim
```

Finally, add an alias to make it easier to launch this setup:
```
alias ivim='NVIM_APPNAME=ivim nvim'
```

## Key Bindings

`<leader>` = `space`

- `<leader>X` - open `xcodebuild.nvim` picker with project actions
- `<leader>xf` - to open Project Manager and manage files
- `<leader>dd` - build, run & debug app
- `<leader>dt` - debug tests
- `<leader>xr` - build & run
- `<leader>xb` - build project
- `<leader>xt` - run tests
- `<leader>xc` - toggle code coverage
- `<leader>xC` - show code coverage report
- `<leader>b` - toggle breakpoint
- `<leader>e` - nvim-tree
- `<leader>fg` - Telescope grep
- `<leader>ff` - Telescope find file
- `<leader>tt` - toggle Trouble

## More Info

This repository is based on a complementary project for Wojciech's blog post: [The Complete Guide To iOS & macOS Development In Neovim](https://wojciechkulik.pl/ios/the-complete-guide-to-ios-macos-development-in-neovim).

Please read it to learn how to use this config.
