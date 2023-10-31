# 🌍 Basecamp 4 Client

A magical library to communicate with the ancient and mysterious Basecamp 4 APIs.

Discover more about the wonders of Basecamp 4 by visiting its [official website](https://basecamp.com/) or delving into its comprehensive [API documentation](https://github.com/basecamp/bc3-api).

🚧 Note to Readers: We sincerely apologize for any formatting inconsistencies you might observe in this document. We're aware of the issue and are actively working on a resolution. In the meantime, please bear with us and refer to the raw markdown or other markdown viewers if anything appears amiss. Thank you for your understanding. 🚧

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

### 2. 🚪 Portals and Pathways (Branching)
Open a new portal (branch) for each spell or enhancement you wish to add. Name your portal descriptively:

git checkout -b feature/add-new-spell

### 3. 📜 Scribing in the Grimoire (Coding)
Ensure your incantations (code) are clear and comprehensible. Fellow mages should be able to understand your magic with ease. Follow the code styling guide of PEP 8.

### 4. 🧙 Mage Duels (Testing)
Before presenting your spells, duel against them (run tests) to ensure they don't backfire:

pytest

### 5. 🌐 Conjuring for All Realms (Compatibility)
Ensure your spells are compatible across different Python versions. They should be woven to be usable by mages from all realms.

### 6. 🍃 Elixirs and Incense (Dependencies)
If you introduce new ingredients (libraries or dependencies), ensure they are added to requirements.txt.

### 7. 🕊 Sharing Your Magic (Submitting a Pull Request)
Once you're satisfied with your enhancements, share them with the grand council (submit a pull request). Describe your spells and their purpose clearly in your message.

### 8. 🌿 Patience and Respect
Remember, the elder mages (maintainers) are wise and will review your spells with a keen eye. Respect their feedback and engage in collaborative discourse.

May your contributions resonate with the energy of the universe, enriching this grimoire for eons to come! 🌟📘🪄

## 🌌 Celestial Collaborators & Ethereal Entities
Behind every magical grimoire, there's a council of wizards, witches, and wondrous entities weaving their spells together:

Miles, the Mystical Maven: Conduit of Code & Master of the Mainframe

## 💫 Magic Wands & Wonderful Widgets
Every masterful mage has their collection of arcane artifacts, and our project is imbued with the powers of several mystical modules. These are but a few of the enchanted essentials powering our potion:

Django's Djinn: An omnipotent oracle that dances with databases and brings dazzling dreams to life. URL: https://www.djangoproject.com/

FastAPI's Familiar: A swift sprite that soars in the service of creating stellar APIs. The speed of this spirit is unparalleled! URL: https://fastapi.tiangolo.com/
 
Flask's Phantasm: A lightweight luminary, ever-ready to render radiant web realms at a moment's notice. URL: https://flask.palletsprojects.com/

Numpy's Nexus: A numerical nymph, weaving wonders with arrays and matrices. Mathematics is its playground. URL: https://numpy.org/

Pandas' Parchment: A proficient paper, blessed by the bear of data manipulation and analysis. Perfect for potion preparation protocols. URL: https://pandas.pydata.org/

Pytest's Potion: The elixir expert! Every time we craft a new concoction, it's the first to test its taste and tell if it's terrific or toxic. URL: https://pytest.org/

Celery's Circlet: Asynchronous actions are an art, and with this circlet, tasks travel through time, taken care of in the twinkle of an eye. URL: https://docs.celeryproject.org/en/stable/

Werkzeug's Wisp: A utility spirit, whispering wizardry for WSGI, used wisely within Flask's fold. URL: https://werkzeug.palletsprojects.com/

Pillow's Portal: Our project's pictorial protector, painting and processing pictures with perfection. URL: https://pillow.readthedocs.io/





