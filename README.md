# Shields [![Gittip](http://img.shields.io/gittip/shields.io.png)](https://www.gittip.com/Shields.io/) [![npm version](http://img.shields.io/npm/v/gh-badges.svg)](https://npmjs.org/package/gh-badges) [![build status](http://img.shields.io/travis/badges/gh-badges.svg)](https://travis-ci.org/badges/gh-badges)

A legible & concise status badge solution for third-party codebase services.

Make your own badges [here][badges]!

[badges]: <http://img.shields.io>

## Services using the Shields standard
- [Code Climate](https://codeclimate.com/changelog/510d4fde56b102523a0004bf)
- [Coveralls](https://coveralls.io/r/kaize/nastachku)
- [Gemfury/RubyGems](http://badge.fury.io/)
- [Gemnasium](http://blog.tech-angels.com/post/43141047457/gemnasium-v3-aka-gemnasium)
- [Travis CI](http://about.travis-ci.org/docs/user/status-images/)
- [Scrutinizer CI](https://scrutinizer-ci.com/)
- [Semaphore](https://semaphoreapp.com)

## Problem
Many GitHub repos sport badges for things like:
- [Travis CI](https://travis-ci.org/) build status:

![travis badge](http://f.cl.ly/items/2H233M0I0T43313c3h0C/Screen%20Shot%202013-01-30%20at%202.45.30%20AM.png)

- [Gemnasium](https://gemnasium.com/) dependency checks:

![gemnasium badge](http://f.cl.ly/items/2j1D2R0q2C3s1x2y3k09/Screen%20Shot%202013-01-30%20at%202.46.10%20AM.png)

- [Code Climate](http://codeclimate.com):

![code climate badge](http://f.cl.ly/items/0H2O1A3q2b3j1D2i0M3j/Screen%20Shot%202013-01-30%20at%202.46.47%20AM.png)

- [RubyGems](http://rubygems.org) released gem version:

![rubygems badge](http://f.cl.ly/items/443X21151h1V301s2s3a/Screen%20Shot%202013-01-30%20at%202.47.10%20AM.png)

As you can see from the zoomed 400% versions of these badges above, nobody is (really) using the same badge file and at normal size, they're hardly legible. Worst of all, they're completely inconsistent. The information provided isn't of the same kind on each badge. The context is blurry, which doesn't make for å straightforward understanding of how these badges are relevant to the project they're attached to and what information they provide.

## Solution
As you can see below, without increasing the footprint of these badges, I've tried to increase legibility and coherence, removing useless text to decrease the horizontal length in the (likely) scenario that more of these badge thingies crop up on READMEs all across the land.

![Badge design](https://rawgithub.com/badges/shields/master/spec/proportions.png)

We have an effort to produce similar-looking SVGs through a web service at
<http://img.shields.io>. That ensures that we are retina-ready.

## Examples

What kind of meta data can you convey using badges?

- test build status: `build | failing`
- code coverage percentage: `coverage | 80%`
- stable release version: `version | 1.2.3`
- package manager release: `gem | 1.2.3`
- status of third-party dependencies: `dependencies | out-of-date`
- static code analysis GPA: `code climate | 3.8`
- [semver](http://semver.org/) version observance: `semver | 2.0.0`
- amount of [gittip](http://gittip.com) donations per week: `tips | $2/week`

## Retina Ready
Since one of the major concerns is legibility, it's impossible to ignore how badges will render on retina (high DPI) displays.

As suggested by @kneath, badges displayed with an HTML image tag (instead of the easier Markdown image tag) can be given a fixed height to force an image that is actually double the resolution into a 50% smaller image, which will display properly for both retina and non-retina screens.

Here's an example with the following code:

```html
<img src="https://raw.github.com/badges/shields/master/static/shields_white@2x.png" height="143" alt="Retina-ready Shields example" />
```

<img src="https://raw.github.com/badges/shields/master/static/shields_white@2x.png" height="143" alt="Retina-ready Shields example" />

All our badges aren't yet compatible with this but we're working on updating them soon. Look for image filenames with `@2x` suffixes, those will be the pixel doubled versions.

Note: They were pixel doubled manually in Photoshop, not after the fact.

## Font
The font chosen in the specification is the Apache licensed Open Sans Regular available from [Google Web Fonts](http://www.google.com/webfonts/specimen/Open+Sans).

## Specification
See [SPECIFICATION.md](spec/SPECIFICATION.md).

## Installation Instructions
See [INSTALL.md](INSTALL.md).

## Contributions
See [CONTRIBUTING.md](CONTRIBUTING.md).

## License
See [LICENSE.md](LICENSE.md).

[gem]: https://github.com/badges/badgerbadgerbadger

