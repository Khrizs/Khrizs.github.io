---
layout: post
title: Python Testing
categories: testing
tags: [testing,python]
---

# Woah spooky python 😱

Check if something is false with typehints omg!!
~~~python
def isFalseType(string:str) -> bool:
    """
    Args:
        string: String of text to check
    Return:
        Bool: If string is falsy
    """
    if type(string) != str:
        raise ValueError("Non string argument given to string arguement")
    
    try:
        if not eval(string):
            return True
        else:
            return False
    except:
        return False
~~~

ok thaats it
