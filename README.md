# Fruits-Into-Baskets-II
class Solution:
    def numOfUnplacedFruits(self, fruits: List[int], baskets: List[int]) -> int:
        n=len(fruits)
        c=0
        for i in range(n):
            for j in range(n):
                if baskets[j]>=fruits[i]:
                    c+=1
                    baskets[j]=0
                    break
        return n-c
       
