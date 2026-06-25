# Changelog
All notable changes to this project will be documented in this file.

The format is based on
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to
[Semantic Versioning](http://semver.org/spec/v2.0.0.html).


## [Unreleased]

### Added
### Changed
### Deprecated
### Removed
### Fixed
### Security



## [1.4.2] - 2026-06-25

### Changed
- `inctext` made compatible with tagging (issue https://github.com/latex3/tagging-project/issues/1429)
- `\incgraph`, `\incmultigraph`, `\incmultipages` made compatible with tagging
- Overlay content (mainly page numbering) made to be ignored by tagging (issue #6)



## [1.4.1] - 2026-06-09

### Changed
- `x` type expansions replaced by `e` or other code
- Some code improvements
- Documentation produced with `minted` instead of `minted2` (after Python fix)
- Required LaTeX version bumped to 2026-06-01
- Kerning code adapted to the new `\dim_horizontal:n` and `\dim_vertical:n`
    of the L3 programming layer
- Documentation of `documentpaper` amended
- References updated

### Removed
- Keys `page` and `center`, which are deprecated since v1.10 (2012-09-28),
  removed from documentation (still active in code)

### Fixed
- `documentpaper` was broken
- Code style improved with help of explcheck (1 false positive error and 587 warnings removed)



## [1.4.0] - 2026-03-04

### Added
- `incgraph.doc.bib` for references (moved from documentation source)
- `\incmultipages`: specialized macro to include multiple pages from a PDF file

### Changed
- .tds.zip removed from CTAN upload to comply to CTAN rules
- TDS structure flattend on GitHub repository
- `README.md` adapted to these changes
- `CHANGES.md` renamed to `CHANGELOG.md` following https://keepachangelog.com/en/1.1.0/
- `incgraph-doc.sty` renamed to `incgraph.doc.sty`
- References updated
- Required LaTeX version bumped to 2025-06-01
- Implementation of `\igrGetLastPage` changed. It wraps a L3 layer function now.
- `\igrLastPage` is locally assigned now.

### Fixed
- Documentation produced with `minted2` instead of `minted` (currently not compatible to Python>=3.14)
- `\eject` and `\break` replaced by `\clearpage` to get compatibility
    with `twocolumn` documents (part of issue #5)
- Several minor documentation corrections    



## [1.3.0] - 2024-03-14

### Added
- Option `overlay page number options app` (issue #2)
- Option `xshift`
- Option `yshift`
- Autosize Options:
    - Option `autosize`
    - Option `autosize width gap`
    - Option `autosize height gap`
    - Option `autosize gap`
    - Option `autosize min scale`
    - Option `autosize max scale`

### Changed
- Implementation overhauled and completely rewritten in LaTeX3.
    Major changes of the whole code.
    Option keys kept to be pgfkeys.
- `\igrboxcenter` drops box now after usage

### Fixed
- Documentation typo (issue #4)



## [1.2.0] - 2021-10-20

### Added
- Option `overlay page number options` (issue #2)
- `\igrGetPageSize`
- `\igrPageWidth`
- `\igrPageHeight`
- `\igrSetPageSize`
- `\igrGetLastPage`
- `\igrLastPage`
- Adding/Guessing file name extensions (issue #1):
    - Option `extensions`
    - Option `extensions add`
    - Option `extensions from graphics`
    - Option `ignore on not found with extensions`
    - Option `ignore on not found with extensions*`
- Option `no existence check`

### Changed
- Changelog moved from CHANGES to CHANGES.md and adapted to
  [Keep a Changelog](https://keepachangelog.com/en/1.0.0/)
- From now on version numbers adhere to
  [Semantic Versioning](http://semver.org/spec/v2.0.0.html)
- Readme moved from README to README.md 
- Documentation code revised
- Internal package creation process modernized (invisible to the user)
- Adaption of paper size made compatible with lualatex
- Implementation of `\incgraph` and `\incmultigraph` changed (to LaTeX3)

### Fixed
- Documentation typos corrected (issue #3)
- `\incgraph` ignored option settings for not existing files.



## [1.12] - 2015-03-12

### Added
- Option `left border`
- Option `bottom border`
- Option `right border`
- Option `top border`
- Option `horizontal border`
- Option `vertical border`
- Option `border`

### Changed
- ugly pictures of the documentation exchanged by not so ugly ones.



## [1.11] - 2013-01-16

### Added
- added `clearpage` at begin of `inctext`

### Fixed
- Positioning on even pages for twosided documents
- Option `paper=document` could not be used inside the preamble



## [1.10] - 2012-09-28

### Added
- new macro `\igrcenterfit` for an arbitrary paper size
- new user interface environment `inctext` to support
  arbitrary internal graphics
- introduction of various paper format options with the key `paper`
- new `landscape` and `portrait` keys
- new keys `currentpaper`, `graphicspaper` and `documentpaper`
  to replace the deprecated keys `page` and `center`

### Changed
- overlay code and graphics inclusion decoupled internally
- output macro implementation rewritten
- documentation structure changed
- various internal code changes

### Fixed
- interlineskip problem fixed



## [1.02] - 2012-07-06

### Added
- new macro `\igrboxtikzcenter` to support tikz pictures with a centered box.
- new feature to overlay included graphics with tikz picture code
  using the new option keys `overlay`, `overlay page number at`,
  `overlay page number at bottom`, `overlay page number at top`,
  `no overlay`.

### Changed
- key `nohyper` renamed to `no hyper`
- option key `include command` now has a default.

### Fixed
- bug fixed in `\igrboxtikz` which caused a small shift.



## [1.01] - 2012-07-04

### Added
- new macro `\igrtargetset` to set hypertarget values manually
- new key `target` to set hypertarget values manually

### Changed
- the code of the hypertarget setting is rewritten to place it at
  the top left corner of the page (previously it was placed at the
  top left corner of the text area).



## [1.00] - 2012-06-21

### Added
- initial public release
