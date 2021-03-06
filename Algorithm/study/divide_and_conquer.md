# 분할정복법 (divide and conquer)
* 분할정복법이란, **큰 문제를 작은 문제로 나누고, 작은 문제의 해를 모아서 큰 문제의 해를 만드는 알고리즘**이다.
* 전체 형태가 작은 문제에서도 동일한 형태로 존재하므로 **재귀**를 활용한다.

## 방법론 (top-down)
1. 분할 : 해결하기 쉽도록 문제를 여러 개의 작은 부분으로 나눈다.
2. 정복 : 나눈 작은 문제를 각각 해결한다.
3. 통합 : (필요 시) 해결된 답을 모은다.

## 대표 알고리즘
* [이분검색 (Binary Search)](https://github.com/2017100898/TIL/blob/main/Algorithm/study/binary_search.md)
* [합병정렬 (Merge Sort)](https://github.com/2017100898/TIL/blob/main/Algorithm/study/implement/merge_sort.ipynb)
* [빠른정렬 (Quick Sort)](https://github.com/2017100898/TIL/blob/main/Algorithm/study/implement/quick_sort.ipynb)
* [쉬트라쎈 행렬곱셈 (Strassen Algorithm)](https://github.com/2017100898/TIL/blob/main/Algorithm/study/implement/strassen_algorithm.ipynb)
* 큰 수의 곱셈 알고리즘 (Big Integer)

## 분할정복 사용하지 말아야 하는 경우
1. 크기가 n인 입력이 2개 이상의 조각으로 분할되며, 분할된 부분들의 크기가 거의 n에 가깝게 되는 경우
2. 크기가 n인 입력이 거의 n개의 조각으로 분할되며, 분할된 부분의 크기가 n/c인 경우 (여기서 c는 상수)