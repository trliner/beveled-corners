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

    @mixin border-bevel($background-color: unquote("#aaa"), $corner-bevel: unquote("20"), $corner-top-left-bevel: true, $corner-top-right-bevel: true, $corner-bottom-right-bevel: true, $corner-bottom-left-bevel: true, $padding: $corner-bevel)

This will create a gray box with a corner bevel value of `20px`.

    .module {
        @include corner-bevel();
    }

This will create a yellow box.

    .module {
        @include corner-bevel("Yellow");
    }

We can isolate the corners with boolean values:

    .module {
        @include corner-bevel("Yellow", 20, true, false, trua, false);
    }

##Demo

- Demo in CodePen
- Article in my blog explaining things more detailed

<p data-height="608" data-theme-id="0" data-slug-hash="rhlwG" data-user="hilja" data-default-tab="result" class='codepen'>See the Pen <a href='http://codepen.io/hilja/pen/rhlwG'>rhlwG</a> by hilja (<a href='http://codepen.io/hilja'>@hilja</a>) on <a href='http://codepen.io'>CodePen</a></p>
<script async src="//codepen.io/assets/embed/ei.js"></script>