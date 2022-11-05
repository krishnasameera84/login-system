from getpass import getpass

def Register():
    while True:
        username = input('> Enter username: ')
        password = getpass('> Create password: ')
        confirm_password = getpass('> Confirm password: ')
        if password == confirm_password:
            password_file = open('pass.txt', 'a')
            password_file.write(f'Username: {username} --> Password: {confirm_password}' "\n")
            password_file.close()
            print('> Account created!')
            break
        elif password != confirm_password:
            print('> Error, passwords do not match')
            continue

def Login():
    while True:
        username = input('> Enter username: ')
        password = getpass('> Enter password: ')

        password_file = open('pass.txt', 'r').read()
        if username and password in password_file:
            print('> Welcome!')
            break
        else:
            print('> Invalid username or password. Try again!')
            continue
        password_file.close()

print('> Enter reg to register')
print('> Enter login to login')

while True:

    reg_or_login = input('> Do you want to register or login: ')

if reg_or_login == 'reg':
    Register()

elif reg_or_login == 'login':
    Login()

else:
    print('Error, wrong input!')
