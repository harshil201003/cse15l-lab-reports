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


2. The second function we will be talking about here will be `grep -i`. It is a case insensitive function. It finds all the words depite the capitalization. It can be really helpful because it helps eliminate the chances of not finding a certain element because of capitalization. Examples have been provided below - 


    + In the first example, we search for the word "FIVE", and despite the search string beig capitalized, the terminal results with an output.


        `grep -i "FIVE" technical/911report/preface.txt`
        
        The output window is as follows -
        
        
        ```
                        people for their consideration. Ten Commissioners-five Republicans and five
        ```
        
        
    + In the second example, we search for "allocation" -


        `grep -i "AllOCAtion" technical/911report/preface.txt`
        
        The output window was -
        
        `                aviation, the role of congressional oversight and resource allocation, and other`
        
        
    + The third example involves searching for "CLEVELAND?"


        `grep -i "CLEVELAND?" technical/911report/chapter-1.txt`
        
        
        The output was - 
        
        
        ```
            The controller responded, seconds later: "Somebody call Cleveland?"This was followed by a second radio transmission, with sounds of screaming. The Cleveland Center controllers began to try to identify the possible source of the transmissions, and noticed that United 93 had descended some 700 feet. The controller attempted again to raise United 93 several times, with no response. At 9:30, the controller began to poll the other flights on his frequency to determine if they had heard the screaming; several said they had.
        ```


3. The third function we willbe discussing here is `grep -r`. It looks through a sub-directory with txt files and finds matches. It can be very useful when finding a specific string throughout a big subdirectory. This can be used by employers looking for specific words while hiring individuals or by universities looking at appications Examples have been provided below - 


    + The first example involves searching for the word "nonterrorists" in 911report


        `grep -r "nonterrorists" ./technical/911report/*`
        
        
        The output window was - 
        
        
        ```
        ./technical/911report/chapter-13.5.txt:                Medical Examiner's Office, the WTC attacks killed 2,749 nonterrorists, including
        ./technical/911report/chapter-13.5.txt:                Pentagon attack killed 184 nonterrorists, including the occupants of the hijacked
        ./technical/911report/chapter-13.5.txt:                nonterrorists died in the crash of United Airlines Flight 93 in Pennsylvania. FBI
        ```
        

    + The second example involves searching for "first class" in techincal

        
        `grep -r "first class" ./technical/*`
        
        
        
        The output was as follows - 
        
        
        ```
        ./technical/911report/chapter-13.2.txt:                Bobbi Arestegui in first class; Sara Low and Jean Roger in business class; Dianne
        ./technical/911report/chapter-13.2.txt:                assist in first class if needed. See AAL report, "Flight Attendant Jump Seat
        ./technical/911report/chapter-13.2.txt:                cabin service in first class; with Amy King and Robert Fangman in business class;
        ./technical/911report/chapter-13.2.txt:                first class. See Don Dillman briefing (Nov. 18, 2003); Bob Jordan briefing (Nov. 20,
        ./technical/911report/chapter-13.2.txt:                hijackers arrayed themselves similarly: two seated in first class close to the
        ./technical/911report/chapter-13.2.txt:                been in first class; and Kenneth Lewis would have been in the main cabin. On cabin
        ./technical/911report/chapter-13.2.txt:                Deborah Welsh (first class, seat J1 at takeoff); Sandra Bradshaw (coach, seat J5);
        ./technical/911report/chapter-13.2.txt:                Wanda Green (first class, seat J4); Lorraine Bay (coach, seat J3); and CeeCee Lyles
        ./technical/911report/chapter-1.txt:    At 7:50, Majed Moqed and Khalid al Mihdhar boarded the flight and were seated in 12A and 12B in coach. Hani Hanjour, assigned to seat 1B (first class), soon followed. The Hazmi brothers, sitting in 5E and 5F, joined Hanjour in the first-class cabin.
        ./technical/911report/chapter-1.txt:    Reports from two flight attendants in the coach cabin, Betty Ong and Madeline "Amy" Sweeney, tell us most of what we know about how the hijacking happened. As it began, some of the hijackers-most likely Wail al Shehri and Waleed al Shehri, who were seated in row 2 in first class-stabbed the two unarmed flight attendants who would have been preparing for cabin service.
        ./technical/911report/chapter-1.txt:    Sweeney calmly reported on her line that the plane had been hijacked; a man in first class had his throat slashed; two flight attendants had been stabbed-one was seriously hurt and was on oxygen while the other's wounds seemed minor; a doctor had been requested; the flight attendants were unable to contact the cockpit; and there was a bomb in the cockpit. Sweeney told Woodward that she and Ong were trying to relay as much information as they could to people on the ground.
        ./technical/911report/chapter-1.txt:    At 8:41, Sweeney told Woodward that passengers in coach were under the impression that there was a routine medical emergency in first class. Other flight attendants were busy at duties such as getting medical supplies while Ong and Sweeney were reporting the events.
        ./technical/911report/chapter-1.txt:    Because several passengers on United 93 described three hijackers on the plane, not four, some have wondered whether one of the hijackers had been able to use the cockpit jump seat from the outset of the flight. FAA rules allow use of this seat by documented and approved individuals, usually air carrier or FAA personnel. We have found no evidence indicating that one of the hijackers, or anyone else, sat there on this flight. All the hijackers had assigned seats in first class, and they seem to have used them. We believe it is more likely that Jarrah, the crucial pilot-trained member of their team, remained seated and inconspicuous until after the cockpit was seized; and once inside, he would not have been visible to the passengers.
        ./technical/911report/chapter-1.txt:    At 9:57, the passenger assault began. Several passengers had terminated phone calls with loved ones in order        to join the revolt. One of the callers ended her message as follows:"Everyone's running up to first class. I've got to go. Bye."
        ./technical/911report/chapter-5.txt:                Hong Kong aboard a U.S. airliner. He flew in first class, which he realized was a
        ./technical/911report/chapter-7.txt:                While this travel may have been a casing flight-Shehri traveled in first class on
        ./technical/911report/chapter-7.txt:                the end of June. Each traveled in first class, on United Airlines. For the east-west
        ./technical/911report/chapter-7.txt:                flew in first class on the same type of aircraft they would hijack on 9/11 (a Boeing
        ./technical/biomed/1471-2164-3-9.txt:        classes. The first class is comprised of short coiled-coil
        ./technical/biomed/1471-2121-3-18.txt:        including the first class of adaptor proteins with SH2 or
        ./technical/government/Gen_Account_Office/gg96118.txt:first class in September 1995, the GPRA training has been
        ./technical/government/Media/Good_guys_reward.txt:After graduating in CUNY Law School's first class in 1986, he
        ./technical/plos/pmed.0020002.txt:        coccidioidomycosis. The first class is the polyenes, with amphotericin B desoxycholate and
        ./technical/plos/journal.pbio.0030102.txt:        With their strange morphology, vent tubeworms were first classified as a novel phylum,
        ```
        
    + The last example involves searching for a word that does not exist in the files, "hello" -

        
        `grep -r "hello" ./technical/*`
        
        This does not result in an output window because hello does not exist in the files



This concludes the lab report.



