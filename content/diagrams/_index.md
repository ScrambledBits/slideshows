---
title: "Diagrams as code"
date: 2023-02-14T15:24:14-06:00
draft: false
outputs: ["Reveal"]
layout: "list"
---


<!-- 
## Testing

Testing this thing I guess...

---
{{< slide transition="zoom" transition-speed="slow" >}}
## New features

New features here and there
- {{% fragment %}}Feature 1{{% /fragment %}}
- {{% fragment %}}Feature 2{{% /fragment %}}
- {{% fragment %}}Feature 3{{% /fragment %}}

---
{{< slide background-video="/video/coffee.mp4" background-video-loop="true" >}}

#Here, some coffe

### You deserve it
---
{{% section %}}
## Slide 1
---
## Slide 2
Some code...

{{< highlight python >}}
import os
from os.path import abspath

@requires_authorization(roles=["ADMIN"])
def somefunc(param1='', param2=0):
    r'''A docstring'''
    if param1 > param2: ## interesting
        print 'Gre\'ater'
    return (param2 - param1 + 1 + 0b10l) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
{{< /highlight >}}

---
## Slide 3

```python{1-2|4|5-9|11,12|14,15}
import os
from os.path import abspath

@requires_authorization(roles=["ADMIN"])
def somefunc(param1='', param2=0):
    r'''A docstring'''
    if param1 > param2: ## interesting
        print 'Gre\'ater'
    return (param2 - param1 + 1 + 0b10l) or None

class SomeClass:
    pass

>>> message = '''interpreter
... prompt'''
```

{{% /section %}}

---

## Out of the section -->
