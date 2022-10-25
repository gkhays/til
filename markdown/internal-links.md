# Internal, Relative Links in Markdown

This TIL works using simple relative links using the `#<anchor/heading>` convention. But in order to convert to PDF or in other Markdown viewers it is necessary to use embedded `HTML`.

```md
- [Introduction](#introduction)
- [Tools](#tools)

<a name="introduction"></a>

# Introduction

<a name="tools"></a>

# Tools
```
