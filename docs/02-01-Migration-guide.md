# Migration Guide

**First of all**: You are not required to convert your projects to use sentiment topics. All previous functionality is still available.

### Converting Topics to Sentiment Topics

To make use of the new functionality, convert your non-sentiment topics to sentiment topics:

![Merge](images/merge.gif)

1. Drag two corresponding non-sentiment topics, e.g. `Friendly` and `Unfriendly` onto each other. It doesn't matter which one you drag onto the other. A modal will then appear.
2. Activate *"Topic Sentiment"*
3. Adjust the *Topic Label* to be a **Neutral** version of the topic. In our example, this would be `Friendliness`
4. Choose which of the topics represented the *positive* and which represented the `negative` version.
5. Make sure the *sentiment labels* are correct. The *neutral* label can either be left empty (if it is the same as the topic label, it does not make sense to populate it).
6. Hit merge

<!-- theme: info -->
> The codes (numerical IDs) are copied from your previous topics and will thus stay consistent.

<!-- theme: warning -->
> #### Inheriting projects
>
> If you have multiple projects inheriting from each other and still show the old projects in your trend charts, please wait with migrating to the new structure for now.