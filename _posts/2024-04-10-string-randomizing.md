---
layout: post
title: string randomizing
categories: testing
tags: [testing,python]
---

# Conceal your super secret stuff

(don't do this with super super secret stuff like passwords, use real encryption for that)

The seed method from the built-in random can be used to randomize strings. In this case, a timestamp will create a different randomizer for the secret thing "tramp". I use this to make unique identifiers in databases where some values can share alike names.

~~~python
import random, string
from datetime import datetime

random.seed(datetime.now().timestamp())

supersecretthing = "tramp"
supersecretrandomized = supersecretthing + "".join(random.choices(string.ascii_letters + string.digits, k=16))
print(supersecretrandomized)
~~~

ok thaats it
