# Export UTF-8

Export UTF-8 is a way to export text encoded as UTF-8, which a lot of other software requires for input.

## Installation

 1. Import the "Modules" > "Export UTF-8" script folder and all its contents into your file's "Modules" folder.

## Usage

There are two techniques for exporting files encoded as UTF-8. The script-based method is requires less set-up on your part, but is slower. The record export method is much faster, but requires more set-up on your part. Both techniques require that you go to a container field to export files from before calling the module scripts. See the "Export UTF-8: READ ME" script in the module for script use examples.

Script parameters and results are formatted as [Let Notation](http://filemakerstandards.org/pages/viewpage.action?pageId=5668879). In the event of an error, scripts will return the results:
- $errorCode: The codes of any errors encountered during operation.
- $errorMessage: A human-readable message reporting any errors.
$errorCode will be returned with the value 0 if there was no error.

### Encode via Script

Call the "Export Text as UTF-8 ( $textToExport ) { $filePath }" script using the parameters:
- $textToExport (required): The text to encode as UTF-8 and export
- $filePath (optional): The file path to export $textToExport to

### Encode via XSLT

Call the "Export UTF-8 XSLT File" script, which return the file path to the exported XSLT file as a script result. You can then use that XSLT to transform the output of your export. If used more than once in a single session, the "Export UTF-8 XSLT File" script will simply return the path of the file it already exported (which it saved to a global variable) rather than re-exporting the XSLT.

## License

Anyone may do anything with this software for any purpose. There is no warranty.

## Credits

Thanks to [Ryan Simms](https://beezwax.net/beez/301) for work leading to the XSLT-based functionality.