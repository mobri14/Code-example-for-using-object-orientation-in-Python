class Languages:
    # This class collects information about languages spoken by people

    def __init__(self, question):
        """Initialize the survey question and an empty list to store responses"""
        self.question = question  # Store the survey question
        self.responses = []  # Create an empty list to store responses

    def show_question(self):
        """Display the survey question"""
        print(self.question)  # Print the survey question

    def store_response(self, response):
        """Store a single response to the survey"""
        self.responses.append(response)  # Append the response to the responses list

    def show_responses(self):
        """Display all the collected responses"""
        print("Here are the collected responses:")  # Display a message before responses
        for response in self.responses:  # Loop through each response
            print(f"- {response}")  # Print each response

# Test code
def test_languages():
    """Function to test the Languages class functionality"""

    # Create an instance of the Languages class
    language_poll = Languages("Which languages do you speak?")  # Create a class object with a question

    # Display the question
    language_poll.show_question()  # Show the survey question

    # Simulate responses
    language_poll.store_response("1-Persian")  # Store the response "1-Persian"
    language_poll.store_response("2-English")  # Store the response "2-English"
    language_poll.store_response("3-French")  # Store the response "3-French"

    # Display collected responses
    language_poll.show_responses()  # Display all collected responses

    # Ask user to select a language by number
    try:
        x = int(input("Please choose a number (1, 2, or 3): "))  # Prompt the user to select a number
    except ValueError:
        print("Invalid input, please enter a number.")  # Display error if input is not a number
        return  # Exit function if input is invalid

    # Display message based on user choice
    if x == 1:
        print("Persian is a beautiful language")  # If user selects 1, display message about Persian
    elif x == 2:
        print("English is a beautiful language")  # If user selects 2, display message about English
    elif x == 3:
        print("French is a beautiful language")  # If user selects 3, display message about French
    else:
        print("Invalid choice, please select 1, 2, or 3.")  # If the input is not valid, display error message

# Call the test function
test_languages()  # Run the test function to test the Languages class functionality
