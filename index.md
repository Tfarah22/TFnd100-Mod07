## Module 07 Pickling and Structured error handling

YI will demonstrate how to work with pickling and structured error handling. Pickling is the process of serializing and deserializing data entered. Structured error handling is a set of predefined exceptions or errors.

```markdown
Here 
is the code that entered to complete assignment 

import pickle  # This imports code from another code file!

# Data -------------------------------------------- #
strFileName = 'AppData.dat'
lstCustomer = []


# Processing -------------------------------------- #
def save_data_to_file(file_name, list_of_data):
    file = open(file_name, "ab")
    pickle.dump(list_of_data, file)
    file.close()


def read_data_from_file(file_name):
    file = open(file_name, "rb")
    list_of_data = pickle.load(file)
    file.close()
    return list_of_data


# Presentation ------------------------------------ #
try:
    id = int(input("Enter the ID: "))
    if type(id) == str:
        raise Exception

    str_name = (input('Enter Name: '))
    if str_name.isnumeric():
        raise Exception('Do not use numbers for Name')

    lstCustomer = [id, str_name]
    save_data_to_file(strFileName, lstCustomer)

except Exception as e:
    print("Error! Tip *Enter number")
    print("Error! Tip *Enter letters")

input('Press enter to finish')



<img width="1030" alt="image" src="https://user-images.githubusercontent.com/105770102/171337777-2def43a8-d9fa-48e3-8317-ee8e575d7b04.png">


I applied my knowledge and was able to confirm that the script worked 


<img width="928" alt="image" src="https://user-images.githubusercontent.com/105770102/171337644-df1de3fb-e6e8-42df-a097-e00948c92076.png">
I was able to confirm that the error codes were working 
