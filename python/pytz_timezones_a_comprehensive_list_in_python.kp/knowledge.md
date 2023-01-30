---
title: Do you know where I can find a list of pytz timezones?
authors:
- smart_coder
tags:
- python
- knowledge
thumbnail: images/python.png
created_at: 2023-01-30 00:00:00
updated_at: 2023-01-30 00:00:00
tldr: Yes, a list of Pytz Timezones in Python can be found at https//gist.github.com/heyalexej/8bf688fd67d7199be4a1682b3eec7568.
---

**Contents**

[TOC]

**Section 1: Pytz Documentation**

The official documentation for Pytz can be found here:

https://pytz.readthedocs.io/en/latest/

The documentation includes a list of all the available timezones in Pytz.

**Section 2: List of Timezones**

The following is a list of the available timezones in Pytz:

Africa/Abidjan
Africa/Accra
Africa/Addis_Ababa
Africa/Algiers
Africa/Asmara
Africa/Bamako
Africa/Bangui
Africa/Banjul
Africa/Bissau
Africa/Blantyre
Africa/Brazzaville
Africa/Bujumbura
Africa/Cairo
Africa/Casablanca
Africa/Ceuta
Africa/Conakry
Africa/Dakar
Africa/Dar_es_Salaam
Africa/Djibouti
Africa/Douala
Africa/El_Aaiun
Africa/Freetown
Africa/Gaborone
Africa/Harare
Africa/Johannesburg
Africa/Juba
Africa/Kampala
Africa/Khartoum
Africa/Kigali
Africa/Kinshasa
Africa/Lagos
Africa/Libreville
Africa/Lome
Africa/Luanda
Africa/Lubumbashi
Africa/Lusaka
Africa/Malabo
Africa/Maputo
Africa/Maseru
Africa/Mbabane
Africa/Mogadishu
Africa/Monrovia
Africa/Nairobi
Africa/Ndjamena
Africa/Niamey
Africa/Nouakchott
Africa/Ouagadougou
Africa/Porto-Novo
Africa/Sao_Tome
Africa/Tripoli
Africa/Tunis
Africa/Windhoek

**Section 3: Using the List**

The list of timezones can be used to set the timezone for a datetime object in Python. For example, the following code sets the timezone to Africa/Nairobi:

import datetime
import pytz

tz = pytz.timezone('Africa/Nairobi')
now = datetime.datetime.now(tz)

**Section 4: Additional Resources**

For more information on using Pytz, please refer to the official documentation:

https://pytz.readthedocs.io/en/latest/
