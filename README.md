# n-least-common-multiples
# python
# Find the least common multiple of numbers in a list 리스트안에 있는 수들의 최소공배수를 구하기
def solution(arr):
    answer=0
    n=1
    while(True):
        answer=max(arr)*n
        result=True #True면 최소공배수 아니면 최소공배수 아님
        for i in arr:
            if answer%i!=0:
                result=False
                break
        if result:  #True면 While문을 빠져나옴
            break
        n+=1
    return answer
arr=[2,6,8,14]
a=solution(arr)
print(a)
# result--> 168
