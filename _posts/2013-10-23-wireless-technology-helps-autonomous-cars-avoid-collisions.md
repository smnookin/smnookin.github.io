---
layout: post
published: true
title: Wireless Technology Helps Autonomous Cars Avoid Collisions
category: science
author: Leo Liu
tags: 
  - student
displaydate: "2013-10-20"
date: "2013-10-20"
---

![](http://upload.wikimedia.org/wikipedia/commons/thumb/6/65/Hands-free_Driving.jpg/800px-Hands-free_Driving.jpg) Automakers are expecting autonomous cars to be commercially available by the end of the decade, but the cars have to overcome one crucial flaw first.
Just like human drivers, autonomous cars have blind spots. According to the National Highway Traffic Safety Administration, blind spots cause 840,000 collisions and 300 fatalities a year in the U.S. The sensors on the cars can only view objects in their lines of sight. But MIT researchers are aiming to solve this problem by letting cars wirelessly share information about potential dangers.

The goal of autonomous vehicles is to move safely and efficiently without the need for a human driver. They use sensors that collect data about their surroundings and feed that data into an onboard computer that plans the car’s movements. 

To solve the problem of blind spots, Swarun Kumar, a Ph.D. student in computer science at MIT, and other researchers from the networks research group at MIT developed technology that presents a new way to represent information about the environment and a method of wirelessly sharing it among the cars. It’s called CarSpeak.

Autonomous car sensors typically generate gigabytes of data every second - far too much to share wirelessly, Kumar said. To simplify the situation, CarSpeak represents the entire 3-D environment as cubes. Each cube is marked as “occupied”, “empty”, or “unknown” depending on whether the sensors detect an object inside the corresponding location.

Using wireless communication, a car equipped with CarSpeak can ask other cars whether a particular location is occupied. Nearby cars enabled with CarSpeak reply with the state of the corresponding cube; the first car uses the replies to avoid collisions. This new representation is especially useful for storage and transmission because it is more compact.

The main challenge of wireless communication is that two devices cannot transmit at the same time; otherwise, the data will not reach its destination. Dorothy Curtis, a computer science researcher at MIT, explained that wireless signals get mixed together during simultaneous transmissions. The data is lost because there is no way to “untangle the signals.” 

One solution is to use 802.11, which is the method used by laptops to connect to the Internet. 802.11 prevents simultaneous transmissions by fairly dividing up the possible transmissions among the devices. In the paper, Kumar pointed out that 802.11 unfortunately doesn’t work well for cars. If twenty cars held information about a particular cube, and only one car had information about a second cube, then 802.11 would allow for twenty times more transmissions related to the first cube than the second one, delaying the transmission of information about the second cube. These delays would become much worse as the number of cars increases.

To solve this problem, the researchers introduced an alternative to 802.11. The new method divides the transmissions evenly among the cubes of location information, instead of the number of cars. Kumar says that their method will improve the ability of autonomous vehicles to communicate “regardless of how they move.” 

The team evaluated their system on ten miniature robots, each the size of a Roomba, placed in a room with obstacles. Robots using 802.11 collided due to the delays in receiving information, and robots using CarSpeak didn’t. The researchers also tested CarSpeak on an autonomous golf cart and found that it stopped even if it was a meter away from a pedestrian emerging from a blind spot.

According to Kumar, research in autonomous vehicles usually treats the communication system as a black box and focus on its uses. In contrast, his team focused on the communication system to deliver the best performance for this particular application.

All in all, cars with Carspeak navigated around obstacles 2.4 times quicker and were 14 times less likely to crash than other cars.

Carspeak could also benefit human drivers by providing advanced warnings about obstacles they cannot see, said Kumar. This application seems especially promising to Curtis, whose family member was involved in an accident caused by a blind spot. 

Kumar and his team are currently in talks with members of the automobile industry to introduce CarSpeak into future autonomous and semi-autonomous cars. They are also working on ways to broaden CarSpeak’s applications and further improve its communication efficiency.