# 🌍 Basecamp 4 Client

A magical library to communicate with the ancient and mysterious Basecamp 4 APIs.

## 🌟 Features
Automatic potion brewing (token management).
Enchanted map integration (session handling).
Scroll of forecasting (rate limit management).

## 🛠 Installation
pip install -r requirements.txt

## 📖 Usage
### 🌍 Entering the Basecamp 4 Realm:
from basecamp4 import Basecamp4
camp = Basecamp4(token="your_ancient_token")

### Setting up a Potion (Token Management):
camp.brew_token("your_ingredients")

### 🦉 Summoning Your Projects:
To call forth all the projects you've imbued with your magic:
mystic_projects = camp.invoke_projects()
for project in mystic_projects:
    print(project.title)
    
### 🌱 Planting a Thought (Creating a Todo):
Whenever a new quest or task emerges, inscribe it into the fabric of Basecamp:
quest = camp.engrave_todo(project_id=12345, 
                          title="Defeat the dragon",
                          description="Venture to the east and face the fearsome beast!")
### 🌖 Gazing into the Future (Fetching Upcoming Events):
Peek into the threads of time to foresee upcoming events:
events = camp.see_future()
for event in events:
    print(event.details)

## 🌌 Advanced Usage
For wizards wishing to channel raw, unbridled magic. 

### 🌪 Conjuring the Elements (Complex Filtering):
Invoke the wind and water to filter through your projects, finding only those that resonate with specific energies:
filtered_projects = camp.invoke_projects(status='active', 
                                         creator_id=67890,
                                         last_updated_after='2023-01-01')
for project in filtered_projects:
    print(project.title)

### 🕊 Sending Messenger Birds (Notifications):
Send out your magical messenger birds to notify your guild members of important updates:
camp.send_bird_message(project_id=12345,
                       message="The stars have aligned! Our quest begins tomorrow at dawn.

### 🌀 Direct Communication with Basecamp Spirits:
For those moments when you must converse directly with the ethereal beings of Basecamp without the aid of predefined spells:
response = camp.direct_commune(method='GET', endpoint='/projects/12345/todolists.json')
print(response.json())

### ⏳ Manipulating the Sands of Time (Updating Deadlines):
With your newfound power, you can also change the very sands of time! Update deadlines for tasks:
camp.shift_time(project_id=12345, 
                todo_id=98765, 
                new_deadline='2023-12-31')

### 🔐 Unearthing Hidden Secrets:
Venture deep into the annals of Basecamp to fetch hidden documents:
secret_docs = camp.unearth_secrets(project_id=12345, 
                                   search_terms=['map', 'treasure'])
for doc in secret_docs:
    print(doc.title)
   
Always remember, great mage, with great power comes great responsibility. These advanced incantations provide you immense might, but they should be wielded with care. Tread cautiously on this path, and may the forces of code ever be in your favor. 🌌🔥🪄

## 🛡 Testing
To ensure our protective barriers are always up.
pytest

## 🌠 Contributing to Basecamp 4 Client's Enchanted Grimoire
Seeking fellow mages to make this spellbook even more powerful! Adventurers from all realms are welcomed to enhance this sacred tome. However, as with all magical quests, there are rules and guidelines:
### 1. 🌌 Embarking on the Journey
Before you embark, ensure you are familiar with the current spells and incantations. Clone the repository and set up a local environment.
git clone []
cd Basecamp-4-Client
pip install -r requirements.txt
