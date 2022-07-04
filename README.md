# Microsoft Rewards Bot
[![License](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](LICENSE)
[![Version](https://img.shields.io/badge/version-v0.1-blue.svg?style=flat)](#)

An automated solution for earning daily Microsoft Rewards points using Python and Selenium.

## Installation
* Clone the repo.
* Install requirements with the following command :
 ```
 pip install -r requirements.txt
 ```
* Make sure you have Chrome installed.
* Edit the accounts.json.sample with your accounts credentials and rename it by removing .sample at the end
If you want to add more than one account, the syntax is the following (mobile_user_agent is optional):
```json
{
  "username": "Your Email",
  "password": "Your Password",
  "mobile_user_agent": "Your Preferred Mobile User Agent"
},
{
  "username": "Your Email",
  "password": "Your Password",
  "mobile_user_agent": "Your Preferred Mobile User Agent"
}
```
* Due to limits of Ipapi sometimes it returns error and it causes bot stops. So you can define default language and location to prevent it.
* Run the script.
	* Optional arguments:
		*  `--headless ` You can use this argument to run the script in headless mode.
		*  `--session ` Use this argument to create session for each account.
		*  `-everyday TIME` This argument takes time in 24h format (HH:MM) to run it everyday at the given time by leaving the program open.
	* If you run the script normally it asks you for input instead.

### Using Github Actions
* Fork the repo.
* Go to `Settings`>`Secrets`>`Actions` and add `New repository secret` named `ACCOUNTS` where the value will `Your Email:Your Password`.
* Go to `Actions`>`Deploy` and run the workflow.
 
## Features
* Bing searches (Desktop, Mobile and Edge) with User-Agents.
* Complete automatically the daily set.
* Complete automatically punch cards.
* Complete automatically the others promotions.
* Headless Mode.
* Multi-Account Management (Config and command-line).
* Worflow for automatic deployement.
* Modified to be undetectable as bot.
* If it faces to an unexpected error then try the account from first.
* Save progress of bot in a log file and use it to pass completed account on the next start at the same day.
* Detect suspended accounts.
* Detect locked accounts.
* Detect unusual activites.
* Uses time out to prevent infinite loop
* You can assign custom user-agent for mobile like above example.
* Set clock to start it at specific time.
* For Bing search it uses random word at first try and if api failed then it uses google trends.

## Credits
* [@charlesbel](https://github.com/charlesbel) The original author of the repo.
* [@Farshadz1997](https://github.com/farshadz1997) For adding a bunch of features.
