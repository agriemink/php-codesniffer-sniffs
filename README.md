Moxio PHP_CodeSniffer sniffs
=============================
This is a collection of our custom PHP_Codesniffer sniffs for detecting potential bugs 
and unexpected behavior in PHP code. It may be used as a ruleset on its own, but it is mainly
intended as a set of separate sniffs that can be integrated into other standards.

Description of sniffs
---------------------
_More sniffs will be added soon._

**Moxio.PHP.DisallowBareContinueInSwitch**: Disallows the `continue` statement without a numeric
argument when used directly within a `switch`-`case`. This prevents silent bugs caused by PHP 
considering `switch` [to be a looping structure](http://php.net/manual/en/control-structures.switch.php).

**Moxio.PHP.DisallowImplicitLooseComparison**: Disallows implicit non-strict comparisons by functions
like `in_array` and `array_search`. Requires that the `$strict`-parameter to these functions is
explicitly set. This prevents hidden bugs due to [counter-intuitive behavior of non-strict 
comparison](https://twitter.com/fabpot/status/460707769990266880).

License
-------
These sniffs are released under the MIT license.
