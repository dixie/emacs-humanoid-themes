# Fork of Humanoid-themes for Emacs

Minor changes like:

- added blue border around mode-line for recognizing boundaries between windows.
- window-divider is blue-light, again for better visibility of windows boundaries.

# Humanoid-themes for Emacs

Humanoid theme is an Emacs color theme package that started as a theme for [spacemacs](https://github.com/syl20bnr/spacemacs).
The collection comes with a dark and a light variant and it should work well with true color and 256 color terminals.

## Screenshots

[![light theme](https://github.com/humanoid-colors/emacs-humanoid-themes/wiki/assets/screenshots/org-mode-humanoid-light.png)](https://github.com/humanoid-colors/emacs-humanoid-themes/wiki/assets/screenshots/org-mode-humanoid-light.png)

[![dark theme](https://github.com/humanoid-colors/emacs-humanoid-themes/wiki/assets/screenshots/org-mode-humanoid-dark.png)](https://github.com/humanoid-colors/emacs-humanoid-themes/wiki/assets/screenshots/org-mode-humanoid-dark.png)

## Highlights

The theme has good support for org mode.

## Installation and usage

[![MELPA](https://melpa.org/packages/humanoid-themes-badge.svg)](https://melpa.org/#/humanoid-themes)

The recommended way to install the Humanoid themes is with [MELPA](https://melpa.org/#/getting-started):

Install the Humanoid themes from the [MELPA repository](https://melpa.org/#/humanoid-themes). The version of `humanoid-themes` there will always be up-to-date.

Enable the theme use either `humanoid-light` or `humanoid-dark`:

```
M-x load-theme RET humanoid-light 
```

Or add the following to your `init.el` or `.emacs` file to load the theme at start:

```lisp
(load-theme 'humanoid-light t) ;; Use "humanoid-dark" for the dark variant
```

## Supported modes

Some of the supported modes are:

* calfw
* company
* ein
* erc
* ESS modes (users may want to customize the variables ess-R-font-lock-keywords and inferior-ess-r-font-lock-keywords)
* gnus
* helm
* ido
* info
* ledger
* magit
* mu4e
* neotree
* org
* rainbow
* and others

## Customizations

The theme has some options that can be tweaked via `M-x customize`:

* `humanoid-thmes-arc-bg`:

Makes background colors suitable for Arc colored GUI themes.

* `humanoid-thmes-comment-bg`:

This toggles a background color for the comment lines.

* `humanoid-thmes-comment-italic`:

This toggles italics for comments and will also add a lighter color to it. It is recommended to disable `humanoid-thmes-comment-bg` if you turn this option on for better contrast.

* `humanoid-thmes-keyword-italic`:

This toggles italics for keywords.

* `humanoid-thmes-org-agenda-height`:

This toggles the use of varying org agenda heights.

* `humanoid-thmes-org-bold`:

This toggles bold text for org headings.

* `humanoid-thmes-org-height`:

This toggles the use of varying org headings heights.

* `humanoid-thmes-org-highlight`:

This toggles highlighting of org headings.

* `humanoid-thmes-org-priority-bold`:

This toggles bold text for priority items in agenda view.

* `humanoid-thmes-custom-colors`:

This allows for specifying a list of custom colors to override humanoid theme colors. More details in the next section.

* `humanoid-thmes-underline-parens`:

This toggles the underline of matching parens when using `show-paren-mode` or similar.

### Override theme's colors

The theme can be customized by overriding one of the theme local variables by setting a list in the `humanoid-thmes-custom-colors` variable.
Here's a list of all the local variables and roles:

| var           | role                                                                                              |
|---------------|---------------------------------------------------------------------------------------------------|
| act1          | One of mode-line's active colors.                                                                 |
| act2          | The other active color of mode-line.                                                              |
| base          | The basic color of normal text.                                                                   |
| base-dim      | A dimmer version of the normal text color.                                                        |
| bg1           | The background color.                                                                             |
| bg2           | A darker background color. Used to highlight current line.                                        |
| bg3           | Yet another darker shade of the background color.                                                 |
| bg4           | The darkest background color.                                                                     |
| border        | A border line color. Used in mode-line borders.                                                   |
| cblk          | A code block color. Used in org's code blocks.                                                    |
| cblk-bg       | The background color of a code block.                                                             |
| cblk-ln       | A code block header line.                                                                         |
| cblk-ln-bg    | The background of a code block header line.                                                       |
| cursor        | The cursor/point color.                                                                           |
| const         | A constant.                                                                                       |
| comment       | A comment.                                                                                        |
| comment-bg    | The background color of a comment. To disable this, `customize` `humanoid-thmes-comment-bg`.      |
| comp          | A complementary color.                                                                            |
| err           | errors.                                                                                           |
| func          | functions.                                                                                        |
| head1         | Level 1 of a heading. Used in org's headings.                                                     |
| head1-bg      | The background of level 2 headings. To disable this, `customize` `humanoid-thmes-org-highlight`.  |
| head2         | Level 2 headings.                                                                                 |
| head2-bg      | Level 2 headings background.                                                                      |
| head3         | Level 3 headings.                                                                                 |
| head3-bg      | Level 3 headings background.                                                                      |
| head4         | Level 4 headings.                                                                                 |
| head4-bg      | Level 4 headings background.                                                                      |
| highlight     | A highlighted area.                                                                               |
| highlight-dim | A dimmer highlighted area.                                                                        |
| keyword       | A keyword or a builtin color.                                                                     |
| lnum          | Line numbers.                                                                                     |
| mat           | A matched color. Used in matching parens, brackets and tags.                                      |
| meta          | A meta line. Used in org's meta line.                                                             |
| str           | A string.                                                                                         |
| suc           | To indicate success. Opposite of error.                                                           |
| ttip          | Tooltip color.                                                                                    |
| ttip-sl       | Tooltip selection color.                                                                          |
| ttip-bg       | Tooltip background color.                                                                         |
| type          | A type color.                                                                                     |
| var           | A variable color.                                                                                 |
| war           | A warning color.                                                                                  |


There is also explicit colors variables that can be customized:

* aqua
* aqua-bg
* green
* green-bg
* green-bg-s
* cyan
* red
* red-bg
* red-bg-s
* blue
* blue-bg
* blue-bg-s
* magenta
* yellow
* yellow-bg

The `green` and `red` colors have two background versions. The `green-bg` and  `red-bg` are normal light background colors.
The `green-bg-s`, `red-bg-s`, and `blue-bg-s` are a stronger version and are used in `ediff` and places were text is added, deleted or changed.

If you are using [spacemacs](https://github.com/syl20bnr/spacemacs), you can put this snippet in your `dotspacemacs/user-init` to override these colors:

```elisp
  (custom-set-variables '(humanoid-custom-colors
                          '((act1 . "#ff0000")
                            (act2 . "#0000ff")
                            (base . "#ffffff"))))
```

This will override `act1`, `act1` and `base` to use the specified colors.
