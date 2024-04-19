# Expand Parameters
```bash
local -r unexpanded="${1}"
eval EXPANDED="$(echo "$unexpanded" | cut -d' ' -f2)"
echo "${EXPANDED}"
```

As a function.
```bash
#!/bin/bash

function expand_var() { 
    local -r unexpanded="${1}" 
    eval expanded="$(echo "$unexpanded" | cut -d' ' -f2)" 
    echo "$expanded" 
}

user="$(expand_var "$with_default")" 
echo "User: $user"
```

Input string: `user: ${DB_USER:-postgres}`

To set up the test string it was necessary to prevent premature expansion. Which was made possible by using single quotes.

```bash
template='user: ${DBA_USER:-postgres}' 
echo "Input string: $template" 
with_default=$(echo "$template" | cut -d' ' -f2) 
echo "With default: $with_default"
```

Within single quotes, we don’t interpolate anything:

```bash
$ text='a $(echo b) c'
$ echo "${text}"
a $(echo b) c
```

Using grep, it can be done as follows:

```bash
grep -oP "from\s+\K\w+" input.txt

```
Where,
```
-o  ==>  option for printing only the matching part of the line
-P  ==>  use perl-regexp
\K  ==>  do not print that comes before \K (zero-width look-behind assertion)
\w  ==>  match word characters
```

Or:
```
awk '{for (I=1;I<NF;I++) if ($I == "from") print $(I+1)}' file
```
