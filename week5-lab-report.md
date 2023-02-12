# Week 5 Lab Report

Vivian Wang    A17457779    v8wang@ucsd.edu

## Researching Command: `grep`

### `grep -w`

This command only prints the results that has the whole-word matched. Without this command, it will still be printed as a result even if the word is a substring of another word

* Example 1:
  ```
  % grep -w "Hawaii" written_2/travel_guides/berlitz1/HandRHawaii.txt
          Kahala Mandarin Oriental Hawaii $$$$ 5000 Kahala Avenue,
          Big Island of Hawaii
          the world for years, and it is still one of Hawaii’s premier oceanfront
          the best hotel pools and swimming beaches in Hawaii. 419 rooms.
  ```

* Example 2:
  ```
  % grep -w "Sharon" written_2/non-fiction/OUP/Berk/*.txt
  written_2/non-fiction/OUP/Berk/ch1.txt:•Bob and Sharon, parents of a 4-year-old: Our daughter, Lydia, could recite her ABCs and count from 1 to 20 by age 2 1/2. When we looked for a preschool, many programs appeared to do little more than let children play, so we chose one with lots of emphasis on academics. To me, Lydia’s preschool seems like great preparation for kindergarten and ﬁrst grade, but each morning, Lydia hates to go. Why is Lydia, who’s always been an upbeat, curious child, so unhappy?
  written_2/non-fiction/OUP/Berk/ch2.txt:Furthermore, prior to this age, children have diculty inferring characters’ motives and connecting contradictory TV scenes into a coherent story line. They cannot appreciate why a character who at ﬁrst seemed like a “good guy” but later behaves aggressively is really a “bad guy.” They evaluate such characters and their actions much too favorably.110 For example, psychologist Sharon Purdie showed second graders a complex dramatic program in which an accused kidnapper, who had at ﬁrst appeared friendly, tried to shoot a prosecution witness and got arrested during the attempt. Children who failed to grasp the kidnapper’s motive and the reason for the arrest judged him to be “good,” not “bad.”111
  ```

### `grep -i`

This command ignore cases when searching.

* Example 1:
  ```
  % grep -i "hong" written_2/travel_guides/berlitz1/HandRHongKong.txt
          Hong Kong has some of the most luxurious hotels in the
          limited room service, and a wide range of facilities. Hong Kong hotels
          arrangements, the Hong Kong Hotel Reservation Center at the
          indicate high-season rates in Hong Kong dollars, based on double
  ```

* Example 2:
  ```
  % grep -i "the" written_2/travel_guides/berlitz1/HandRIbiza.txt
          The establishments listed below offer a cross-section of
          local restaurants, and should convince you that not everything on the
          The star rating in brackets after each entry refers to the
          As a basic guide, the symbols we use indicate what you can
          tip. Drinks will add considerably to the final bill.
  ```

### `grep -r`

This command search recursively through all the subdirectories.

* Example 1:
  ```
  % grep -r "Ebusus" written_2/travel_guides/berlitz1
  written_2/travel_guides/berlitz1/HistoryIbiza.txt:        Ebysos, the Romans called it Ebusus, and the Moors, Yebisah.
  ```

* Example 2:
  ```
  % grep -r "Sharon" written_2
  written_2/non-fiction/OUP/Berk/ch2.txt:Furthermore, prior to this age, children have diculty inferring characters’ motives and connecting contradictory TV scenes into a coherent story line. They cannot appreciate why a character who at ﬁrst seemed like a “good guy” but later behaves aggressively is really a “bad guy.” They evaluate such characters and their actions much too favorably.110 For example, psychologist Sharon Purdie showed second graders a complex dramatic program in which an accused kidnapper, who had at ﬁrst appeared friendly, tried to shoot a prosecution witness and got arrested during the attempt. Children who failed to grasp the kidnapper’s motive and the reason for the arrest judged him to be “good,” not “bad.”111
  written_2/non-fiction/OUP/Berk/ch1.txt:•Bob and Sharon, parents of a 4-year-old: Our daughter, Lydia, could recite her ABCs and count from 1 to 20 by age 2 1/2. When we looked for a preschool, many programs appeared to do little more than let children play, so we chose one with lots of emphasis on academics. To me, Lydia’s preschool seems like great preparation for kindergarten and ﬁrst grade, but each morning, Lydia hates to go. Why is Lydia, who’s always been an upbeat, curious child, so unhappy?
  written_2/travel_guides/berlitz1/WhereToIsrael.txt:        It is also the capital of the Sharon Plain citrus-growing area and the
  ```

### `grep -c`

This command prints the filenames with the number of lines that has the string.

* Example 1:
  ```
  % grep -c "they" written_2/non-fiction/OUP/Berk/*.txt
  written_2/non-fiction/OUP/Berk/CH4.txt:72
  written_2/non-fiction/OUP/Berk/ch1.txt:52
  written_2/non-fiction/OUP/Berk/ch2.txt:61
  written_2/non-fiction/OUP/Berk/ch7.txt:56
  ```

* Example 2:
  ```
  % grep -c "Hong Kong" written_2/travel_guides/berlitz1/HandR*.txt
  written_2/travel_guides/berlitz1/HandRHawaii.txt:0
  written_2/travel_guides/berlitz1/HandRHongKong.txt:4
  written_2/travel_guides/berlitz1/HandRIbiza.txt:0
  written_2/travel_guides/berlitz1/HandRIsrael.txt:0
  written_2/travel_guides/berlitz1/HandRIstanbul.txt:0
  written_2/travel_guides/berlitz1/HandRJamaica.txt:1
  written_2/travel_guides/berlitz1/HandRJerusalem.txt:0
  written_2/travel_guides/berlitz1/HandRLakeDistrict.txt:0
  written_2/travel_guides/berlitz1/HandRLasVegas.txt:0
  written_2/travel_guides/berlitz1/HandRLisbon.txt:0
  written_2/travel_guides/berlitz1/HandRLosAngeles.txt:0
  written_2/travel_guides/berlitz1/HandRMadeira.txt:0
  written_2/travel_guides/berlitz1/HandRMadrid.txt:0
  written_2/travel_guides/berlitz1/HandRMallorca.txt:0
  ```

### Resource:

https://phoenixnap.com/kb/grep-command-linux-unix-examples