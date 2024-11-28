- 👋 Hi, I’m @MayuriRaimal
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
MayuriRaimal/MayuriRaimal is a ✨ special ✨ repository because its `README.md` (this file) appears on you
import time
import random

def slow_print(text, delay=0.05):
    """Prints text slowly for dramatic effect."""
    for char in text:
        print(char, end='', flush=True)
        time.sleep(delay)
    print()

def introduction():
    slow_print("You are Emily Carter, a paranormal investigator.")
    slow_print("You’ve been called to investigate a haunted house where the Perrin family has experienced terrifying events.")
    slow_print("Armed with your flashlight, tape recorder, and an ancient book of rituals, you step into the house...")
    input("\nPress Enter to continue...\n")

def haunted_room():
    slow_print("You enter a dark room. The air feels heavy.")
    slow_print("You hear whispers. Suddenly, the door slams shut behind you.")
    slow_print("Do you:")
    slow_print("1. Use your flashlight to investigate.")
    slow_print("2. Open the ritual book.")
    slow_print("3. Run to the door and try to escape.")
    choice = input("\nChoose 1, 2, or 3: ")
    
    if choice == "1":
        flashlight_event()
    elif choice == "2":
        ritual_book_event()
    elif choice == "3":
        door_event()
    else:
        slow_print("Invalid choice. The entity grows stronger...")
        haunted_room()

def flashlight_event():
    slow_print("You turn on your flashlight and see eerie symbols on the walls.")
    slow_print("The symbols glow, and the whispers grow louder.")
    outcome = random.choice(["good", "bad"])
    if outcome == "good":
        slow_print("You discover a protective sigil and draw it on the floor.")
        slow_print("The whispers fade, and you feel a brief moment of safety.")
        haunted_room()
    else:
        slow_print("The symbols pulse with energy. A shadowy figure lunges at you!")
        game_over()

def ritual_book_event():
    slow_print("You open the ritual book and begin reading a protection spell.")
    slow_print("The room starts to shake. The whispers turn into screams.")
    outcome = random.choice(["success", "failure"])
    if outcome == "success":
        slow_print("The entity is weakened! You gain the courage to explore further.")
        haunted_room()
    else:
        slow_print("The spell backfires! The entity grows stronger.")
        game_over()

def door_event():
    slow_print("You run to the door and try to open it.")
    slow_print("It won’t budge. The whispers turn into maniacal laughter.")
    outcome = random.choice(["escape", "caught"])
    if outcome == "escape":
        slow_print("The door finally opens, and you run to safety.")
        slow_print("But the house is still cursed. Your mission is incomplete.")
        game_over("You survived, but the Perrin family remains in danger.")
    else:
        slow_print("You feel icy hands gripping your shoulders.")
        slow_print("The last thing you hear is your own scream...")
        game_over()

def game_over(message="The entity has claimed you."):
    slow_print(f"\nGAME OVER: {message}")
    play_again = input("Do you want to try again? (yes/no): ").strip().lower()
    if play_again == "yes":
        main()
    else:
        slow_print("Thanks for playing. Stay safe out there!")
        exit()

def main():
    introduction()
    haunted_room()

if __name__ == "__main__":
    main()
    
    
