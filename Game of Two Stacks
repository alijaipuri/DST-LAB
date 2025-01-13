import math
import os
import random
import re
import sys

def twoStacks(x, a, b):
    current_sum = 0
    count = 0
    i = 0
    while i < len(a) and current_sum + a[i] <= x:
        current_sum += a[i]
        i += 1
    max_count = i
    j = 0
    while j < len(b) and i >= 0:
        current_sum += b[j]
        j += 1
        while current_sum > x and i > 0:
            i -= 1
            current_sum -= a[i]
        if current_sum <= x:
            max_count = max(max_count, i + j)
    return max_count

if __name__ == "__main__":
    g = int(input())  
    for _ in range(g):
        n, m, x = map(int, input().split()) 
        a = list(map(int, input().split()))  
        b = list(map(int, input().split()))  
        print(twoStacks(x, a, b))
