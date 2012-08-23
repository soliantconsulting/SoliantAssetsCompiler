# SoliantAssetCompiler

AssetsCompiler is a tiny Zend Framework 2 Module that brute-force copies all files in each /module/*/public directory to /public/assets/ directory which must exist and _must be writable_ by php in order for the module to run.


## Setup
`/modules/MyModule/public/` should contain all the required public assets for the module, including .js, .css, .png, .mov, .cdr files and directories; everything under public is copied exactly.

## Usage

To access your module assets use the convention `/assets/ModuleName/path/file.ext`.

## Example

An html page would reference a public asset such as `<img src="/assets/ModuleName/logo.gif">`

## Caution
Only run this module in your development environment, and only when you need it, as it uses brute force, and will copy ever asset every time. You could chose to run it as part of an installer, or based on environment config variable.
