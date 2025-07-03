#python code for Binary Search 
Ar=[1,2,5,8,9,10,11,15,16,19] #can change to your will 
print (Ar)
def BS(find):
    L=0
    H=len(Ar)-1
    found= False
    not_found= False
    while found==False and not_found==False:
        #calculate midpoint 
        M=(L+H)//2
        #check if item is found
        if Ar[M]==find:
            found=True
        elif L>=H:
            not_found=True
        elif Ar[M]<find:
            L=M+1
        else:
            H=M-1
    if found==True:
        x=("Item Found")
    else:
        x=("Item Not Found")
    return x

#main
n=int(input("Enter number to search "))
Result=BS(n)
print(Result)
