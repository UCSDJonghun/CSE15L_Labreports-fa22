# Week 5 Lab Report

* The grep command allows you to search one file or multiple files for lines that contain a pattern. Exit status is 0 if matches were found, 1 if no matches were found, and 2 if errors occurred.

## The 'grep' command: Option -i

* when searching ignore uppercase vs lowercase.
* Useful : This searches for the given string/pattern case insensitively. so it masthces all the words insensitively as shown below.

Example 1: "Korea"

```
[cs15lfa22lp@ieng6-201]:skill-demo1:168$ grep -i "Korea" technical/*/*.txt       
technical/911report/chapter-11.txt:                in Korea another. But these were attacks by major powers. While by no means as
technical/911report/chapter-11.txt:                the main focus (war in Korea), and as too unrealistic. As we pointed out in chapter
technical/911report/chapter-12.txt:                not experienced such a rapid surge in national security spending since the Korean
technical/911report/chapter-13.4.txt:                Khallad, Aug. 13, 2003; Apr. 5, 2004. According to Khallad, Thailand, South Korea,
technical/911report/chapter-5.txt:                Singapore, or Korea.) This part of the operation has been confirmed by Khallad, who
technical/911report/chapter-5.txt:                Thailand, South Korea, Hong Kong, or Malaysia, and using Yemenis who would not need
technical/911report/chapter-6.txt:                emphasized other issues such as North Korea and the Israeli- Palestinian peace
technical/911report/chapter-6.txt:                with the faltering Middle East 
peace process and North Korea. Clarke said that the
technical/biomed/1471-2148-2-17.txt:          Korea, and was previously considered a species of subg.
technical/biomed/1471-2148-2-17.txt:          Europe and the Far East in Manchuria, Korea, and Japan.
technical/biomed/1471-2156-3-11.txt:          from SeeGene (Seoul, Korea). The
technical/biomed/1472-6823-2-2.txt:          Jolla, CA; Sofia, Bulgaria; Seoul, South Korea and São
technical/biomed/1472-6823-2-2.txt:          Brazil; The Catholic University of Korea, Seoul, South
technical/biomed/1472-6823-2-2.txt:          Korea). No information that would identify the subjects
technical/biomed/1472-6920-2-3.txt:        South Korea [ 5 ] and for a Turkish medical school [ 6 ] .
technical/plos/journal.pbio.0020121.txt:        imported cases in the Republic of Korea, but surveillance has not been thorough in North
```
* I got all words include "Korea" 

Example 2: "fbi"
```
[cs15lfa22lp@ieng6-201]:skill-demo1:168$ grep -i "fbi" technical/*/*.txt      
technical/911report/chapter-8.txt:            On September 4, the FBI sent a teletype to the CIA, the FAA, the Customs Service, the
technical/911report/chapter-8.txt:                Moussaoui, FBI headquarters instructed Minneapolis that it could not share the more
technical/911report/chapter-8.txt:                were gaps in the FBI headquarters teletype.
technical/911report/chapter-8.txt:            There was substantial disagreement between Minneapolis agents and FBI headquarters as
technical/911report/chapter-8.txt:            There is no evidence that either FBI 
Acting Director Pickard or Assistant Director
technical/911report/chapter-8.txt:                Michael Rolince, the FBI assistant director heading the Bureau's
technical/911report/chapter-8.txt:                case on August 27, he declined to go up the chain of command at FBI headquarters and
technical/911report/chapter-8.txt:                flight from London to New York. He was told that the FBI had arrested Moussaoui
technical/911report/chapter-8.txt:                because of a visa overstay and that the CIA was working the case with the FBI. Tenet
technical/911report/chapter-8.txt:                an FBI case, he did not discuss the matter with anyone at the White House or the
technical/911report/chapter-8.txt:                FBI. No connection was made between Moussaoui's presence in the United States and
technical/911report/chapter-8.txt:            On September 11, after the attacks, the FBI office in London renewed their appeal for
technical/911report/chapter-8.txt:            The FBI also learned after 9/11 that 
the millennium terrorist Ressam, who by 2001 was
technical/911report/chapter-8.txt:            As mentioned above, before 9/11 the FBI agents in Minneapolis had failed to persuade
technical/911report/chapter-9.txt:                authority delegated to the FBI for operational response). Additionally, the
technical/911report/chapter-9.txt:                State Police, the Virginia Department of Emergency Management, the FBI, FEMA, a
technical/911report/chapter-9.txt:                because of the warning of an approaching hijacked aircraft passed along by the FBI.
technical/911report/preface.txt:                insight. The PENTTBOM team at the FBI, the Director's Review Group at the CIA, and
technical/biomed/1471-2121-2-12.txt:        p14 Arfgene [ 2]. p14 Arfbinds to and sequesters mdm2,
technical/biomed/1471-2164-4-6.txt:        http://www.cstl.nist.gov/biotech/strbase/fbicore.htm.
technical/biomed/gb-2002-3-10-research0055.txt:          TGFBI, LPL and LDLR were the origin of serious disorders:
```
* There are more results. I typed "fbi" it finds instances of "FBI" because it ignores cases

