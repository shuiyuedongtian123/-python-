import numpy as np
input=[[0,0],[0,1], [1,0], [1,1]]
input=map(lambda x:x+[1],input)#加偏置
output=[-1,-1,-1,1]
w=np.array([0,0,0])
T=10000
k=0
for  t in range(T):
    for i in range(len(input)):
        l=sum(w* output[i]* np.array(input[i]))  #[output[i] * x for x in input[i]]
        if l<=0 :
            w+=output[i]* np.array(input[i])
            k+=1
w  # -python-
