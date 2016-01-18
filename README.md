# udacity_stage_2
# Udacity stage 2 python code for inctructor help


print "Welcome to a quiz designed to measure your understanding of Python"
print "You will be asked to fill-in-the-blanks in a number of statements."
print 
import time
quiz_difficulty_level = raw_input("Please select a game difficulty by typing it in! Possible choices include easy, medium, and hard.")
if quiz_difficulty_level.lower() == "easy":
    print "Here is your easy quiz. Fill-in-the-Blanks for ___1___, ___2___, and ___3___ in the following sentence."
    print 
    time.sleep(3)
    print 
    print "___1___ refers to the rules that govern what statements are 'legal' in a language. Python has its own ___1___. A ___2___ is a titled container that holds information while a ___3___ is just text."
    print 
    # List of replacement words for text
    blanks_to_replace_easy = ["___1___", "___2___", "___3___"]
    easy_text = "___1___ refers to the rules that govern what statements are 'legal' in a language. Python has its own ___1___. A ___2___ is a titled container that holds information while a ___3___ is just text."
    # Checks if a vocabulary word the user chooses is in the easy text. 
    def vocab_in_text_easy(vocab, blanks_to_replace_easy):
        for text in blanks_to_replace_easy:
            if text in vocab:
                return text
        return None
    def easy_section(easy_text, blanks_to_replace_easy):
        replaced = []
        easy_text = easy_text.split()
        for vocab in easy_text:
            replacement = vocab_in_text_easy(vocab, blanks_to_replace_easy)
            if replacement != None:
                user_input = raw_input("Fill in the blank: " + replacement + " ")
                vocab = vocab.replace(replacement, user_input)
                replaced.append(vocab)
            else:
                replaced.append(vocab)
        replaced = " ".join(replaced)
        print 
        time.sleep(2)
        print "results"
        return replaced
    print easy_section(easy_text, blanks_to_replace_easy)
