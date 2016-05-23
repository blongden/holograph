# Holograph (alpha)

Holograph is a NPM module that parses comments in your CSS and turns them into a beautiful style guide. It is initially a port of the excellent work done by the [Hologram Ruby gem](https://trulia.github.io/hologram/) and aims to be compatible with most of its features.

In addition to features found in Hologram, Holograph includes:
* a responsive version of the [Hologram GitHub Template](https://github.com/wearecube/hologram-github-theme) with some minor alterations to content styles
* support for displaying multiple [colour palettes](#colour-palettes)

## Installation

Install the latest release from npm with (add --save or --save-dev to add the dependency to your project)

`npm install holograph`

## Configuration

Copy the template config into your project root

`cp node_modules/holograph/holograph_config.yml .`

The config file contains inline documentation for each entry, update it at this point to match your project.

## Usage

The binary takes no parameters and just reads all options from the config file

`node_modules/.bin/holograph`

The default build location is `./holograph/`. You can configure this by setting the `destination` value in `holograph_config.yml`.

### Documenting your styles

Holograph will scan for stylesheets (`.css`, `.scss`, `.sass`, `.less`, `.styl`) within the source directory defined in your configuration. It will find Holograph comments and generate style guide sections from your comment's settings and content.

Sample comment:

    /*doc
    ---
    title: Buttons
    name: buttons
    category: atoms
    ---

    Button styles can be applied to any element. Typically you'll want to use either a `<button>` or an `<a>` element:

    ```html_example
    <button class="button">button element</button>
    <a class="button" href="http://www.github.com">link element</a>
    ```

    ## Button types
    
    You can also show examples in markdown tables as follows:

    Button                                                                  | Class
    ----------------------------------------------------------------------- | -----------------
    <button class="button">default button</button>                          | `button`
    <button class="button button--primary">primary button</button>          | `button button--primary`
    <button class="button button--secondary">secondary button</button>      | `button button--secondary`
    <button class="button" disabled>disabled</button>                       | `button:disabled`
    */

For more information and syntax for these comments, see [documenting your styles and components](https://github.com/trulia/hologram#documenting-your-styles-and-components) in the Hologram repo.

### Colour palettes

Holograph allows creation of colour palettes from your proprocessor stylesheets (`.css`, `.scss`, `.sass`, `.less`, `.styl`). This feature is new for Holograph and is not found in Ruby Hologram.

For documentation, see [how to use colour palettes](https://github.com/blongden/holograph/wiki/How-to-use-colour-palettes).

## How to test the software

## Known issues

### Incomplete features

* content and configuration for `index.html`
* `parent` option
* support for JavaScript content
* [referencing other components](https://github.com/trulia/hologram#referencing-other-components)

### Features not in scope
* support for colour values in palettes that require compilation, such as `darken($brand-primary, 10%)` and nested colour variables

## Getting help

If you have questions, concerns, bug reports, etc, please file an issue in this repository's [issue tracker](https://github.com/blongden/holograph/issues).

## Getting involved

## More about the project

### Contributors
* [Ben Longden](https://twitter.com/blongden)
* [Laura Kishimoto](https://twitter.com/chicgeek)

### Open source licensing info
* [Terms](TERMS.md)
* [License](LICENSE)
* [CFPB Source Code Policy](https://github.com/cfpb/source-code-policy/)

### Credits and references

* [hologram](https://trulia.github.io/hologram/)
* [hologram-github-template](https://github.com/wearecube/hologram-github-theme)
