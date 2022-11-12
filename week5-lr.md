# WEEK 5 Lab Report

## Researching Commands 

The command that we will be discussing in detail will be `grep`. Grep takes a string and a file, and prints out all the lines in that file
that match the string. 



1. The first example is `grep -w`. This function of grep returns whole words instead of parts of the word. Example being if we search
for the string "lemon", it will only return the instances of the word "lemon" in the search file. Default grep would also return "lemonade" with "lemon".
The terminal code has been provided below.


    `grep -w "string" (filename)`


    + For the first example, the input command was as follows - 


        `grep -w "four" technical/911report/chapter-1.txt`


        The output windows has been given below for the first example -


        ```
        The four men passed through the security checkpoint, owned by United Airlines and operated under contract by Argenbright Security. Like the checkpoints in Boston, it lacked closed-circuit television surveillance so there is no documentary evidence to indicate when the hijackers passed through the checkpoint, what alarms may have been triggered, or what security procedures were administered. The FAA interviewed the screeners later; none recalled anything unusual or suspicious.
        The four men boarded the plane between 7:39 and 7:48. All four had seats in the first-class cabin; their plane had no business-class section. Jarrah was in seat 1B, closest to the cockpit; Nami was in 3C, Ghamdi in 3D, and Haznawi in 6B.
        The 19 men were aboard four transcontinental flights.
        At the same time or shortly thereafter, Atta-the only terrorist on board trained to fly a jet-would have moved to the cockpit from his business-class seat, possibly accompanied by Omari. As this was happening, passenger Daniel Lewin, who was seated in the row just behind Atta and Omari, was stabbed by one of the hijackers-probably Satam al Suqami, who was seated directly behind Lewin. Lewin had served four years as an officer in the Israeli military. He may have made an attempt to stop the hijackers in front of him, not realizing that another was sitting behind him.
        The Hijacking of American 77 American Airlines Flight 77 was scheduled to depart from Washington Dulles for Los Angeles at 8:10. The aircraft was a Boeing 757 piloted by Captain Charles F. Burlingame and First Officer David Charlebois. There were four flight attendants. On September 11, the flight carried 58 passengers.
        The terrorists who hijacked three other commercial flights on 9/11 operated in five-man teams. They initiated their cockpit takeover within 30 minutes of takeoff. On Flight 93, however, the takeover took place 46 minutes after takeoff and there were only four hijackers. The operative likely intended to round out the team for this flight, Mohamed al Kahtani, had been refused entry by a suspicious immigration inspector at Florida's Orlando International Airport in August.
        Because several passengers on United 93 described three hijackers on the plane, not four, some have wondered whether one of the hijackers had been able to use the cockpit jump seat from the outset of the flight. FAA rules allow use of this seat by documented and approved individuals, usually air carrier or FAA personnel. We have found no evidence indicating that one of the hijackers, or anyone else, sat there on this flight. All the hijackers had assigned seats in first class, and they seem to have used them. We believe it is more likely that Jarrah, the crucial pilot-trained member of their team, remained seated and inconspicuous until after the cockpit was seized; and once inside, he would not have been visible to the passengers.
        FAA Control Centers often receive information and make operational decisions independently of one another. On 9/11, the four hijacked aircraft were monitored mainly by the centers in Boston, New York, Cleveland, and Indianapolis. Each center thus had part of the knowledge of what was going on across the system. What Boston knew was not necessarily known by centers in New York, Cleveland, or Indianapolis, or for that matter by the Command Center in Herndon or by FAA headquarters in Washington.
        Controllers track airliners such as the four aircraft hijacked on 9/11 primarily by watching the data from a signal emitted by each aircraft's transponder equipment. Those four planes, like all aircraft traveling above 10,000 feet, were required to emit a unique transponder signal while in flight.
        On 9/11, the terrorists turned off the transponders on three of the four hijacked aircraft. With its transponder off, it is possible, though more difficult, to track an aircraft by its primary radar returns. But unlike transponder data, primary radar returns do not show the aircraft's identity and altitude. Controllers at centers rely so heavily on transponder signals that they usually do not display primary radar returns on their radar scopes. But they can change the configuration of their scopes so they can see primary radar returns. They did this on 9/11 when the transponder signals for three of the aircraft disappeared.
        In summary, NEADS received notice of the hijacking nine minutes before it struck the North Tower. That nine minutes' notice before impact was the most the military would receive of any of the four hijackings. 
        ```



    + Another example of searching a part of the word -


        `grep -w "Pres" technical/911report/preface.txt`



        This does not reslt in an answer because there is no complete word "Pres" in preface.txt


    + A full word like "President", however results in the word being found.



      `grep -w "President" technical/911report/preface.txt`


      The output window was -


      ```
                      the President of the United States, the United States Congress, and the American
                  To answer these questions, the Congress and the President created the National
                      have been superb. We thank the Congress and the President. Executive branch agencies
      ```


2. The second function we will be talking about here will be `grep -i`. It is case insensitive. It finds all the words depite the capitalization. It can be really helpful because it helps eliminate the chances of not finding a certain element because of capitalization. Examples have been provided below - 


<img width="647" alt="Screenshot 2022-10-31 at 7 02 58 PM" src="https://user-images.githubusercontent.com/114549600/199142932-8c7b596f-8d4c-4db2-a0c5-08c8e03b0d5e.png">


<img width="707" alt="Screenshot 2022-10-31 at 7 05 14 PM" src="https://user-images.githubusercontent.com/114549600/199142945-6f969dc0-b16b-488f-b31c-57d3afce23b0.png">


<img width="1712" alt="Screenshot 2022-10-31 at 7 06 04 PM" src="https://user-images.githubusercontent.com/114549600/199142958-866eb527-5b89-4ee5-be68-cc708e44b768.png">



The third function we willbe discussing here is `grep -r`. It looks through a sub-directory with txt files and finds matches. Examples are given below -


<img width="962" alt="Screenshot 2022-10-31 at 7 27 27 PM" src="https://user-images.githubusercontent.com/114549600/199145351-cc96f74d-58b7-40ff-94d6-3dc43e1b8413.png">


<img width="1710" alt="Screenshot 2022-10-31 at 7 28 42 PM" src="https://user-images.githubusercontent.com/114549600/199145522-b044bd91-6685-471f-ad31-88adeb11b831.png">


<img width="456" alt="Screenshot 2022-10-31 at 7 28 57 PM" src="https://user-images.githubusercontent.com/114549600/199145543-8ac0b88c-ccc4-42fb-b38c-938200a93349.png">



This concludes the laab report.



