//function for kadanes algorithm


def maxSubArray(A,n):
    
    mtn=A[0] //assigning first element of the array
    meh=A[0]
    for i in range(1,len(A)): 
        
        meh=max(meh+A[i],A[i])
        
        if(mtn<meh):
            mtn=meh
            
            
    return mtn
    
    
n=int(input("enter no.of elements : "))
arr=[]
for i in range(0,n):
    x=int(input("enter next element : "))
    arr.append(x)
    
print(maxSubArray(arr,n))
