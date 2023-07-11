# QuillJS Table (quill1-table)

<p>
  <a href="https://npmjs.com/package/quill1-table" title="Version">
    <img src="https://img.shields.io/npm/v/quill1-table.svg" alt="Version">
  </a>
  <a href="https://npmjs.com/package/quill1-table" title="Downloads">
    <img src="https://img.shields.io/npm/dm/quill1-table.svg" alt="Downloads">
  </a>
</p>

`TABLE` functionality in QuillJS (v1) using Containers.

Code of quill is included in project so we can easily play with it in our tests.

## Features

* Add or remove a table/column/row/cell
* ctrl+z/ctrl+shift+z (undo/redo)
* select a cell or multiple cells
* split/merge cell
* remove cell/selection
* copy/paste a table
* add col/row before/after
* copy & paste table from Word
* tabbing between cells
* select all cell content
* cell selection on click or with CTRL key

## Usage

see example [demo.js](../master/src/demo.js)

```
// import module
import TableModule from 'quill1-table';

// register module
Quill.register('modules/table', TableModule);

// add toolbar controls in Toolbar module options
[
  {
    table: TableModule.tableOptions()
  },
  {
    table: [
      'insert',
      'append-row-above',
      'append-row-below',
      'append-col-before',
      'append-col-after',
      'remove-col',
      'remove-row',
      'remove-table',
      'split-cell',
      'merge-selection',
      'remove-cell',
      'remove-selection',
      'undo',
      'redo'
    ]
  }
]

// add module in Quill options
modules: {
  table: {
    // table module options
    cellSelectionOnClick: true // true: cell selection on click, false: cell selection with CTRL key
  },
  // add keyboard bindings in Keyboard options
  keyboard: {
    // Since Quill’s default handlers are added at initialization, the only way to prevent them is to add yours in the configuration.
    bindings: {
      backspace: {
        key: 'backspace',
        handler: function (range, keycontext) {
          return TableModule.keyboardHandler(this.quill, 'backspace', range, keycontext);
        }
      },
      delete: {
        key: 'delete',
        handler: function (range, keycontext) {
          return TableModule.keyboardHandler(this.quill, 'delete', range, keycontext);
        }
      },
      undo: {
        ctrlKey: true,
        key: 'z',
        handler: function (range, keycontext) {
          return TableModule.keyboardHandler(this.quill, 'undo', range, keycontext);
        }
      },
      redo: {
        ctrlKey: true,
        shiftKey: true,
        key: 'z',
        handler: function (range, keycontext) {
          return TableModule.keyboardHandler(this.quill, 'redo', range, keycontext);
        }
      }
    }
  }
}
```

## Changelog

see [CHANGELOG.md](../master/CHANGELOG.md)

### For development
```shell script
npm install

npm run build
```