Example 3: "ucsd"
```
[cs15lfa22lp@ieng6-201]:skill-demo1:171$ grep -i "ucsd" technical/*/*.txt
technical/biomed/1471-2091-3-30.txt:        Insel, UCSD) demonstrated constitutive 
activation of ERKs
technical/biomed/1471-2121-2-22.txt:        http://ncmir.ucsd.edu/~perkins/tBid. For example, it became
technical/biomed/1471-2164-3-18.txt:          http://genome.ucsd.edu/index.html [ 54 55 ] . The
technical/biomed/1471-2407-2-15.txt:          UCSD Viral Vector Core. The plasmids 
were co-transfected
technical/biomed/1471-2407-2-15.txt:          approved by the animal care committee at UCSD. The cells
technical/biomed/1471-244X-3-5.txt:          UCSD Medical Center, La Jolla, during 
July and August of
technical/biomed/1472-6823-2-2.txt:          respective local human IRBs (UCSD, La 
Jolla, CA; Veterans
technical/biomed/1476-4598-2-2.txt:          Ludwig Institute of Cancer Research at UCSD. The tumor
technical/biomed/bcr620.txt:          UCSD Medical Center. Samples were obtained in random
technical/biomed/bcr620.txt:          approval of the UCSD Institutional Review Board for
technical/plos/journal.pbio.0020064.txt:        field, including collaborators Charles Zuker (University of California, San Diego [UCSD],
technical/plos/journal.pbio.0020064.txt:        The bitter receptors fell first to 
the onslaught of the UCSD–NIDCR team and other
technical/plos/journal.pbio.0020064.txt:        UCSD–NIDCR researchers used the draft of the human genome to search for sequences that
technical/plos/journal.pbio.0020064.txt:        T1R3, a third member of the T1R family. The UCSD–NIDCR team subsequently showed that the
technical/plos/journal.pbio.0020064.txt:        knockout mice behaved differently, 
but the UCSD–NIDCR researchers suggest that the residual
technical/plos/journal.pbio.0020064.txt:        the UCSD–NIDCR researchers took PLCβ2 knockout mice, which did not respond to bitter,
```

* I find all words includ "ucsd" but all words are "UCSD" instead of "ucsd"

## The 'grep' command: Option -b

* Display the block number at the beginning of each line.
useful : -B is the option which prints the specified N lines before the match. When doing a grep on a huge file, it may be useful to see some lines after the match.
Example "ucsd"

```
[cs15lfa22lp@ieng6-201]:skill-demo1:178$ grep -b "ucsd" technical/*/*.txt
technical/biomed/1471-2121-2-22.txt:9834:        http://ncmir.ucsd.edu/~perkins/tBid. For example, it became
technical/biomed/1471-2164-3-18.txt:39199:          http://genome.ucsd.edu/index.html [ 54 55 ] . The
```

