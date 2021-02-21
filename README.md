# Simple Webpack Encore

Simple Webpack Encore implementation, with `sass-loader` for css.
This package provides a simple recipe for webpack encore
to use without `Stimilus` integration and `webpack-encore-bundle`.

## Installation

```bash
composer require l91/webpack-encore
```

The symfony/flex recipe should now generate the CSS/JS setup
in your project directories.

### Build CSS / JS

```bash
cd assets/website
npm install
npm run build
```

### Embed JS

```twig
<script src="{{ asset('build/website/app.js', 'website') }}"></script>
```

### Embed CSS

```twig
<link href="{{ asset('build/website/app.css', 'website') }}" rel="stylesheet">
```

### Remove Package

Now the best is you can savely remove this package.
That symfony flex will not remove the recipe files we just checkout
the composer files.

```bash
git checkout symfony.lock composer.lock composer.json
```
