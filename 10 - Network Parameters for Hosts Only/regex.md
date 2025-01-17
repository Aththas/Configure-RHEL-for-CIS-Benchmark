# The cmd:
    $ sudo grep -P '^(?!#).*[\s]*net.ipv4.conf.all.send_redirects.*$' /etc/sysctl.d/*.conf

### Explanation:
**-P**: Use Perl-compatible regular expressions.

**'^(?!#).*[\s]*net.ipv4.conf.all.send_redirects.*$'**: The regular expression to search for

1. **^** : Match the start of a line.

2. **(?!#)** : Negative lookahead to ensure the line does not start with # (i.e., it's not commented out).

3. **.** : Matches any character except newline.

4. *: Matches 0 or more of the preceding character (in this case, any character).

5. **[\s]*** : Matches 0 or more whitespace characters (spaces, tabs, etc.).

6. **net.ipv4.conf.all.send_redirects** : The specific string we are looking for.

7. .* : Matches 0 or more of any character (allowing for anything after the target string).

8. **$** : Asserts the position at the end of the line.

**$** explanation:
**abc$**

abc: Matches because abc is at the end of the line.

abcd: Does not match because abc is followed by d, so it's not at the end of the line.

efgabc: Matches because abc is at the end of the line.




# cmd:
    $ sudo grep -q -m 1 -i "^net.ipv4.conf.all.send_redirects\\>" /etc/sysctl.conf

**-q**: Quiet mode, suppress output.

**-m 1**: Stop reading after the first match.

**-i**: Case-insensitive search.

**\\>**: Ensures the match ends at a word boundary, making sure it matches the exact parameter and not a longer name starting with the same string.

Matches:

net.ipv4.conf.all.send_redirects = 1

net.ipv4.conf.all.send_redirects 0

Does Not Match:

net.ipv4.conf.all.send_redirects_something_else = 1

# cmd:
    $ sudo sysctl --system

**--system**: Apply all the settings from the sysctl configuration files
