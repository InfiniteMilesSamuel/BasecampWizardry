# Basecampy4
Streamline Basecamp 4 integration in Python apps. Authenticate, manage projects, messages, to-dos, and more. Simplify workflows with an intuitive Python interface.
# Basecamp 4 API Python Client Library

![Python Version](https://img.shields.io/badge/Python-3.11-blue.svg)
![PyPI Version](https://img.shields.io/pypi/v/basecamp4-client)
### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

An easy-to-use Python interface to the Basecamp 4 API.

**Note:** Basecamp 4 Client Library will drop support for Python 2 and Python 3.5 in future releases.

## Features

- Simple and intuitive API client.
- Authentication handling, including access and refresh tokens.
- Rate limiting and caching support.

## Installation

You can install the library using pip:

$```bash
pip install basecamp4-client

## Configuration
To configure the library, use the following command:

bash
$bc4 configure
Follow the prompts to obtain access and refresh tokens, which will be saved to ~/.config/basecamp4.conf. This allows you to call Basecamp4() without any parameters. Make sure you've created your Basecamp 4 app integration before proceeding.

Alternatively, you can store credentials in environment variables:

BASECAMP_CLIENT_ID
BASECAMP_CLIENT_SECRET
BASECAMP_REDIRECT_URL
BASECAMP_ACCESS_TOKEN
BASECAMP_REFRESH_TOKEN
This makes it easier for CI/CD deployments. You can initialize with:

python
$from basecamp4 import Basecamp4

bc4 = Basecamp4.from_environment()

## Usage
## Basic Example
python
$from basecamp4 import Basecamp4

bc4 = Basecamp4()

for project in bc4.projects.list():
    print(project.name)

new_project = bc4.projects.create("My New Project",
                                  description="The best project ever made.")
new_project.campfire.post_message("Hello World!")
new_message = new_project.message_board.post_message("Check this out",
                                                     content="This is a new message thread start.")
new_message.archive()

todolist = new_project.todoset.create("Things to be done")
todolist.create("Get Milk")
todolist.create("Get Eggs")
go_to_bed = todolist.create("Go to bed.")
go_to_bed.check()  # this is marked as done
Not all API functionality is available yet. For anything missing, you can use the requests Session object directly and consult the Basecamp 4 API docs. The benefit of using this Session object is you will benefit from the authentication, rate-limiting, and caching features.
## Direct Session Example
python
from basecamp4 import Basecamp4
import json

bc4 = Basecamp4()

# Replace these with actual IDs of the Basecamp objects you wish to get
recording_id = 123456789
project_id = 1234567

url = bc4.urls.comments.list_by_recording(project=project_id,
                                          recording=recording_id)
response = url.request(bc4.session)
if not response.ok:
    print("Something went wrong. %s: %s" % (
    response.status_code, response.text))
    exit(1)

data = response.json()
pretty_print = json.dumps(data, indent=4)
print(pretty_print)
## Command Line Interface (CLI) - Coming Soon!
A command-line interface for performing Basecamp 4 operations will be available in future releases.

bash
Copy code
$ bc4 copy-access 12341234 87658765  # Give user 87658765 access to all the projects that 12341234 does
## Todo
Implement the rest of the Basecamp 4 API.
Expand the command-line tool beyond the "configure" command.
Improve testing coverage.

You can replace placeholders like `<yourusername>` with your actual GitHub username and add additional sections or details as needed for your specific Basecamp 4 API client library. Don't forget to include the license file (e.g., `LICENSE`) in your repository if you choose to use the MIT License as shown in the example.
