# prettier-plugin-flavours

This plugin for [Prettier](https://prettier.io) maps a bunch of more or less _exotic_ file types to languages already supported by Prettier.

## Why this plugin?

Recently i had to work with several file types not supported by Prettier and really missed the handy format on save feature in VSCode.

I tried changing [VSCodes's language identifier](https://code.visualstudio.com/docs/languages/identifiers) like in this example for Liquid templates:

```json
"files.associations": {
  "*.liquid": "html"
}
```

This works in the way that Prettier will process those files, but highlighting and auto-completion for Liquid specific syntax breaks.

To get around this issue, this plugin maps Prettier's existing parsers to new file extensions.

## Installation

```sh
npm install -D https://github.com/nicolaibach/prettier-plugin-flavours.git
```

## Usage

> Plugins are automatically loaded if you have them installed in the same `node_modules` directory where `prettier` is located.
>
> –– https://prettier.io/docs/en/plugins.html#using-plugins

## Language Mapping

| Language                                                                                | File Extension | Prettier Parser |
| :-------------------------------------------------------------------------------------- | :------------- | --------------- |
| [Liquid](https://github.com/Shopify/liquid)                                             | .liquid        | HTML            |
| [JavaScript for Automation (JXA)](https://apple-dev.groups.io/g/jxa/wiki/JXA-Resources) | .jxa           | Babel           |

## Resources

- [Prettier Plugins Documentation](https://prettier.io/docs/en/plugins.html)
- [Linguist list of languages](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml)
- [Visual Studio Code Language Identifiers](https://code.visualstudio.com/docs/languages/identifiers)

## License

This project is [MIT](https://github.com/nicolaibach/prettier-plugin-flavours/blob/master/LICENSE) licensed.
