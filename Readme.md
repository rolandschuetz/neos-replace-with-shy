[![Latest Stable Version](https://poser.pugx.org/codeq/replacewithshy/v/stable)](https://packagist.org/packages/codeq/replacewithshy)
[![License](https://poser.pugx.org/codeq/replacewithshy/license)](LICENSE)

# Neos - Replace with Shy

Optional word-breaks are hard to enter in Neos CMS. This Neos package provides a helper to replace occurences of `||` with the Soft hyphen `&shy;`.

Thanks [jonnitto](https://github.com/jonnitto/) for developing this code, which I just packaged.


## Installation

Most of the time you want to use this package within your site package. Because of that, it is important to add the corresponding package to the composer from your theme package. Mostly this is the site packages located under `Packages/Sites/`. To install it correctly go to your theme package (e.g.`Packages/Sites/Foo.Bar`) and run following command:
```bash
composer require codeq/replacewithshy --no-update
```

The `--no-update` command prevent the automatic update of the dependencies. After the package was added to your theme `composer.json`, go back to the root of the Neos installation and run `composer update`. Et voilà! Your desired package is now installed correctly.

## Usage

1. Install with `composer require codeq/ReplaceWithShy`

2. Wrap any object with `||`with `&shy` to repalace in its output,
e.g. you would probably want to normalize full page output like this:

```
prototype(Page).@process.shy = CodeQ.ReplaceWithShy:ReplaceWithShy
```

## License

Licensed under MIT, see [LICENSE](LICENSE)
