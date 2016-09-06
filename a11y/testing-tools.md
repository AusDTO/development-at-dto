# Integrated tools for unit accessibility testing

## Table of contents

1. [Resources](#resources)
1. [Tools](#tools)

## Resources

- [The Magic of Automated Accessibility Testing](1), Marcy Sutton 2015

## Tools

**Note:** Unless otherwise stated, all tools are open source.

- [a11y - Web accessibility audits powered by the Chrome Accessibility Developer Tools](2)
  - Node package than you can easily build into Gulp/Grunt (+ many other build processes) for automated accessibility testing every time the project is updated.
  - Tests against the [Chrome Accessibility Tools Audit Rules](3).
- [AccessLint CI - Automated Web Accessibility Testing](4)
  - AccessLint CI automatically comments on your pull-requests instead of triggering build failures, and only tells you what has changed since the last build..
  - Built on [axe-core](5).
  - Use AccessLint CI with middleman and CircleCI.
- [aXe - the Accessibility Engine](6)
  - JavaScript accessibility checker that does not need to be 'installed' as it is just JS that runs on the page. Can be run in a browser environment to give a good accessibility report on technical issues in the browser's console.
  - Tests against the [axe-core rules](7).
- [Pa11y - Your automated accessibility testing pal](8)
  - Very comprehensive accessibility command line tool. Can be used in a variety of different ways and environments. This offers a really good output of errors and suggestions on how to fix them.
  - Tests against [Squiz’s HTMLsniffer WCAG 2.0 criteria](9).
- [Protractor Accessibility Plugin](10)
  - The accessibility plugin runs a set of accessibility audits on your web app. It is published as an npm module.
  - Can be configured to use [Chrome Accessibility Developer Tools](3) or [Tenon.io](11).
- [Tenon.io](11) (paid tool, not open source)
  - Accessibility testing tool in that it is aimed at offering unprecedented flexibility in tooling for designers developers testers and content authors.
  - Tests against [Tenon's own criteria](12).

--

[1]: http://marcysutton.github.io/a11y-automated-testing/#/
[2]: https://addyosmani.com/a11y/
[3]: https://github.com/GoogleChrome/accessibility-developer-tools/wiki/Audit-Rules
[4]: https://robots.thoughtbot.com/introducing-accesslint-web-accessibility-testing-in-ci
[5]: https://github.com/dequelabs/axe-core
[6]: http://www.deque.com/products/axe/
[7]: https://github.com/dequelabs/axe-core/blob/master/doc/rule-descriptions.md
[8]: http://pa11y.org/
[9]: http://squizlabs.github.io/HTML_CodeSniffer/Standards/WCAG2/
[10]: https://github.com/angular/protractor-accessibility-plugin
[11]: https://tenon.io/
[12]: https://tenon.io/documentation/what-tenon-tests.php
