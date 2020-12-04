# Teachable Camera Hardware

## Introduction

This repository contains the design files that we used for building a Teachable Camera. The Teachable Camera is built using the [Google Coral Dev Board](https://coral.ai/products/dev-board), commercially available components, and a few 3D printed parts. We experimented with a number of different design configurations to aid in development and allow the system to be tested in a more realistic environment.

<img src="./images/001.jpg" alt="assembly" width="50%">

_Teachable Camera in the wild_

## Software

For details about the software that runs on the Coral see the [Teachable Camera Software](https://github.com/IQTLabs/Teachable-Camera) repository

## Design Configurations

There were three designs that we experimented with during the development of the project.

### [Design 1 - Benchtop Testing (Simple 3D Printed Coral Case)](./design-1.md)

The Benchtop Testing hardware is a simple case configuration that houses the Google Coral Development Board and provides a mount which allows you to aim the Coral Camera. The enclosure is 3D printed and provides basic protection for the electronics. This configuration was used to do most of the development and testing of the system.

<a href="./design-1.md"><img src="./images/design-1.jpg" alt="assembly" width="50%"></a>

See [Design 1 page](./design-1.md) for more details.

### [Design 2 - Light Field Deployment (Coral in Pelican Case with USB Battery)](./design-2.md)

The Light Field Deployment hardware is a simple configuration with a durable case that houses the Google Coral Development Board and large USB battery. This configuration is built upon a 3D printed chassis that holds the Coral, camera, and battery, and is mounted inside a small Pelican case. The configuration allows the system to be deployed in areas without power for short durations and provides more protection when transporting/shipping the system. With a 26800mAh USB battery the system will operate for approximately 10 hours.

<a href="./design-2.md"><img src="./images/design-2.jpg" alt="assembly" width="50%"></a>

See [Design 2 page](./design-2.md) for more details.

### [Design 3 - Extended Run Field Deployment (Coral in Pelican Case, GoalZero Battery, Ubiquity IP Camera](./design-3.md)

The Extended Run Field Deployment hardware is an advanced configuration with a durable case that houses the Google Coral Development Board, a GoalZero battery/solar power system, and a PoE Ubiquity G3 Pro security camera. 

<a href="./design-3.md"><img src="./images/design-3.jpg" alt="assembly" width="50%"></a>

See [Design 3 page](./design-3.md) for more details.

## Design Features of Note

### Power/Solar

For the field system (Design 3) power we chose the GoalZero [200X power supply](https://www.goalzero.com/shop/portable-power/goal-zero-yeti-200x/) and the [Boulder 50W](https://www.goalzero.com/shop/solar-panels/boulder-50-solar-panel/) solar panel. The GoalZero power supplies are consumer friendly, the X series is light weight, and there are lots of options for additional battery or solar capacity.

### PoE Power

We needed a way to power the Ubiquity Power over Ethernet (PoE) IP camera using a 5V battery but were unable to located a commerical solution. To solve this we sourced [DC-DC transformer](https://www.amazon.com/Yeeco-Converter-Adjustable-Transformer-Stabilizer/dp/B074J9D278/ref=sr_1_11?dchild=1&keywords=5v+to+48v&qid=1598463288&sr=8-11) to step up the battery voltage from 5V to 48V coupled with a generic [PoE injector](https://www.amazon.com/WS-GPOE-1-WM-Gigabit-Passive-Ethernet-Injector/dp/B00ENNUWO4/ref=sr_1_3?crid=3F1UOEQOGUEO&dchild=1&keywords=24v+poe+injector+dc&qid=1591818504&sprefix=24v+poe+i%2Caps%2C146&sr=8-3) to power the camera. This solution ended up working quite well and could probably be utilized for other projects too. 

### 3D Printing

The 3D printed parts were printed with the Prusa i3 mk3 using PETG filament. PETG is a high temperature material and seems to hold up well even in the summer heat.

## Third Party Files 3D Models

In addition to the models included in this repository, the following files from GRAB CAD were also used in the SolidWorks Assembly for illustration purposes.

- https://grabcad.com/library/google-coral-dev-board-1
- https://grabcad.com/library/coral-camera-1
- https://grabcad.com/library/pelican-case-1150-1
- https://grabcad.com/library/tripod-gtt204-1

## License

<p xmlns:dct="http://purl.org/dc/terms/" xmlns:cc="http://creativecommons.org/ns#" class="license-text">This work by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://www.iqt.org/labs/">IQT Labs LLC</a> is licensed under <a rel="license" href="https://creativecommons.org/licenses/by/4.0">CC BY 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" /><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" /></a></p>