# masihdatascience
this is a file where i need help and suggetions

#type ctrl+m+b together to get new code cell
import pandas as pd
df=pd.read_csv('/content/drive/MyDrive/Colab Notebooks/empdata.csv')
print(df)
#performing queries on data
df[df.sal>10000]
df[df.sal==df.sal.max()] #this is to retrive whole row info which has maximum salary
df[['empid','ename','sal']][df.sal>10000]  #print all of them having sal gret than 10000
df.index  #we can create any part of data frame as index for example see the next
df1=df.set_index('empid')
print()
#print(df1) #in order to see we need to print it
df.set_index('empid',inplace=True) #in order to make changes in original df to be indexed at empid
print()
#print(df)
print()
#df.loc[1002] #this is to easily get entire details of a particular empid
#df.reset_index(inplace=True) #to easily reset the index at initial place as it was or suppose to be
#print(df)
#sorting the data using parse_dates['doj']
df=pd.read_csv('/content/drive/MyDrive/Colab Notebooks/empdata.csv',parse_dates=['doj'])
print(df)
#df1=df.sort_values('doj') #sorting data based on doj
#df1
#df1=df.sort_values('doj',ascending=False)  #to print data in descending order
#df1
df1=df.sort_values(by=['doj','sal'], ascending=[False, True])
df1 #the above one to get sorted list if same two employee has same doj then sort by salary in ascending order

#NOW DATA VISUALIZATION
import matplotlib.pyplot as plt  #for drawing the graph
import pandas as pd    #for creating data frame
df=pd.read_csv('/content/drive/MyDrive/Colab Notebooks/emp.csv')
print(df)
x=df['empid']
y=df['sal']
plt.bar(x,y, label='Employee data',color='red')
plt.xlabel('Employee ids')
plt.ylabel('Employee salaries')
plt.title('MASIH INC')
plt.legend()
plt.show()

#output as qr code
![qr code for masih data science](https://user-images.githubusercontent.com/65607767/112433164-df27af80-8d67-11eb-859a-4a7a5d326b05.png)

#bar graph with ids, salaries
import matplotlib.pyplot as plt
import pandas as pd
#take employee data as dictionary
#empdata={"empid":[1001,1002,1003,1004,1005,1006],"ename":["anu","masih","elon musk"."mark jukerburg","jeff bejos","bill gates"],"sal":[1000.00,2000.00,3000.00,4000.00,5000.00,6000.00],
#"doj":["10-10-2000","3-6-2002","3-3-2002","9-10-2000","10-8-2000","9-9-1999"]}
df=pd.read_csv('/content/sample_data/mnist_test.csv')
#create a data frame
print(df)
#df=pd.DataFrame(empdata)
#extract empid and salary data into x and y vars
#x=df['empid']
#y=df['sal']
#create bar graph
#plt.bar(x,y, label='Employee data',color='red')
#set x and y axis labels
plt.xlabel('Employee ids')
plt.ylabel('Employee salaries')
#set company title
plt.title('MASIH PVT LTD')
#show legend
plt.legend()
#display the graph
plt.show()      





















