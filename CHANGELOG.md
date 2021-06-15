# v1.3.1
Some fixes and adjustments / changes.
- Should now appear on the new user modal.
    - This closes **[issue #4](https://github.com/Discord-Theme-Addons/refined-user-connections/issues/4)**.
- Now using `@forward` and `@use` instead of `@import`.
- Some color adjustments.

# v1.3.0
Now using `@each` instead of `@mixins`. I feel like this is a way better system, tho generally it does the same thing.

Here are some other misc changes:
- Removed all usage of #app-mount as it's completely unnecessary.
- Changed to border-left instead of box-shadow.
- Some adjustments to margin and padding.
- Changed all rounding to 2px.
- Some file reconstructing.

# v1.2.8
Some small enhancements.
- Removed the unnecessary use of #app-mount. This shouldn't really change much.
- Updated some of the connection colors, original ones looked too virbant. The new colors look less virbant.

# v1.2.7
Added osu! connection support for the **[Better Connections](https://github.com/AAGaming00/better-connections)** plugin.

# v1.2.6
I learnt something new with mixins: you can have varaibles inside of attributes. I've changed it to where the mixins make use of this feature, which makes everything less of an eye sore and easier to add. Here's an example of that:
```scss
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
