# blog

## exemplos

``` py title="bubble_sort.py"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```


Task List

-   [X] item 1
    *   [X] item A
    *   [ ] item B
        more text
        +   [x] item a
        +   [ ] item b
        +   [x] item c
    *   [X] item C
-   [ ] item 2
-   [ ] item 3

???+ note "Open styled details"

    ???+ danger "Nested details!"
        And more content again.
    ??? warning "Opa"
        adasd
    ???+ note "asdasd"

/// admonition | Some title
    type: success
## assdf
Some content\
sdfsdf
///    