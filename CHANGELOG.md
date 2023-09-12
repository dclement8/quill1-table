# Changelog

All notable changes to this project will be documented in this file.

## [1.7.0] - 2023-09-12

- Show/hide table border <https://github.com/dclement8/quill1-table/pull/12> by [@cfonseca88](https://github.com/cfonseca88)
- Fix cmd key not working on Mac

## [1.6.5] - 2023-07-11

- Fix remove row function not working if cursor is in cell <https://github.com/dclement8/quill1-table/pull/10> by [@cfonseca88](https://github.com/cfonseca88)
- Fix quill delta in text-change event during split cell <https://github.com/dclement8/quill1-table/pull/9> by [@vtejuf](https://github.com/vtejuf)
- Update quill-delta, webpack-cli dev dependency

## [1.6.4] - 2023-01-23

- Manage th, empty td and td without p <https://github.com/dclement8/quill1-table/issues/7>

## [1.6.3] - 2022-12-14

- Specify which export should be exposed as a library in webpack config <https://github.com/dclement8/quill1-table/issues/6>

## [1.6.2] - 2022-11-07

- Add typescript definition <https://github.com/dclement8/quill1-table/issues/5>

## [1.6.1] - 2022-09-22

- Fix "Edge case for delete then undo of cell" <https://github.com/dclement8/quill1-table/issues/3>

## [1.6.0] - 2022-09-01

- Update dependencies

### Added

- Tabbing between cells by [@cfonseca88](https://github.com/cfonseca88).
- Select all in cell by [@cfonseca88](https://github.com/cfonseca88).
- Option for selecting cells with CTRL key by [@cfonseca88](https://github.com/cfonseca88).

## [1.5.2] - 2022-08-04

### Changed

- Improve TableToolbar enabled/disabled options (updated selectors)

## [1.5.1] - 2022-07-04

### Added

- Copy table selection to clipboard (ctrl+c)

## [1.5.0] - 2022-07-01

### Changed

- Manage multiple instances of quill1-table

### Breaking Changes

- Keyboard bindings handler functions must be used as regular functions in order to pass this.quill to TableModule.keyboardHandler method (as first argument, before key name)
- Table data (containing pasted, row_counter and cell_counter) is no longer stored in quill.history.tables, stored in quill.table.tables instead
- TableSelection.isInTable moved to quill.table.isInTable (for managing multiple instances)
- TableHistory.undo and TableHistory.redo need quill instance as first argument (and change id as second argument)
- TableSelection.mouseDown, TableSelection.mouseMove, TableSelection.mouseUp and TableSelection.selectionChange need quill instance as first argument

[Unreleased]: https://github.com/dclement8/quill1-table/compare/1.7.0...HEAD
[1.7.0]: https://github.com/dclement8/quill1-table/compare/1.6.5...1.7.0
[1.6.5]: https://github.com/dclement8/quill1-table/compare/1.6.4...1.6.5
[1.6.4]: https://github.com/dclement8/quill1-table/compare/1.6.3...1.6.4
[1.6.3]: https://github.com/dclement8/quill1-table/compare/1.6.2...1.6.3
[1.6.2]: https://github.com/dclement8/quill1-table/compare/1.6.1...1.6.2
[1.6.1]: https://github.com/dclement8/quill1-table/compare/1.6.0...1.6.1
[1.6.0]: https://github.com/dclement8/quill1-table/compare/1.5.2...1.6.0
[1.5.2]: https://github.com/dclement8/quill1-table/compare/1.5.1...1.5.2
[1.5.1]: https://github.com/dclement8/quill1-table/compare/1.5.0...1.5.1
[1.5.0]: https://github.com/dclement8/quill1-table/compare/1.4.1...1.5.0
