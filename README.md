# Code-example-for-using-object-orientation-in-Python
Code example for using object orientation in Python
It is posted here in both Persian and English

class Languages:
    # This class collects information about languages spoken by people
    # این کلاس اطلاعات مربوط به زبان‌های صحبت شده توسط افراد را جمع‌آوری می‌کند

    def __init__(self, question):
        """Initialize the question and an empty list to store responses"""
        """مقداردهی اولیه به سوال نظرسنجی و ایجاد یک لیست خالی برای ذخیره پاسخ‌ها"""
        self.question = question  # Store the survey question / سوال نظرسنجی را ذخیره می‌کند
        self.responses = []  # Create an empty list to store responses / لیستی خالی برای ذخیره پاسخ‌ها

    def show_question(self):
        """Display the survey question"""
        """نمایش سوال نظرسنجی"""
        print(self.question)  # Print the survey question / سوال نظرسنجی را چاپ می‌کند

    def store_response(self, response):
        """Store a single response to the survey"""
        """ذخیره یک پاسخ به نظرسنجی"""
        self.responses.append(response)  # Append the response to the responses list / پاسخ کاربر را به لیست پاسخ‌ها اضافه می‌کند

    def show_responses(self):
        """Display all the collected responses"""
        """نمایش همه پاسخ‌های جمع‌آوری‌شده"""
        print("Here are the collected responses:")  # Display a message before responses / پیام نمایش پاسخ‌ها را چاپ می‌کند
        for response in self.responses:  # Loop through each response / برای هر پاسخ در لیست
            print(f"- {response}")  # Print each response / هر پاسخ را چاپ می‌کند

# Test code / کد تست
def test_languages():
    """Function to test the Languages class functionality"""
    """تابعی برای تست عملکرد کلاس Languages"""

    # Create an instance of the Languages class
    # ایجاد یک نمونه از کلاس Languages
    language_poll = Languages("Which languages do you speak?")  # Create a class object with a question / نمونه‌ای از کلاس با سوال

    # Display the question / نمایش سوال
    language_poll.show_question()  # Show the survey question / سوال نظرسنجی را نمایش می‌دهد

    # Simulate responses / شبیه‌سازی پاسخ‌ها
    language_poll.store_response("1-Persian")  # Store the response "1-Persian" / پاسخ "1-فارسی" را ذخیره می‌کند
    language_poll.store_response("2-English")  # Store the response "2-English" / پاسخ "2-انگلیسی" را ذخیره می‌کند
    language_poll.store_response("3-French")  # Store the response "3-French" / پاسخ "3-فرانسوی" را ذخیره می‌کند

    # Display collected responses / نمایش پاسخ‌های جمع‌آوری‌شده
    language_poll.show_responses()  # Display all collected responses / تمامی پاسخ‌ها را نمایش می‌دهد

    # Ask user to select a language by number / درخواست از کاربر برای انتخاب زبان
    try:
        x = int(input("Please choose a number (1, 2, or 3): "))  # Prompt the user to select a number / از کاربر درخواست انتخاب عدد
    except ValueError:
        print("Invalid input, please enter a number.")  # Display error if input is not a number / در صورت ورودی غیر عددی، پیام خطا نمایش داده می‌شود
        return  # Exit function if input is invalid / در صورت خطا، از تابع خارج می‌شود

    # Display message based on user choice / نمایش پیام بر اساس انتخاب کاربر
    if x == 1:
        print("Persian is a beautiful language")  # If user selects 1, display message about Persian / در صورت انتخاب ۱، پیام فارسی نمایش داده می‌شود
    elif x == 2:
        print("English is a beautiful language")  # If user selects 2, display message about English / در صورت انتخاب ۲، پیام انگلیسی نمایش داده می‌شود
    elif x == 3:
        print("French is a beautiful language")  # If user selects 3, display message about French / در صورت انتخاب ۳، پیام فرانسوی نمایش داده می‌شود
    else:
        print("Invalid choice, please select 1, 2, or 3.")  # If the input is not valid, display error message / در صورت ورودی نامعتبر، پیام خطا نمایش داده می‌شود

# Call the test function / فراخوانی تابع تست
test_languages()  # Run the test function / اجرای تابع برای تست کلاس
