#AgeCalculator

while(True):
    print("BIRTH DAY DETAILS")
    print()
    num1=int(input("Enter your year of birth         : "))
    str1=input("Enter the month of your birth    : ")
    num2=int(input("Enter the date that you were born: "))
    print()
    print()
    
    
    days=[31,28,31,30,31,30,31,31,30,31,30,31,0]
    
    if(str1=='january' or str1=='1' or str1=='January'):
        month=1
        
    elif(str1=='february' or str1=='2' or str1=='February'):
        month=2
        
    elif(str1=='march' or str1=='3' or str1=='March'):
        month=3
        
    elif(str1=='april' or str1=='4' or str1=='April'):
        month=4
        
    elif(str1=='may' or str1=='5' or str1=='May'):
        month=5
        
    elif(str1=='june' or str1=='6' or str1=='June'):
        month=6
        
    elif(str1=='july' or str1=='7' or str1=='July'):
        month=7
        
    elif(str1=='august' or str1=='8' or str1=='August'):
        month=8
        
    elif(str1=='september' or str1=='9' or str1=='September'):
        month=9
        
    elif(str1=='october' or str1=='10' or str1=='October'):
        month=10
        
    elif(str1=='november' or str1=='11' or str1=='November'):
        month=11
        
    elif(str1=='december' or str1=='12' or str1=='December'):
        month=12
        
    else:
        print("Invalid month/check the spelling")

        
    print("CURRENT DAY DETAILS")
    print()
    num3=int(input("Enter year : "))
    str2=input("Enter month: ")
    num4=int(input("Enter date : "))

        
    if(str2=='january' or str2=='1' or str2=='January'  ):
        month1=1
        
    elif(str2=='february' or str2=='2' or str2=='February'):
        month1=2
        
    elif(str2=='march' or str2=='3' or str2=='March'):
        month1=3
        
    elif(str2=='april' or str2=='4' or str2=='April'):
        month1=4
        
    elif(str2=='may' or str2=='5' or str2=='May'):
        month1=5
        
    elif(str2=='june' or str2=='6' or str2=='June'):
        month1=6
        
    elif(str2=='july' or str2=='7' or str2=='July'):
        month1=7
        
    elif(str2=='august' or str2=='8' or str2=='August'):
        month1=8
        
    elif(str2=='september' or str2=='9' or str2=='September'):
        month1=9
        
    elif(str2=='october' or str2=='10' or str2=='October'):
        month1=10
        
    elif(str2=='november' or str2=='11' or str2=='November'):
        month1=11
        
    elif(str2=='december' or str2=='12' or str2=='December'):
        month1=12
    else:
        print("Invalid month/check the spelling")
        
    leap=0
    for i in range(num1,2024+1):
        if(i%4==0 and i%100!=0) or(i%400==0):
            leap+=1
            
    day=0  
    for i in range(month,13):
        day+=days[i]
        
    day+=days[month-1]-num2
    
    for i in range(0,month1-1):
        day+=days[i]
    day+=num4
        
    
    year=num3-num1
    day1=0
    print()
    print()
    if(day>=num4):
        if (month>=month1):
            year-=1
            print("You are ",year,"years old now")
            day1=year*365
        
    else:
        print("You are ",year,"years old now!")
        year-=1  
        day1=year*365
        
    
    day=day+leap+day1
    print("Congratulations, you’ve had ",day," days of adventure so far!")

        
    ch=input("Do you want to continue(y/n)")   
    if ch=='n':
        exit()
