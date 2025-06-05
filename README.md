# CodeAlpha_BasicChatbot
import pyjokes

def chatbot():
    print("Chatbot: Hello! I'm here to chat with you. Type 'bye' to end the conversation.")

    while True:
        user_input = input("You: ").lower()

        if "bye" in user_input or "exit" in user_input:
            print("Chatbot: Goodbye! Have a great day.")
            break
        elif any(word in user_input for word in ["hello", "hi", "hey", "hlo"]):
            print("Chatbot: Hey there! How can I help you today?")
        elif "how are you" in user_input or "how r u" in user_input:
            print("Chatbot: I'm doing great, thank you! How about you?")
        elif "your name" in user_input or "who are you" in user_input:
            print("Chatbot: I'm a smart little chatbot built with Python!")
        elif "help" in user_input:
            print("Chatbot: You can ask me how I am, who I am, or even ask me to tell you a joke!")
        elif "thank" in user_input:
            print("Chatbot: You're welcome! ")
        elif "weather" in user_input:
            print("Chatbot: I can't fetch live weather yet, but I hope it's nice outside!")
        elif "joke" in user_input:
            joke = pyjokes.get_joke()
            print("Chatbot (Joke):", joke)
        else:
            print("Chatbot: Hmm, I'm not sure how to respond to that. Try asking something else!")

# Run the chatbot
chatbot()
