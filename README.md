# File-Handling-and-Exception-Handling-Assignment
def read_user_file():
    filename = input("Please enter the filename: ")
    try:
        with open(filename, 'r') as file:
            content = file.read()
            print("File content:")
            print(content)
    except FileNotFoundError:
        print(f"Error: The file '{filename}' does not exist.")
    except IOError:
        print(f"Error: The file '{filename}' cannot be read.")

# Example usage
read_user_file()
