import random

# Define the list of responses
responses = [
    "It is certain",
    "Without a doubt",
    "You may rely on it",
    "Yes definitely",
    "It is decidedly so",
    "Reply hazy try again",
    "Better not tell you now",
    "Ask again later",
    "Cannot predict now",
    "Concentrate and ask again",
    "Don't count on it",
    "Outlook not so good",
    "My sources say no",
    "Very doubtful",
    "Signs point to yes",
    "Yes",
    "Most likely",
    "Outlook good",
    "My reply is no",
    "Not a chance"
]

# Shuffle the list of responses
random.shuffle(responses)

# Define the number of affirmative, non-committal, and negative responses
num_affirmative = 10
num_noncommittal = 5
num_negative = 5

# Create a list of responses with the specified number of each type
affirmative_responses = responses[:num_affirmative]
noncommittal_responses = responses[num_affirmative:num_affirmative+num_noncommittal]
negative_responses = responses[num_affirmative+num_noncommittal:]

# Prompt the user to ask a question
question = input("What is your question? ")

# Determine which type of response to use
response_type = random.randint(1, 3)

# Give a random response of the appropriate type
if response_type == 1:
    response = random.choice(affirmative_responses)
elif response_type == 2:
    response = random.choice(noncommittal_responses)
else:
    response = random.choice(negative_responses)

# Output the response
print(response)
