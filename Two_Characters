#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'alternate' function below.
#
# The function is expected to return an INTEGER.
# The function accepts STRING s as parameter.
#

def alternate(s):
    # Write your code here
    set_of_chars = list(set(s))
    n = len(set_of_chars)
    max_length = 0

    for i in range(n):
        for j in range(i + 1, n):
            c1, c2 = set_of_chars[i], set_of_chars[j]

            Acceptable = []
            for char in s:
                if char == c1 or char == c2:
                    Acceptable.append(char)

            is_alternating = True
            for k in range(len(Acceptable) - 1):
                if Acceptable[k] == Acceptable[k + 1]:
                    is_alternating = False
                    break

            if is_alternating:
                max_length = max(max_length, len(Acceptable))

    return max_length

        

if __name__ == '__main__':
    fptr = open(os.environ['OUTPUT_PATH'], 'w')

    l = int(input().strip())

    s = input()

    result = alternate(s)

    fptr.write(str(result) + '\n')

    fptr.close()