* 9834 and 39199 is the block number at the beginning of each line.

Example "Korea"

```
[cs15lfa22lp@ieng6-201]:skill-demo1:179$ grep -e "ucsd" technical/*/*.txt
technical/biomed/1471-2121-2-22.txt:        http://ncmir.ucsd.edu/~perkins/tBid. For example, it became
technical/biomed/1471-2164-3-18.txt:          http://genome.ucsd.edu/index.html [ 54 55 ] . The
[cs15lfa22lp@ieng6-201]:skill-demo1:180$ grep -b "Korea" technical/*/*.txt
technical/911report/chapter-11.txt:1935:                in Korea another. But these were attacks by major powers. While by no means as
technical/911report/chapter-11.txt:25557:                the main focus (war in Korea), and as too unrealistic. As we pointed out in chapter
technical/911report/chapter-12.txt:1058:                not experienced such a rapid surge in national security spending since the Korean
technical/911report/chapter-13.4.txt:34919:                Khallad, Aug. 13, 2003; 
Apr. 5, 2004. According to Khallad, Thailand, South Korea,
technical/911report/chapter-5.txt:37844:                Singapore, or Korea.) This 
part of the operation has been confirmed by Khallad, who
technical/911report/chapter-5.txt:38038:                Thailand, South Korea, Hong Kong, or Malaysia, and using Yemenis who would not need
technical/911report/chapter-6.txt:90375:                emphasized other issues such as North Korea and the Israeli- Palestinian peace
technical/911report/chapter-6.txt:91620:                with the faltering Middle East peace process and North Korea. Clarke said that the
technical/biomed/1471-2148-2-17.txt:20077:          Korea, and was previously considered a species of subg.
technical/biomed/1471-2148-2-17.txt:32471:          Europe and the Far East in Manchuria, Korea, and Japan.
technical/biomed/1471-2156-3-11.txt:19259:          from SeeGene (Seoul, Korea). The
technical/biomed/1472-6823-2-2.txt:4333:          Jolla, CA; Sofia, Bulgaria; Seoul, South Korea and São
technical/biomed/1472-6823-2-2.txt:8156:          Brazil; The Catholic University of Korea, Seoul, South
technical/biomed/1472-6823-2-2.txt:8221:          Korea). No information that would identify the subjects
technical/biomed/1472-6920-2-3.txt:415:        South Korea [ 5 ] and for a Turkish 
medical school [ 6 ] .
technical/plos/journal.pbio.0020121.txt:3632:        imported cases in the Republic of Korea, but surveillance has not been thorough in North
```
* The numbers are is the block number.

Example "fbi"

```
[cs15lfa22lp@ieng6-201]:skill-demo1:181$ grep -b "fbi" technical/*/*.txt
technical/911report/chapter-13.3.txt:42519:                FBI" (online at www.fbi.gov/libref/historic/history/historymain.htm); the FBI's
technical/911report/chapter-13.3.txt:42711:                updated June 18, 2003 (online at www.fas.org/irp/agency/doj/fbi/fbi_hist.htm). For
technical/biomed/1471-2121-2-12.txt:1488:        p14 Arfgene [ 2]. p14 Arfbinds to 
and sequesters mdm2,
technical/biomed/1471-2164-4-6.txt:22248:        http://www.cstl.nist.gov/biotech/strbase/fbicore.htm.
```
* The nmbers are also the block number such as 42519,42711,1488, and 22248

## The 'grep' command: Option -w

* Display matching whole word.
* useful : searching for whole word, so we can find only typing word will show out all the lines eventhought the word is normal.

Example "fbi"

```
[cs15lfa22lp@ieng6-201]:skill-demo1:183$ grep -w "fbi" technical/*/*.txt
technical/911report/chapter-13.3.txt:                FBI" (online at www.fbi.gov/libref/historic/history/historymain.htm); the FBI's
technical/911report/chapter-13.3.txt:                updated June 18, 2003 (online 
at www.fas.org/irp/agency/doj/fbi/fbi_hist.htm). For
```

