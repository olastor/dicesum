# dicesum

Create human readable hash strings composed of 10 different words based on a md5 hash. The list of words is equivalently useful in calculating a checksum and comparing it compared to md5, but it's more readable by humans and thus easier to remember hashes or distinguish them.

## Installation

```sh
curl -L https://raw.githubusercontent.com/olastor/dicesum/main/dicesum.py -o /usr/local/bin/dicesum && chmod +x /usr/local/bin/dicesum
```

## Example

```
echo -n "test" > test.txt
dicesum test.txt
armrest-washhouse-denture-blank-devoutly-predefine-pony-campus-constrict-ranking	test.txt
```

You should see the exact same combination of strings when executing this.
