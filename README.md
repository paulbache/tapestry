# CSS guidelines

## Goals
* Maintainable OOCSS components
* Scalable code

## Naming

* BEM - Block-element--modifier
* PascaleCase for component name
* camelCase for component childs
* Lowercase for modifiers
 * Use `is-*` and `has-*` modifiers when needed

```html
<div class="Component Component--modifier is-state">
  <div class="Component-child"></div>
  <div class="Component-otherChild"></div>
</div>
```

## Spacing and indentation

* Two spaces indent
* Space after `:` property declaration
* Space before `{` rule declaration
* Closing braces on a new line

```css
.Component {
  display: inline-block;
}
```

## Else

 * Never use IDs
 * No magic number
 * Only use `!important` on utility classes
 * Max nesting level: 3



# Tools

## Visual tests

### Installation

```
npm install
npm install -g phantomjs
npm install -g casperjs
```

## Pre-commit and pre-push

### Installation

```bash
npm run pre-commit
npm run pre-push
```

### NPM scripts

Tests are run with Travis and have to be updated before branch merges. They can be run locally with these following commands.

```js
npm run lint // linter
npm run vt:refs // build references
npm run vt:compare // compare references with actual HEAD
```

### Bypass

To bypass the pre-commit, just add `-n` option.

```
git ci -n
git ci -nm "My commit message"
```
