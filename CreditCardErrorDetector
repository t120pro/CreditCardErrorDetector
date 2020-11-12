# Name of Program: Credit Card Error Detection
# Author: tl120pro
# Description of Program: This program takes in a credit card number, and determines if its number is valid.
import re

print("We take security seriously!")
cont = "yes"
while cont.lower() == "yes":
    cc_num = input("Please enter your 14 digit Credit Card number: ").strip()
    first_sum = 0
    last_sum = 0
    index = 0
    
    #reg ex for credit card number
    cc_reg_ex = re.compile(r'^\d{14}$')
    cc_correct_reg_ex = cc_reg_ex.search(cc_num)
    if cc_correct_reg_ex == None:
        print ("\nThe Credit Card number you entered does no fit the proper format. \nPlease Try Again...\n")
        continue

    for cc_char in cc_num:
        cc_num = int(cc_char)
        #step 1: taking every other digit, multiplying it by 2, and subtracting 9 if it has 2 digits
        if (index%2 == 0 ):
            double_num = cc_num*2
            if (double_num > 9):
                double_num -= 9
            first_sum += double_num
        #step 2: taking every the remaining digits and adding them together
        else:
            last_sum += int(cc_num)
        index += 1

    total_sum = str(last_sum + first_sum)
    if (total_sum[-1] == '0' ):
        print("The Credit Card number entered is valid.")
    else:
        print("The Credit Card number entered is invalid.")
    cont = input("Would you like to enter another Credit Card number? (yes/no)")
