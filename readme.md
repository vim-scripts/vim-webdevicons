**NOTE: This is just a mirror, official repo is here: https://github.com/ryanoasis/vim-devicons**

<h1 align="center">
	<img src="https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/branding-logo.png" alt="vim-devicons">
</h1>
[![GitHub version][img-version-badge]][badge-version] [![Join the chat at https://gitter.im/ryanoasis/vim-devicons][img-gitter-badge]][badge-gitter] [![Flattr this git repo][img-flattr-badge]][badge-flattr]
***
| **[Screenshots](#screenshots)**| **[API](#api)** | **[Fonts ➶][patched-fonts]** | **[Patcher ➶][nerd-fonts]** |
|--------------------------------|-----------------|------------------------------|-----------------------------|
| [![screenshots][img-visual-toc-screenshots]](#screenshots) | [![api][img-visual-toc-api]](#api) | [![patcher-logo-small][img-visual-toc-patched-fonts]][patched-fonts] | [![patcher-logo-small][img-visual-toc-fonts-patcher]][nerd-fonts] |
***

Adds filetype glyphs (icons) to other plugins such as [NERDTree], [vim-airline], [CtrlP], [unite], [lightline.vim], [vimfiler], and [flagship].

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/overall-screenshot.png)


## Table of Contents

- [vim-devicons v0.5.4](#)
	- [Quick Setup (TL;DR)](#quick-setup)
	- [Usage](#usage)
	- [Font Configuration](#font-configuration)
	- [Font Installation](#font-installation)
	- [Screenshots](#screenshots)
	- [Features](#features)
	- [Extra Configuration](#extra-configuration)
		- [character mappings](#character-mappings)
	- [Installation](#installation)
	- [Lightline](#lightline.vim)
	- [Todo](#todo)
	- [FAQ / Troubleshooting](#faq--troubleshooting)
	- [Contributing](#contributing)
	- [Rationale](#rationale)
	- [Inspiration and special thanks](#inspiration-and-special-thanks)
	- [License](#license)


<a name="quick-setup"></a>
## Quick Setup (TL;DR)

1. Install the plugin per your usual method
   _[(» More details... «)](#installation)_
2. Download and install a patched font (or patch your own):
  * [nerd-fonts]
   _[(» More details... «)](#font-installation)_
3. Set font  _[(» More details... «)](#font-configuration)_
  * a. **vim**: Set your terminal emulator font
  * b. **gvim**: Set `guifont` in your `vimrc`

## Usage

After installing the patched font and setting the vim font just open or look at any of the supported plugins you have installed ([NERDTree][nerdtree], [airline][vim-airline], [unite], [lightline.vim], [vimfiler], or [flagship]).

* _NOTE:_ if you don't have `guifont` set and are not running gvim you will need to set the terminal font.

* _NOTE:_ for support of these plugins: [NERDTree], [vim-airline], [CtrlP], [unite], [vimfiler], [flagship] you **must** configure vim to load those plugins **_before_** vim-devicons loads.

* _NOTE:_ for better [nerdtree-git-plugin] support, you _should_ configure vim to load nerdtree-git-plugin **_before_** vim-devicons loads.

## Font Configuration

* Encoding **must** be set to UTF-8 for the glyphs to show
  ```vim
  set encoding=utf8
  ```
* For Powerline symbols to show in airline the following needs to be set
  ```vim
  let g:airline_powerline_fonts = 1
  ```

* The _ONLY_ other configuration needed should be setting the font vim uses to a
  patched font.

Already patched fonts and the font patcher script are provided at:
[nerd-fonts]

It works without configuration *ONLY* when used with a patched font provided in
the separate repository above. Install the font and add it to your `vimrc` or
`gvimrc`:

Linux
 ```vim
 set guifont=<FONT_NAME> <FONT_SIZE>
 ```

OS X and Windows
 ```vim
 set guifont=<FONT_NAME>:h<FONT_SIZE>
 ```

e.g.

Linux
```vim
set guifont=Droid\ Sans\ Mono\ for\ Powerline\ Plus\ Nerd\ File\ Types\ 11
```

OS X and Windows
```vim
set guifont=Droid\ Sans\ Mono\ for\ Powerline\ Plus\ Nerd\ File\ Types:h11
```

## Font Installation

You basically have to put any font you would like to use into the `~/.fonts` folder. For example:


Linux
```sh
cd ~/.fonts && curl -fLo DroidSansMonoForPowerlinePlusNerdFileTypes.otf https://raw.githubusercontent.com/ryanoasis/nerd-fonts/master/patched-fonts/DroidSansMono/Droid%20Sans%20Mono%20for%20Powerline%20Plus%20Nerd%20File%20Types.otf
```

OS X
```sh
cd ~/Library/Fonts && curl -fLo DroidSansMonoForPowerlinePlusNerdFileTypes.otf https://raw.githubusercontent.com/ryanoasis/nerd-fonts/master/patched-fonts/DroidSansMono/Droid%20Sans%20Mono%20for%20Powerline%20Plus%20Nerd%20File%20Types.otf
```

You can find more fonts under my [patched fonts repo][patched-fonts].


## Screenshots

![image](https://raw.githubusercontent.com/wiki/ryanoasis/vim-devicons/screenshots/v0.5.x/vim.png)

### [NERDTree]

![image](https://raw.githubusercontent.com/wiki/ryanoasis/vim-devicons/screenshots/v0.5.x/nerdtree.png)


### [vim-airline]

section             | preview
------------------- | -------------
statusline          | ![image](https://raw.githubusercontent.com/wiki/ryanoasis/vim-devicons/screenshots/v0.5.x/airline-statusline.png)
tabline             | ![image](https://raw.githubusercontent.com/wiki/ryanoasis/vim-devicons/screenshots/v0.5.x/airline-tabline-1.png)
tabline             | ![image](https://raw.githubusercontent.com/wiki/ryanoasis/vim-devicons/screenshots/v0.5.x/airline-tabline-2.png)
fileformats symbols | ![image](https://raw.githubusercontent.com/wiki/ryanoasis/vim-devicons/screenshots/v0.5.x/fileformats-symbols-sample.png)


### [CtrlP][CtrlP]

* Supports the original [CtrlP][CtrlP] plugin and [CtrlP active fork][ctrlpvim-CtrlP]
* Currently only MRU file mode supported

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/ctrlp.png)


### [unite][unite]

* Currently only supports `file`, `file_rec`, and `buffer`

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/unite.png)


### [lightline.vim][lightline.vim]

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/lightline.png)


### [vimfiler][vimfiler]

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/vimfiler.png)


### [flagship][flagship]

* _NOTE: [flagship] support is **experimental** because the [API may be changing](https://github.com/tpope/vim-flagship/issues/6#issuecomment-116121220)_

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/flagship.png)


### [nerdtree-git-plugin]

* with `g:WebDevIconsNerdTreeGitPluginForceVAlign` on

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/nerdtree-git-plugin-valign-on-sample.png)

* with `g:WebDevIconsNerdTreeGitPluginForceVAlign` off

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/nerdtree-git-plugin-valign-off-sample.png)


### Different patched fonts example

![image](https://raw.githubusercontent.com/wiki/ryanoasis/vim-devicons/screenshots/v0.5.x/different-fonts-sample.png)


### Various Terminal Emulators

* gnome terminal

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/terminal-gnome-sample.png)

* Urxvt terminal

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/terminal-urxvt-sample.png)

### Windows

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/windows-sample.png)

### Mac OS X

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/osx-sample.png)
*Thanks @RageZBla*

### Glyph set test file

![image](https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v0.5.x/glyph-set-test.png)

## Features
* show developer file type glyphs from a font in various vim plugins, currently supports:
  * [NERDTree]
  * [vim-airline][vim-airline] (statusline and tabline)
  * [lightline.vim][lightline.vim] (statusline)
    * see: [lightline](#lightline) for setup
* Adds a global config map of characters to file extensions (or entire filenames)
* customizable and extendable filetype detections
  * ability to override predefined dictionary variable
  * if you are unhappy with the default glyph used you can choose your own
* supports a range of file type extensions by default:
  * ```styl, scss, htm, html, slim, css, less, md, json, js, jsx, rb, php, py, pyc, pyd, pyo, coffee, mustache, hbs, conf, ini, yml, jpg, jpeg, bmp, png, gif, twig, cpp, c++, cxx, cc, cp, c, hs, lhs, lua, java, sh, fish, diff, db, clj, cljs, edn, scala, go, dart, xul, sln, suo, pl, pm, t, rss, f#, fsscript, fsx, fs, fsi, rs, rlib, d, erl, hrl, vim, ai, psd, psb```
* supports full filename matches, by default:
  * ```gruntfile.coffee, gruntfile.js, gruntfile.ls, gulpfile.coffee, gulpfile.js, gulpfile.ls, dropbox```
* supports library pattern matches, by default:
  * ```jquery, angular, backbone, requirejs, materialize, mootools```
* font patcher ([nerd-fonts])
  * requires: python2, python-fontforge package
  * example usage
	> ./font-patcher unpatched-sample-fonts/Droid\ Sans\ Mono\ for\ Powerline.otf

## Extra Configuration

* by default you should not *NEED* to configure anything to get the basics working
  * _NOTE:_ You *NEED* to use one of the patched font provided or patch your own ([nerd-fonts]) _unless_ you want to configure the filetype to glyph mappings yourself for your current font
* these options can be defined in your `vimrc` or `gvimrc`
* the following options are provided however for overriding

* enable/disable loading the plugin (default 1)
 ```vim
let g:webdevicons_enable = 1
 ```

* enable/disable adding the flags to NERDTree (default 1)
 ```vim
 let g:webdevicons_enable_nerdtree = 1
  ```

* enable/disable adding the custom source to unite (default 1)
 ```vim
 let g:webdevicons_enable_unite = 1
  ```

* enable/disable adding the column to vimfiler (default 1)
 ```vim
 let g:webdevicons_enable_vimfiler = 1
  ```

* enable/disable adding to vim-airline's tabline (default 1)
 ```vim
let g:webdevicons_enable_airline_tabline = 1
  ```

* enable/disable adding to vim-airline's statusline (default 1)
 ```vim
let g:webdevicons_enable_airline_statusline = 1
  ```

* enable/disable ctrlp MRU file mode glyphs (default 1)
 ```vim
 let g:webdevicons_enable_ctrlp = 1
  ```

* enable/disable adding to flagship's statusline (default 1)
 ```vim
let g:webdevicons_enable_flagship_statusline = 1
  ```

* turn on/off file node glyph decorations (not particularly useful)
 ```vim
let g:WebDevIconsUnicodeDecorateFileNodes = 1
  ```

* whether or not font is using double-width glyphs (default 1, set to 0 for single character width glyphs)
	* _note:_ does not actually switch the font or try to use the correct font, just adds a space to account for a double width glyph, you have to set the correct double width glyph font in your terminal or `guifont`
 ```vim
let g:WebDevIconsUnicodeGlyphDoubleWidth = 1
  ```

* whether or not to show the nerdtree brackets around flags (default 1)
```vim
let g:webdevicons_conceal_nerdtree_brackets = 1
```

* the amount of space to use after the glyph character (default ' ')
```vim
let g:WebDevIconsNerdTreeAfterGlyphPadding = '  '
```

* Force extra padding in NERDTree so that the filetype icons line up vertically (when [nerdtree-git-plugin] is present) (default 1)
```vim
let g:WebDevIconsNerdTreeGitPluginForceVAlign = 1
```

### Character Mappings

* `ƛ` is used as an example below, substitute for the glyph you **actually** want to use

* change the default character when no match found
 ```vim
let g:WebDevIconsUnicodeDecorateFileNodesDefaultSymbol = 'ƛ'
  ```

* enable folder/directory glyph flag (disabled by default with 0)
 ```vim
let g:WebDevIconsUnicodeDecorateFolderNodes = 1
  ```

* enable custom folder/directory glyph exact matching (enabled by default when g:WebDevIconsUnicodeDecorateFolderNodes is set to 1)
 ```vim
let WebDevIconsUnicodeDecorateFolderNodesExactMatches = 1
  ```

* change the default folder/directory glyph/icon
 ```vim
let g:WebDevIconsUnicodeDecorateFolderNodeDefaultSymbol = 'ƛ'
  ```

* change the default dictionary mappings for file extension matches
 ```vim
let g:WebDevIconsUnicodeDecorateFileNodesExtensionSymbols = {} " needed
let g:WebDevIconsUnicodeDecorateFileNodesExtensionSymbols['js'] = 'ƛ'
  ```

* change the default dictionary mappings for exact file node matches
 ```vim
let g:WebDevIconsUnicodeDecorateFileNodesExactSymbols = {} " needed
let g:WebDevIconsUnicodeDecorateFileNodesExactSymbols['MyReallyCoolFile.okay'] = 'ƛ'
  ```

* add or override individual additional filetypes
 ```vim
let g:WebDevIconsUnicodeDecorateFileNodesExtensionSymbols = {} " needed
let g:WebDevIconsUnicodeDecorateFileNodesExtensionSymbols['myext'] = 'ƛ'
  ```

## Installation

* [Sample Windows vimrc configuration 1](https://github.com/ryanoasis/vim-devicons/wiki/samples/v0.5.x/.vimrc-windows-1)
* [Sample Linux vimrc configuration 1](https://github.com/ryanoasis/vim-devicons/wiki/samples/v0.5.x/.vimrc-linux-1)

This plugin follows the standard runtime path structure, and as such it can be installed with a variety of plugin managers:

*  [Pathogen](https://github.com/tpope/vim-pathogen)
  *  `git clone https://github.com/ryanoasis/vim-devicons ~/.vim/bundle/vim-devicons`
*  [NeoBundle](https://github.com/Shougo/neobundle.vim)
  * Add to vimrc:

      ```vim
      NeoBundle 'ryanoasis/vim-devicons'
      ```
  * And install it:

      ```vim
      :so ~/.vimrc
      :NeoBundleInstall
      ```

*  [Vundle](https://github.com/gmarik/vundle)
  * Add to vimrc:

       ```vim
       Plugin 'ryanoasis/vim-devicons'
       ```
  * And install it:

       ```vim
       :so ~/.vimrc
       :PluginInstall`
       ```

*  manual
  *  copy all of the files into your `~/.vim` directory

## Lightline

To add the appropriate icon to [lightline](https://github.com/itchyny/lightline.vim), call the function `WebDevIconsGetFileTypeSymbol()` and/or `WebDevIconsGetFileFormatSymbol()` in your `.vimrc`. For example, you could set your sections to:

```vim
let g:lightline = {
      \ 'component_function': {
      \   'filetype': 'MyFiletype',
      \   'fileformat': 'MyFileformat',
      \ }
      \ }

function! MyFiletype()
  return winwidth(0) > 70 ? (strlen(&filetype) ? &filetype . ' ' . WebDevIconsGetFileTypeSymbol() : 'no ft') : ''
endfunction

function! MyFileformat()
  return winwidth(0) > 70 ? (&fileformat . ' ' . WebDevIconsGetFileFormatSymbol()) : ''
endfunction
```

## API

```vim
" returns the font character that represents the icon
" parameters: a:1 (filename), a:2 (isDirectory)
" both parameters optional
" by default without parameters uses buffer name
WebDevIconsGetFileTypeSymbol(...)

" returns the font character that represents
" the file format as an icon (windows, linux, mac)
WebDevIconsGetFileFormatSymbol()
```

### API Examples

* todo

## Todo

* [ ] more filetypes to support
* [x] ~~make sure it works properly and does not conflict with [nerdtree-git-plugin]~~
* [ ] customize filetype icon colors
* [ ] more customization options in general
* [ ] more specific FAQ and Troubleshooting help

## FAQ / Troubleshooting

* I don't want to use any of the fonts provided, I want to use font ABC
 * try the font patcher: [nerd-fonts]
 * see font configuration above for more details

* It isn't working
  * Are you using the patched font provided in the separate repo ([nerd-fonts]) or are you patching your own?
  * _NOTE:_ if running vim and no font set it will default to the terminal font that is set
  * check what the vim/gvim font is set to, from ex mode:

    ```vim
    :set guifont?
    ```

  * check if the plugin is loaded (should give '1'), from ex mode:

    ```vim
    :echo loaded_webdevicons
    ```

  * check if the plugin is enabled (should give '1'), from ex mode:

    ```vim
    :echo g:webdevicons_enable
    ```

  * check if the plugin is enabled for NERDTree (should give '1'), from ex mode:
    * this should *NOT* need to be set under normal circumstances

    ```vim
    :echo g:webdevicons_enable_nerdtree
    ```

  * check if you are able to see the characters, from ex mode:

    ```vim
    :echo g:WebDevIconsUnicodeDecorateFileNodesDefaultSymbol
    ```

  * if all this looks correct you may try this to see if any files show flags
    * last resort, see if you can even set the default symbol and have it display anywhere (NERDTree, vim-airline's statusline, vim-airlines's tabline), from ex mode:

    ```vim
    :let g:WebDevIconsUnicodeDecorateFileNodesDefaultSymbol='x'
    ```

* How did you get color matching based on file type in nerdtree?
  * my current settings are from: https://github.com/scrooloose/nerdtree/issues/201#issuecomment-9954740

	```vim
	" NERDTress File highlighting
	function! NERDTreeHighlightFile(extension, fg, bg, guifg, guibg)
	 exec 'autocmd FileType nerdtree highlight ' . a:extension .' ctermbg='. a:bg .' ctermfg='. a:fg .' guibg='. a:guibg .' guifg='. a:guifg
	 exec 'autocmd FileType nerdtree syn match ' . a:extension .' #^\s\+.*'. a:extension .'$#'
	endfunction

	call NERDTreeHighlightFile('jade', 'green', 'none', 'green', '#151515')
	call NERDTreeHighlightFile('ini', 'yellow', 'none', 'yellow', '#151515')
	call NERDTreeHighlightFile('md', 'blue', 'none', '#3366FF', '#151515')
	call NERDTreeHighlightFile('yml', 'yellow', 'none', 'yellow', '#151515')
	call NERDTreeHighlightFile('config', 'yellow', 'none', 'yellow', '#151515')
	call NERDTreeHighlightFile('conf', 'yellow', 'none', 'yellow', '#151515')
	call NERDTreeHighlightFile('json', 'yellow', 'none', 'yellow', '#151515')
	call NERDTreeHighlightFile('html', 'yellow', 'none', 'yellow', '#151515')
	call NERDTreeHighlightFile('styl', 'cyan', 'none', 'cyan', '#151515')
	call NERDTreeHighlightFile('css', 'cyan', 'none', 'cyan', '#151515')
	call NERDTreeHighlightFile('coffee', 'Red', 'none', 'red', '#151515')
	call NERDTreeHighlightFile('js', 'Red', 'none', '#ffa500', '#151515')
	call NERDTreeHighlightFile('php', 'Magenta', 'none', '#ff00ff', '#151515')
	call NERDTreeHighlightFile('ds_store', 'Gray', 'none', '#686868', '#151515')
	call NERDTreeHighlightFile('gitconfig', 'Gray', 'none', '#686868', '#151515')
	call NERDTreeHighlightFile('gitignore', 'Gray', 'none', '#686868', '#151515')
	call NERDTreeHighlightFile('bashrc', 'Gray', 'none', '#686868', '#151515')
	call NERDTreeHighlightFile('bashprofile', 'Gray', 'none', '#686868', '#151515')
	```
	Note: If the colors still are not highlighting, try invoking such as:
	```
	autocmd VimEnter * call NERDTreeHighlightFile('jade', 'green', 'none', 'green', '#151515')
	```
	per: https://github.com/ryanoasis/vim-devicons/issues/49#issuecomment-101753558

* Issues after re-sourcing `vimrc`
  * Try adding this to the bottom of your `vimrc`

	```vim
	if exists("g:loaded_webdevicons")
		call webdevicons#refresh()
	endif
	```

## Contributing

Best ways to contribute
* Star it on GitHub - if you use it and like it please at least star it :)
* [Promote](#promotion)
* Open [issues/tickets](https://github.com/ryanoasis/vim-devicons/issues)
* Submit fixes and/or improvements with [Pull Requests](#source-code)

### Promotion

Like the project? Please support to ensure continued development going forward:
* Star this repo on [GitHub][vim-devicons-repo]
* Follow the repo on [GitHub][vim-devicons-repo]
* Vote for it on [vim.org](http://www.vim.org/scripts/script.php?script_id=5114)
* Follow me
  * [Twitter](http://twitter.com/ryanlmcintyre)
  * [GitHub](https://github.com/ryanoasis)

### Source code

Contributions and pull requests are welcome.

No real formal process has been setup - just stick to general good conventions
for now.

## Rationale

After seeing the awesome theme for Atom (seti-ui) and the awesome plugins work done for NERDTree and vim-airline and wanting something like this for Vim I decided to create my first plugin.

## Inspiration and special thanks

* [vim-airline]
* [nerdtree]
* [nerdtree-git-plugin]
* [seti-ui](https://atom.io/themes/seti-ui)
* [devicons by Theodore Vorillas](http://vorillaz.github.io/devicons)
* [benatespina development.svg.icons](https://github.com/benatespina/development.svg.icons)
* [Steve Losh](http://learnvimscriptthehardway.stevelosh.com/)

### Also thanks to the many contributors:
* [contributors list](https://github.com/ryanoasis/vim-devicons/graphs/contributors)

## License

See [LICENSE](LICENSE)

<!---
Link References
-->

[nerd-fonts]:https://github.com/ryanoasis/nerd-fonts
[patched-fonts]:https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts
[NERDTree]:https://github.com/scrooloose/nerdtree
[vim-airline]:https://github.com/bling/vim-airline
[lightline.vim]:https://github.com/itchyny/lightline.vim
[lightline]:https://github.com/itchyny/lightline.vim
[nerdtree-git-plugin]:https://github.com/Xuyuanp/nerdtree-git-plugin
[unite]:https://github.com/Shougo/unite.vim
[unite.vim]:https://github.com/Shougo/unite.vim
[vimfiler]:https://github.com/Shougo/vimfiler.vim
[flagship]:https://github.com/tpope/vim-flagship
[CtrlP]:https://github.com/kien/ctrlp.vim
[ctrlpvim-CtrlP]:https://github.com/ctrlpvim/ctrlp.vim

[vim-devicons-repo]:https://github.com/ryanoasis/vim-devicons
[vim-devicons-polls]:https://github.com/ryanoasis/vim-devicons/labels/poll
[badge-version]:http://badge.fury.io/gh/ryanoasis%2Fvim-devicons
[badge-gitter]:https://gitter.im/ryanoasis/vim-devicons?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge
[badge-flattr]:https://flattr.com/submit/auto?user_id=ryanoasis&url=https://github.com/ryanoasis/vim-devicons&title=vim-devicons&language=viml&tags=github&category=software

[img-version-badge]:https://badge.fury.io/gh/ryanoasis%2Fvim-devicons.svg
[img-gitter-badge]:https://img.shields.io/badge/%E2%8A%AA%20GITTER%20-CHAT%20%E2%86%92-1dce73.svg?style=flat
[img-flattr-badge]:https://img.shields.io/badge/donate-flattr%20this!-8DB65B.svg?style=flat
[img-visual-toc-screenshots]:https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v1.0.0/branding-logo-screenshots-sm.png
[img-visual-toc-api]:https://github.com/ryanoasis/vim-devicons/wiki/screenshots/v1.0.0/branding-logo-api-sm.png
[img-visual-toc-patched-fonts]:https://raw.githubusercontent.com/ryanoasis/nerd-fonts/master/images/nerd-fonts-character-logo-md.png
[img-visual-toc-fonts-patcher]:https://raw.githubusercontent.com/ryanoasis/nerd-fonts/master/images/nerd-fonts-patcher-logo-md.png
