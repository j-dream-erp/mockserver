import random
import string

# Function to generate a random user
def generate_user(user_id):
    names = ['Alice', 'Bob', 'Charlie', 'David', 'Eve']
    email_domains = ['example.com', 'test.com', 'demo.com']
    name = random.choice(names)
    email = f'{name.lower()}{user_id}@{random.choice(email_domains)}'
    age = random.randint(18, 65)
    return {'id': user_id, 'name': name, 'email': email, 'age': age}

# Generate mock data for 5 test users
mock_users = [generate_user(i) for i in range(1, 6)]

# Display the generated mock users
for user in mock_users:
    print(user)