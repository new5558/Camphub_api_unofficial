# Usage

get an information about the camp and compettion currently available

aims to be used mainly on thailand event and compettion centered aroud tech and computer

I don't have intention to make it a scraper for commercial purpose I just want to share the information I found in discord faster

<strong>user of this project should only use it for personal use and not for commercial purpose</strong>

## Supported Site

- https://www.camphub.in.th/

# Installation

```bash
pip install camp_parser
```

# Usage

## Get CampInfro

```python
from camp_parser import camphub_parser # or any thing thatREADME.rst we support
camp = camphub_parser('https://www.camphub.in.th/computer/') #page url
print(camp.info) #get the information
```

## Fetch many pages at once

```python
from camp_parser import camphub_parser # or any thing
if __name__ == '__main__':
    camp = camphub_parser('https://www.camphub.in.th/computer/') #page url

    print(camp.page_fetching('https://www.camphub.in.th/computer/', pages = 50))
    print(camp.page_fetching('https://www.camphub.in.th/computer/', pages = 50, workers = -1)) # Enable Multiprocessing
```

## Information structure

```python
{
    'title': 'title of the camp',
    'link': 'link to the camp page',
    'small_description': 'mified description of the camp',
    'type': 'event type (onsite/online/etc...)',
    'organize_date': 'start date of the camp',
    'register_deadline': 'last day yu can register to the camp',
    'max_paticipants': '(string not number Ex. ไม่จำกัด, 200ค คน)',
    'costs': 'cost of the camp Ex. ฟรี, 1000 บาท',
    'paticipants_requirements': 'what you need to join the camp',
    'organizer': 'who organize the camp',
    'full_description': 'full description of the camp',

}
```
