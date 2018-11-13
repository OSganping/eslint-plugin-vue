# enforce `v-on` directive style (vue/v-on-style)

- :gear: This rule is included in `"plugin:vue/strongly-recommended"` and `"plugin:vue/recommended"`.
- :wrench: The `--fix` option on the [command line](https://eslint.org/docs/user-guide/command-line-interface#fixing-problems) can automatically fix some of the problems reported by this rule.

This rule enforces `v-on` directive style which you should use shorthand or long form.

## :book: Rule Details

:-1: Examples of **incorrect** code for this rule:

```html
<div v-on:click="foo"/>
```

:+1: Examples of **correct** code for this rule:

```html
<div @click="foo"/>
```

:-1: Examples of **incorrect** code for this rule with `"longform"` option:

```html
<div @click="foo"/>
```

:+1: Examples of **correct** code for this rule with `"longform"` option:

```html
<div v-on:click="foo"/>
```

## :wrench: Options
Default is set to `shorthand`.

```json
{
  "vue/v-on-style": [2, "shorthand" | "longform"]
}
```

- `"shorthand"` (default) ... requires using shorthand.
- `"longform"` ... requires using long form.

## Related links

- [Style guide - Directive shorthands](https://vuejs.org/v2/style-guide/#Directive-shorthands-strongly-recommended)

## :mag: Implementation

- [Rule source](https://github.com/vuejs/eslint-plugin-vue/blob/master/lib/rules/v-on-style.js)
- [Test source](https://github.com/vuejs/eslint-plugin-vue/blob/master/tests/lib/rules/v-on-style.js)