* Display "fbi" and "FBI" whole word.

Example "Korea"

```
[cs15lfa22lp@ieng6-201]:skill-demo1:185$ grep -w "Korea" technical/*/*.txt
technical/911report/chapter-11.txt:                in Korea another. But these were attacks by major powers. While by no means as
technical/911report/chapter-11.txt:                the main focus (war in Korea), and as too unrealistic. As we pointed out in chapter
technical/911report/chapter-13.4.txt:                Khallad, Aug. 13, 2003; Apr. 5, 2004. According to Khallad, Thailand, South Korea,
technical/911report/chapter-5.txt:                Singapore, or Korea.) This part of the operation has been confirmed by Khallad, who
technical/911report/chapter-5.txt:                Thailand, South Korea, Hong Kong, or Malaysia, and using Yemenis who would not need
technical/911report/chapter-6.txt:                emphasized other issues such as North Korea and the Israeli- Palestinian peace
technical/911report/chapter-6.txt:                with the faltering Middle East peace process and North Korea. Clarke said that the
technical/biomed/1471-2148-2-17.txt:          Korea, and was previously considered 
a species of subg.
technical/biomed/1471-2148-2-17.txt:          Europe and the Far East in Manchuria, Korea, and Japan.
technical/biomed/1471-2156-3-11.txt:          from SeeGene (Seoul, Korea). The     
technical/biomed/1472-6823-2-2.txt:          Jolla, CA; Sofia, Bulgaria; Seoul, South Korea and São
technical/biomed/1472-6823-2-2.txt:          Brazil; The Catholic University of Korea, Seoul, South
technical/biomed/1472-6823-2-2.txt:          Korea). No information that would identify the subjects
technical/biomed/1472-6920-2-3.txt:        South Korea [ 5 ] and for a Turkish medical school [ 6 ] .
technical/plos/journal.pbio.0020121.txt:        imported cases in the Republic of Korea, but surveillance has not been thorough in North
```

* Display  "Korea" and "Korea" whole word.

Example "UCSD"

```
[cs15lfa22lp@ieng6-201]:skill-demo1:186$ grep -w "UCSD" technical/*/*.txt
technical/biomed/1471-2091-3-30.txt:        Insel, UCSD) demonstrated constitutive 
activation of ERKs
technical/biomed/1471-2407-2-15.txt:          UCSD Viral Vector Core. The plasmids 
were co-transfected
technical/biomed/1471-2407-2-15.txt:          approved by the animal care committee at UCSD. The cells
technical/biomed/1471-244X-3-5.txt:          UCSD Medical Center, La Jolla, during 
July and August of
technical/biomed/1472-6823-2-2.txt:          respective local human IRBs (UCSD, La 
Jolla, CA; Veterans
technical/biomed/1476-4598-2-2.txt:          Ludwig Institute of Cancer Research at UCSD. The tumor
technical/biomed/bcr620.txt:          UCSD Medical Center. Samples were obtained in random
technical/biomed/bcr620.txt:          approval of the UCSD Institutional Review Board for
technical/plos/journal.pbio.0020064.txt:        field, including collaborators Charles Zuker (University of California, San Diego [UCSD],
technical/plos/journal.pbio.0020064.txt:        The bitter receptors fell first to 
the onslaught of the UCSD–NIDCR team and other
technical/plos/journal.pbio.0020064.txt:        UCSD–NIDCR researchers used the draft of the human genome to search for sequences that
technical/plos/journal.pbio.0020064.txt:        T1R3, a third member of the T1R family. The UCSD–NIDCR team subsequently showed that the
technical/plos/journal.pbio.0020064.txt:        knockout mice behaved differently, 
but the UCSD–NIDCR researchers suggest that the residual
technical/plos/journal.pbio.0020064.txt:        the UCSD–NIDCR researchers took PLCβ2 knockout mice, which did not respond to bitter,
```

*  display "UCSD" and "ucsd"
