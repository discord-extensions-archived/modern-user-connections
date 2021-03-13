# v1.2.7
Added support for the osu! connection for the Better User Connections plugin.

# v1.2.6
I learnt something new with mixins: you can have varaibles inside of attributes. I've changed it to where the mixins make use of this feature, which makes everything less of an eye sore and easier to add. Here's an example of that:
```scss
// Taking a close look, you can see how this is applied.
@mixin connection($connectionType, $connectionBG, $connectionBorder) {
    [alt="#{$connectionType} Logo"] + .connectedAccountNameInner-1phBvE::after {
        background-color: $connectionBG;
        box-shadow: -2px 0 0 0 $connectionBorder;
    }
}
                 // $connectionType  $connectionBorder
@include connection(GitHub, #24292E, #d9dadb);
                         // $connectionBG
```

# v1.2.5
Repo renmame as well as slight tweaks.

# v1.2.4
Some small yet kinda big changes.
- Redid the sorting for basically everything, usin' some mixins now to fuel my laziness.
- Redid README.md
- Added support for Vizality, BetterDiscord and Web.
- Added a changelog. (you're reading it right now!)
- Fixed the check mark becoming less visible as well.
