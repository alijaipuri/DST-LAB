def isBalanced(s):
    stack = []
    bracket_map = {')': '(', '}': '{', ']': '['}
    for char in s:
        if char in bracket_map:
            top_element = stack.pop() if stack else '#'
            if bracket_map[char] != top_element:
                return "NO"
        else:
            stack.append(char)
    return "YES" if not stack else "NO"

if __name__ == "__main__":
    t = int(input())
    for _ in range(t):
        s = input()
        print(isBalanced(s))
