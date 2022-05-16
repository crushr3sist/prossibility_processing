
# Algorithm

```py
# function to separate the values of the array
def separate_values(str):
    # split the string into a list
    return [char for char in str]


def all_perms(elements):
    # if the list is empty, return the empty list
    if len(elements) <= 1:
        yield elements
    else:
        # for each element in the list
        for perm in all_perms(elements[1:]):
            # for each position in the list
            for i in range(len(elements)):
                # yield the permutation with the element inserted
                yield perm[:i] + elements[0:1] + perm[i:]


if __name__ == "__main__":
    indexer = 0
    for perm in all_perms(separate_values(arr := input("Enter the string: "))):
        print("".join(perm))
        indexer += 1
    print(f"there are {indexer} amounts of permutations possible of {arr}")
```

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
