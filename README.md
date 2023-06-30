# URL-SHORTENER-
import string
import random

# Function to generate a short URL key
def generate_key():
    characters = string.ascii_letters + string.digits
    key = ''.join(random.choices(characters, k=6))
    return key

# Dictionary to store URL mappings
url_mappings = {}

# Function to shorten a URL
def shorten_url(url):
    key = generate_key()
    url_mappings[key] = url
    short_url = "https://example.com/" + key
    return short_url

# Take URL input from the user
original_url = input("Enter the URL: ")

# Shorten the URL
short_url = shorten_url(original_url)

# Print the original and short URLs
print("Original URL:", original_url)
print("Short URL:", short_url)
