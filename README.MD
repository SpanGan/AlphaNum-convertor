
The main.py file automatically converts alpha.num pattern to a reference alpha.num pattern in text. You can exclude parts of the pattern that you want preserved. For example, if you want to copy an eye colour  but want to preserve the rest  of the sequences being changed.

Sequence = Format: aa.000.000.000.000_ab_....._fv1.0 

Operation 

- Original   aa23.100.222.133.666
- Reference  aa1.0.0.0.0
- Change 1st and 3rd numeral to reference
- Output     aa1.100.0.133.666

**Components**

1. Json’s used as general reference.
    
	i. Menu_names.json
   	ii. Parts_Names.json

2. CSV where the results of the conversion will appear.
    	i. Loader and dumper.csv

4. main.py

***How to use***

1. Open the "Loader and dumper.csv".Copy the sequences you want to convert under the **Input column**, below the headings.
**Make sure to fill out the Name column(You can simply number the Name column. Ensure the columns are of same Length.)**. You can ignore the id column if you wish, it will be auto populated serially.

2. Next, paste the string containing the sequence you want to convert to the place shown (E2 cell in loader and dumper). For ease, I recommend exporting only the relevant parts of the sequence string. *For example*, If I only want to change the eye colour of the characters, I will select the Eye tab and export only that.
Then I can exclude everything but eye colour.

3. **Close the CSV file after saving.**

4. Now run the program by double clicking it or through command line. **The Choice you choose next will be excluded from the conversion.**

5. **The program will ask you to type in a choice from the given list**(*Case is ignored.*). It will also try to match you inputs by order of letters, so feel free to only type parts of the word. 
**Press enter to confirm. Leave empty to move to next step** 
E.g.:   
	a. [[Pose],[FootPose],[Eye],[Hair]....]
        b. [[Pose,aa],[Pose,ab],.....]
        c. [[Pose,aa,LeftArmLength_0],.....]

6. Now, a list of numbered matches will be shown. Type in the number  of the option you want and press enter to confirm. **Here, you can make multiple choices. Leave empty and press enter to continue. You will return to the above choice.**   
E.g.:*for "foot"  typed=*
    [(1,Pose),(2,FootPose)]

7. This process will repeat 2 more times. 

8. Once the process ends, your output will be added to the output column in the Csv, with the character converted except for the exclusions you have made. Enjoy.

**Notes**

Special Thanks to KisekaeJade for the explanation of how the Save system works.


