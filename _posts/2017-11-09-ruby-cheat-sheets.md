---
published: true
---

I will continually be adding to this blog post which will provide myself and hopefully others a quick reference to various cheats or quick references to all things Ruby. If you have a link to a resource that needs to be here please feel free to message me a link. 


## String Escape Sequences

| Escape | What it does |
| -- | -- |
| \\ | Backslash () |
| \' | Single-quote (') |
| \" | Double-quote (") |
| \a | ASCII bell (BEL) |
| \b | ASCII backspace (BS) |
| \f | ASCII formfeed (FF) |
| \n | ASCII linefeed (LF) |
|\r | ASCII Carriage Return (CR) |
|\t | ASCII Horizontal Tab (TAB) |
|\uxxxx | Character with 16-bit hex value xxxx (Unicode only) |
|\v | ASCII vertical tab (VT) |
|\ooo |	Character with octal value ooo |
|\xhh |	Character with hex value hh |

## Truth Terms

| Characters | Phrase |
| -- | -- |
| && | (and) |
| \\|\\| | (or) |
| ! | (not) |
| != | (not equal) |
| == | (equal) |
| >= | (greater-than-equal) |
| <= | (less-than-equal) |
| true | |
| false | |

## Truth Tables

| NOT | true? |
| -- | -- |
| !false | true |
| !true | false |

| OR(\|\|) | true? |
| -- | -- |
| true \|\| false | true |
| true \|\| true | true |
| false \|\| true | true |
| false \|\| false | false |

| AND(&&) | true? |
| -- | -- |
| true && false | false |
| true && true | true |
| false && true | false |
| false && false | false |

| NOT OR | true? |
| -- | -- |
| not (true \|\| false | false|
| not (true \|\| true | false|
| not (false \|\| true | false|
| not (false \|\| false | false|

| NOT AND | true? |
| -- | -- |
| !(true && false) | true |
| !(true && true) | false |
| !(false && true) | true |
| !(false && false) | true |

| != | true? |
| -- | -- |
| 1 != 0 | true |
| 1 != 1 | false |
| 0 != 1 | true |
| 0 != 0 | false |

| == | true? |
| -- | -- |
| 1 == 0 | false |
| 1 == 1 | true |
| 0 == 1 | false |
| 0 == 0 | true |
