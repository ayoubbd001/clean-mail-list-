import re

def remove_duplicates(email_list):
    unique_emails = []
    for email in email_list:
        if email.strip() not in unique_emails:
            unique_emails.append(email.strip())
    return unique_emails

def is_valid_email(email):
    pattern = r'^[\w\.-]+@[\w\.-]+\.\w+$'
    return re.match(pattern, email) is not None

def clean_email_list(email_list):
    cleaned_emails = []
    for email in email_list:
        email = email.strip()
        if email and is_valid_email(email):
            cleaned_emails.append(email)
    return cleaned_emails


# _____________---___  TEST  ___-----______________

file_path = 'lt_27439.txt'  # Path to the file containing the email list
email_list = []


with open(file_path, 'r') as file:
    for line in file:
        email_list.append(line.strip())

# Remove duplicates
unique_emails = remove_duplicates(email_list)

# Clean email list
cleaned_emails = clean_email_list(unique_emails)

file_path_clean_list = 'cleanList.txt' # put yr new file to save the clean list
with open(file_path_clean_list, 'a') as filee:
    
    for email in cleaned_emails:
        filee.write(email + '\n')
    print('done')
