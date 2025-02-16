# News

## 3.2.2 - 2019-06-03 {#version-3-2-2}

### Fixes

  * xpath: Fixed a bug for equality and relational expressions.
    [GitHub#17][Reported by Mirko Budszuhn]

  * xpath: Fixed `boolean()` implementation.

  * xpath: Fixed `local_name()` with nonexistent node.

  * xpath: Fixed `number()` implementation with node set.
    [GitHub#18][Reported by Mirko Budszuhn]

### Thanks

  * Mirko Budszuhn

## 3.2.1 - 2019-05-04 {#version-3-2-1}

### Improvements

  * Improved error message.
    [GitHub#12][Patch by FUJI Goro]

  * Improved error message.
    [GitHub#16][Patch by ujihisa]

  * Improved documentation markup.
    [GitHub#14][Patch by Alyssa Ross]

### Fixes

  * Fixed a bug that `nil` variable value raises an unexpected exception.
    [GitHub#13][Patch by Alyssa Ross]

### Thanks

  * FUJI Goro

  * Alyssa Ross

  * ujihisa

## 3.2.0 - 2019-01-01 {#version-3-2-0}

### Fixes

  * Fixed a bug that no namespace attribute isn't matched with prefix.

    [ruby-list:50731][Reported by Yasuhiro KIMURA]

  * Fixed a bug that the default namespace is applied to attribute names.

    NOTE: It's a backward incompatible change. If your program has any
    problem with this change, please report it. We may revert this fix.

    * `REXML::Attribute#prefix` returns `""` for no namespace attribute.

    * `REXML::Attribute#namespace` returns `""` for no namespace attribute.

### Thanks

  * Yasuhiro KIMURA

## 3.1.9 - 2018-12-20 {#version-3-1-9}

### Improvements

  * Improved backward compatibility.

    Restored `REXML::Parsers::BaseParser::UNQME_STR` because it's used
    by kramdown.

## 3.1.8 - 2018-12-20 {#version-3-1-8}

### Improvements

  * Added support for customizing quote character in prologue.
    [GitHub#8][Bug #9367][Reported by Takashi Oguma]

    * You can use `"` as quote character by specifying `:quote` to
      `REXML::Document#context[:prologue_quote]`.

    * You can use `'` as quote character by specifying `:apostrophe`
      to `REXML::Document#context[:prologue_quote]`.

  * Added processing instruction target check. The target must not nil.
    [GitHub#7][Reported by Ariel Zelivansky]

  * Added name check for element and attribute.
    [GitHub#7][Reported by Ariel Zelivansky]

  * Stopped to use `Exception`.
    [GitHub#9][Patch by Jean Boussier]

### Fixes

  * Fixed a bug that `REXML::Text#clone` escapes value twice.
    [ruby-dev:50626][Bug #15058][Reported by Ryosuke Nanba]

### Thanks

  * Takashi Oguma

  * Ariel Zelivansky

  * Jean Boussier

  * Ryosuke Nanba
