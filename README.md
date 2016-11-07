# XYplorer Script in Atom

Add syntax highlighting and snippets for [XYplorer]( https://www.xyplorer.com/ "XYplorer Website" )  script.



## Initially Commit
Start from XYplorer forum files published by [highend](https://www.xyplorer.com/xyfc/viewtopic.php?f=7&t=14230)


## Support [File-Icons][1cf1d58f]

Enable [file-icons][1cf1d58f] package and add the following code to `styles.less`.

```css
@import "packages/file-icons/styles/colors";
@import "packages/file-icons/styles/icons";
@import "packages/file-icons/styles/items";
@{pane-tab-selector}, .icon-file-text {
  &[data-name$=".xys"]:before { .xmos-icon;             .dark-blue; }
  &[data-name$=".xyi"]:before { .xmos-icon;         .medium-purple; }
}
```
## Support ctags

Add the following code in `ctags.cnf`

```ini
--langdef=XYplorer
--langmap=XYplorer:.xys.xyi
--regex-XYplorer=/^\s*(function|FUNCTION)\s+([a-zA-Z\-]+)/\2/f, functions/
```

[1cf1d58f]: https://atom.io/packages/file-icons "file-icons"
