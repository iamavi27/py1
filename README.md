# Username and Password
dict = {'swastik': 1, 'abhishek': 2, 'arin': 3}

# Details
name = {    'swastik': 'Swastik Sharma',
            'abhishek': 'Abhishek Raj',
            'arin': 'Arin Choudhary'}

age = {     'swastik': '18',
            'abhishek': '18',
            'arin': '19'}

dob = {     'swastik': '01/01/2003',
            'abhishek': '02/02/2003',
            'arin': '03/03/2002'}

status = {  'swastik': 'Single',
            'abhishek': 'Commited',
            'arin': 'Commited'}

key = {     'swastik': 2001,
            'abhishek': 2002,
            'arin': 2003}

print('Welcome')

usname = input("Enter your username: ")

if usname in dict:
    print('Welcome ' + usname)
    password = int(input('Enter your password: '))
    if (dict[usname] == password):
        print('Login successful')
        print(name.get(usname))
        print(age.get(usname))
        print(dob.get(usname))
        print(status.get(usname))
# Edit details
        change = int(input('If you want to change any details press 1 : '))
        if (change == 1) : 
            i = input('Enter what you want to change : ')
            if(i == "name" ):
                new_name = input('Enter new name : ')
                name[usname] = new_name
                print('Name is changed to ' + name.get(usname))
                 # print(name)
            if(i == "age"):
                new_age = input('Enter new age : ')
                age[usname] = new_age
                print('Age is changed to ' + age.get(usname))
                # print(age)
            if(i == "dob"):
                new_dob = input('Enter new DOB : ')
                dob[usname] = new_dob
                print('DOB is changed to ' + dob.get(usname))
                # print(dob)
            if(i == "status"):
                new_status = input('Enter new status : ')
                status[usname] = new_status
                print('Status is changed to ' + status.get(usname))
                # print(status)
            if(i == "key"):
                new_key = input('Enter new key : ')
                key[usname] = new_key
                print('Key is changed to ' + key.get(usname))
                # print(key)

    if (dict[usname] != password):
        print('Invalid password')
 
 #Authentication for password change   
        verify = int(input('If you want to change your password enter your security key else retry : '))
        if (key[usname] != verify):
            print('Invalid Security Key')
        if (key[usname] == verify):
                dict[usname] = input('Enter new password: ')
                print('Your new password is ' + dict.get(usname))
                PRESS = input('If you want to login with your new password PRESS ENTER')
                if (PRESS == 1):
                    usname = input("Enter your username: ")
                if usname in dict:
                    print('Welcome ' + usname)
                    password = (input('Enter your password: '))
                    if (dict[usname] == password):
                        print('Login successful')
                        print(name.get(usname))
                        print(age.get(usname))
                        print(dob.get(usname))
                        print(status.get(usname))
                    if (dict[usname] != password):
                        print('Invalid password')
                    
                    change = int(input('If you want to change any details press 1 : '))
                    if (change == 1) : 
                        i = input('Enter what you want to change : ')
                        if(i == "name" ):
                            new_name = input('Enter new name : ')
                            name[usname] = new_name
                            print('Name is changed to ' + name.get(usname))
                             # print(name)
                        if(i == "age"):
                            new_age = input('Enter new age : ')
                            age[usname] = new_age
                            print('Age is changed to ' + age.get(usname))
                            # print(age)
                        if(i == "dob"):
                            new_dob = input('Enter new DOB : ')
                            dob[usname] = new_dob
                            print('DOB is changed to ' + dob.get(usname))
                            # print(dob)
                        if(i == "status"):
                            new_status = input('Enter new status : ')
                            status[usname] = new_status
                            print('Status is changed to ' + status.get(usname))
                            # print(status)
                        if(i == "key"):
                            new_key = input('Enter new key : ')
                            key[usname] = new_key
                            print('Key is changed to ' + key.get(usname))
                            # print(key)
else:
    print('Invalid username')
