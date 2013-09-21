# google-fonts [![experimental](http://hughsk.github.io/stability-badges/dist/experimental.svg)](http://github.com/hughsk/stability-badges) #

[![google-fonts](https://nodei.co/npm/google-fonts.png?mini=true)](https://nodei.co/npm/google-fonts)

A small helper library for embedding
[Google Fonts](http://www.google.com/fonts) onto your page.

## Usage ##

## `fonts(list)` ##

Given a list of fonts (see below), returns a string like this one (minus the
whitespace) that you can include in a template:

``` html
<link
  href='http://fonts.googleapis.com/css?family=Cantora+One|Ropa+Sans:400,400italic'
  rel='stylesheet'
  type='text/css'
>
```

## `fonts.add(list)` ##

Given the same list of fonts, you can add them directly to your page using
this method (assuming you're using something like
[browserify](http://browserify.org)).

Useful for quick demos/prototypes, but if you want to avoid the flash of
unstyled text then stick with pasting their snippet in your HTML.

The list should be formatted like so:

``` javascript
fonts.add({
    'Ropa Sans': ['400', '400italic']
  , 'Source Sans Pro': true
  , 'Raleway': 400
})
```

Where each key is a font name, and each value is an array of styles to include.
You can also pass a single style, or `true` to include all of the available
ones for that font.
