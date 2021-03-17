# Simple Webpack Encore

Simple Webpack Encore implementation, with `sass-loader` for css.
This package provides a simple recipe for webpack encore
to use without `Stimilus` integration and `webpack-encore-bundle`.

## Installation

```bash
composer require sulu/webpack-encore
```

The symfony/flex recipe should now generate the CSS/JS setup
in your project directories.

### Build CSS / JS

```bash
cd assets/website
npm install
npm run build
```

### Embed JS / CSS

The JS:

```twig
<script src="{{ asset('build/website/main.js', 'website') }}"></script>
```

The CSS:

```twig
<link href="{{ asset('build/website/main.css', 'website') }}" rel="stylesheet">
```

After embedding you should see a colored background. This means
your build did successfully work.

### Remove Package

Now the best is you can savely remove this package.
That symfony flex will not remove the recipe files we just checkout
the composer files.

```bash
git checkout symfony.lock composer.lock composer.json
```

### Preloading CSS / JS

If you want to preload the CSS or CSS you can do this using the
symfony/web-link package:

```bash
composer require symfony/web-link
```

After this just wrap the `asset` function in `preload` e.g.:

The JS:

```twig
<script src="{{ preload(asset('build/website/main.js', 'website')) }}"></script>
```

The CSS:

```twig
<link href="{{ preload(asset('build/website/main.css', 'website')) }}" rel="stylesheet">
```
