Assignment #1: Anagram Checker
Background: Anagram Checker is a program that takes two words and determines if an anagram can be made from it. If so, the program will return true, otherwise false.

Submission Information
🚨 Please review our Assignment Submission Guide 🚨 for detailed instructions on how to format, branch, and submit your work. Following these guidelines is crucial for your submissions to be evaluated correctly.

Submission Parameters:
Submission Due Date: 11:59 PM - 05/05/2024
The branch name for your repo should be: assignment-1
What to submit for this assignment:
This Jupyter Notebook (assignment_1.ipynb) should be populated and should be the only change in your pull request.
What the pull request link should look like for this assignment: https://github.com/<your_github_username>/python/pull/<pr_id>
Open a private window in your browser. Copy and paste the link to your pull request into the address bar. Make sure you can see your pull request properly. This helps the technical facilitator and learning support staff review your submission easily.
Checklist:

Created a branch with the correct naming convention.
Ensured that the repository is public.
Reviewed the PR description guidelines and adhered to them.
Verify that the link is accessible in a private browser window.
If you encounter any difficulties or have questions, please don't hesitate to reach out to our team via our Slack at #cohort-3-help. Our Technical Facilitators and Learning Support staff are here to help you navigate any challenges.

Part 1: Building the base Anagram Checker
Given two valid strings, check to see if they are anagrams of each other. If it is, return True, else False. For this part, we can assume that uppercase letters are the same as if it was a lowercase character.

Examples of anagrams:

Slient and Listen
Night and Think
Example outputs:

anagram_checker("Slient", "listen") # True
anagram_checker("Slient", "Night") # False
anagram_checker("night", "Thing") # True
# This is a function, which we will learn more about next week. For testing purposes, we will write our code in the function
def anagram_checker(word_a, word_b):
  # Your code here


  def anagram_checker(word_a, word_b):


        letters_a = sorted({letter.lower() for letter in word_a})
        letters_b = sorted({letter.lower() for letter in word_b})
        return letters_a == letters_b


# Run your code to check using the words below:
anagram_checker("Slient", "listen")
anagram_checker("Slient", "Night")
anagram_checker("night", "Thing")
Part 2: Expanding the functionality of the Anagram Checker
Using your existing and functional anagram checker, let's add a boolean option called is_case_sensitive, which will return True or False based on if the two compared words are anagrams and if we are checking for case sensitivity.

def anagram_checker(word_a, word_b, is_case_sensitive):
  # Modify your existing code here


def anagram_checker(word_a, word_b, is_case_sensitive):

    if is_case_sensitive == True:
        letters_a = sorted({letter for letter in word_a})
        letters_b = sorted({letter for letter in word_b})
        return letters_a == letters_b
    else:
        letters_a = sorted({letter.lower() for letter in word_a})
        letters_b = sorted({letter.lower() for letter in word_b})
        return letters_a == letters_b


# Run your code to check using the words below:
anagram_checker("Slient", "listen", False) # True
anagram_checker("Slient", "Listen", True) # False
Criteria	Pass	Fail
Code Execution	All code cells execute without errors.	Any code cell produces an error upon execution..