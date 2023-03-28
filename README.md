**NOTE**: This fork has been discontinued, since I opted for a local version of the build. If you would like to create your own personalized local version as well, do the following steps:

- Fork the ckeditor build within a folder on your project (ie. project/external)
- In the forked directory, run `npm install`
- Adjust the build as you would like, adding, removing and configuring your editor
- Perform `yarn build` in the forked directory
- Add the build to the package.json dependencies (ex: `"my-custom-build": "file:./external/ckeditor-build-classic"`)
- In your file, import the build (ex: `import ClassicEditor from 'my-custom-build'`)

You now have a local customizable version of the editor. This can also be applied to other packages, as long as you have the source code. Also, if you have the git still initialized to the upstream fork, you can always perform updates to your build whenever they are available (see [Updating the build](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/development/custom-builds.html#updating-the-build))

CKEditor 5 Classic Plus
========================================

[![npm version](https://badge.fury.io/js/%40ckeditor%2Fckeditor5-build-classic.svg)](https://www.npmjs.com/package/@ckeditor/ckeditor5-build-classic)
[![Build Status](https://travis-ci.org/ckeditor/ckeditor5-build-classic.svg?branch=master)](https://travis-ci.org/ckeditor/ckeditor5-build-classic)
<br>
[![Dependency Status](https://david-dm.org/ckeditor/ckeditor5-build-classic/status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-classic)
[![devDependency Status](https://david-dm.org/ckeditor/ckeditor5-build-classic/dev-status.svg)](https://david-dm.org/ckeditor/ckeditor5-build-classic?type=dev)

The classic editor build for CKEditor 5. Read more about the [classic editor build](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/overview.html#classic-editor) and see the [demo](https://ckeditor.com/docs/ckeditor5/latest/examples/builds/classic-editor.html).

This specific build has been adjusted to use some existing plugins, plus multiple additional plugins. See [Additional Plugins](#Additional-Plugins).

![CKEditor 5 classic editor build screenshot](https://c.cksource.com/a/1/img/npm/ckeditor5-build-classic.png)

## Enabled Default Plugins
 - Essentials
 - UploadAdapter
 - Autoformat
 - Bold
 - Italic
 - Underline
 - Strikethrough
 - SuperScript
 - SubScript
 - Code
 - BlockQuote
 - CKFinder
 - EasyImage
 - Heading
 - Image
 - ImageCaption
 - ImageStyle
 - ImageToolbar
 - ImageUpload
 - Indent
 - Link
 - List
 - MediaEmbed
 - Paragraph
 - PasteFromOffice
 - Table
 - TableToolbar

## <a name="Additional-Plugins">Additional Plugins</a>
 - Alignment
 - Autosave
 - Highlight
 - PendingActions
 - SimpleUploadAdapter
 - Font
 - ImageResize
 - TodoList

## Documentation

See:

* [Installation](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/installation.html) for how to install this package and what it contains.
* [Basic API](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/basic-api.html) for how to create an editor and interact with it.
* [Configuration](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/configuration.html) for how to configure the editor.
* [Creating custom builds](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/development/custom-builds.html) for how to customize the build (configure and rebuild the editor bundle).

## Quick start

First, install the build from npm:

```bash
npm install --save ckeditor5-build-classic-plus
```

And use it in your website:

```html
<div id="editor">
	<p>This is the editor content.</p>
</div>
<script src="./node_modules/ckeditor5-build-classic-plus/build/ckeditor.js"></script>
<script>
	ClassicEditor
		.create( document.querySelector( '#editor' ) )
		.then( editor => {
			window.editor = editor;
		} )
		.catch( err => {
			console.error( err.stack );
		} );
</script>
```

Or in your JavaScript application:

```js
import ClassicEditor from 'ckeditor5-build-classic-plus';

// Or using the CommonJS version:
// const ClassicEditor = require( 'ckeditor5-build-classic-plus' );

ClassicEditor
	.create( document.querySelector( '#editor' ) )
	.then( editor => {
		window.editor = editor;
	} )
	.catch( err => {
		console.error( err.stack );
	} );
```

**Note:** If you are planning to integrate CKEditor 5 deep into your application, it is actually more convenient and recommended to install and import the source modules directly (like it happens in `ckeditor.js`). Read more in the [Advanced setup guide](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/advanced-setup.html).

## License

Licensed under the terms of [GNU General Public License Version 2 or later](http://www.gnu.org/licenses/gpl.html). For full details about the license, please check the `LICENSE.md` file or [https://ckeditor.com/legal/ckeditor-oss-license](https://ckeditor.com/legal/ckeditor-oss-license).
