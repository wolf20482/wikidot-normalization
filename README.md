Simple JavaScript library to provide Wikidot-compatible string normalization.

There isn't a JavaScript implementation of this at the time of writing, only a [PHP implementation in Wikidot (and also newer Wikijump) code](https://github.com/scpwiki/wikijump/blob/develop/web/php/Utils/WDStringUtils.php) and a Rust implementation by the SCP Wiki Tech Team available [here](https://github.com/scpwiki/wikidot-normalize). Since I'm developing a Discord bot in JavaScript that has a feature users to search articles, I feel like I need to make this package to make it easier for the community and make code reuse easier.

## Wikidot page name string form

According to [this](https://github.com/scpwiki/wikidot-normalize):
* All ASCII is lowercase.
* All characters outside of `:`, `a-z`, `0-9`, or `-` are replaced with dashes.
* Underscores are only permitted as the first character.
* Any leading or trailing dashes are removed.
* Any set of multiple dashes are replaced with a single dash.
* Any set of multiple colons are replaced with a single colon.

Examples:
* `"Level 0"` -> `"level-0"`
* `"-test-"` -> `"test"`
* `"bottom--Text"` -> `"bottom-text"

Published under MIT License.

## Install

```
$ npm install wikidot-normalization
```