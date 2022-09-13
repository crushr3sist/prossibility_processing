
# Algorithm

```py
def separate_values(str):
    return list(str)


def all_perms(elements):
    if len(elements) <= 1:
        yield elements
    else:
        for perm in all_perms(elements[1:]):
            for i in range(len(elements)):
                yield perm[:i] + elements[:1] + perm[i:]


if __name__ == "__main__":
    indexer = 0
    for perm in all_perms(separate_values(arr := input("Enter the string: "))):
        print("".join(perm))
        indexer += 1
    print(f"there are {indexer} amounts of permutations possible of {arr}")
```
I made it faster :)

from 0.00599 seconds
to   0.00487 seconds

# Output:

```py
>>> Enter the string: abc
>>> abc
>>> bac
>>> bca
>>> acb
>>> cab
>>> cba
>>> there are 6 amounts of permutations possible of abc
```
