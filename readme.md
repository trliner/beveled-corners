#CSS Beveled Corner Mixin for Sass

Creates beveled corners in same fashion as `border-radius`.

##Wins

- Works down to IE 8
- No extra elements
- Can be applied to any element like any styling
- No images or other crap

##Fails

- Margins are a bit funny, see the demo
- Can't have border around the box, but you can simulate border with `filter: drop-shadow();`. It only works in Chrome but it's something

##Usage

Configurable arguments:

- `$background-color` default `#aaa`, can be hex or RGBA
- `$corner-bevel` bevel amount
- `$corner-top-left-bevel` true or false, default true, false makes the corner non bevel
- `$corner-top-right-bevel` boolean
- `$corner-bottom-right-bevel` boolean
- `$corner-bottom-left-bevel` boolean
- `$padding` effects only to sides

The following will create a gray box with a corner bevel value of `20px`:

    .module {
        @include corner-bevel();
    }

This will create a yellow box:

    .module {
        @include corner-bevel("Yellow");
    }

We can isolate the corners with boolean values:

    .module {
        @include corner-bevel("Yellow", 20, true, false, trua, false);
    }

##Demo and more

- Demo in [CodePen](http://codepen.io/hilja/pen/rhlwG)
- [Article in my blog](http://clubmate.fi/css-beveled-co…2-a-sass-mixin/) explaining things in more detail