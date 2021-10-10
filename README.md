# dicesum

Create human readable hash strings composed of 10 different words based on a md5 hash. The list of words is equivalently useful in calculating a checksum and comparing it compared to md5, but it's more readable by humans and thus easier to remember hashes or distinguish them.

## Installation

**Requirements**

- python3


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

## How it works

A 128-bit md5 hash is padded with two 0 bits and divided into 10 chunks of 13 bits. Each chunk of 13 bits is used as an index number to get a word from a static wordlist of 8192 (= 2^13) unique words, resulting in a combination of 10 words. Thus, the combination of words should practically be as reliable as md5. Any use for cryptography is not adviced.
