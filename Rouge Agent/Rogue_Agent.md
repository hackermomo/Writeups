# Rogue Agent

![image1.jpeg](Rogue%20Agent%200619eca9b80a4d43a7d9f1bfca3662da/image1.jpeg)

**Contract Link-**

[https://hacktoria.com/contracts/rogue-agent/](https://hacktoria.com/contracts/rogue-agent/)

**Contract Brief –** 

---

*Greetings Special Agent K. We have a request on our hands from our friends over at the CIA. In September of 2021, one of their operatives went missing in action. Upon further investigation, it was discovered this operative went rogue and started a smuggling business for the Russians. Mostly dealing in complex electronics, which have become difficult to come by for Russians after sanctions began.*

*The agent we’re looking for is named Valentino Maggi. Born in Brooklyn New York on 18.05.1987. Valentino is one of five sons of the Maggi family, who moved to the United States during World War II. Having grown up a middle class lifestyle, his father a car salesman and mother working as an elementary school teacher. Valentino was recruited into the CIA during his time as a student at Columbia University.*

*Most of his 10 years in active service were spent as an analyst working out of Langley. Recently though, in August of 2020, Valentino moved to oversees work. Being stationed in Italy as a liaison officer for the Italian foreign intelligence agency “Agenzia Informazioni e Sicurezza Esterna”.*

*Doing stellar work, right up until the point he went missing. Prompting an extensive investigation into his whereabouts. Documents were eventually found on his computer, recovered using forensics tools to recover deleted files. These indicate a heavy involvement with the Russian underground. Acquiring much needed microelectronics for the Russian government.*

*And that is where your task begins, Special Agent K. One of the files recovered from Valentino’s computer, is an image with a text file. We believe this to be the current location of Valentino Maggi. Locate the safehouse, so local authorities can raid the premises.*

*As always, Special Agent K. The contract is yours, if you choose to accept.*

---

**Link to Linkfile** - [https://hacktoria.com/wp-content/contracts/items/linkfile-rogue-agent.zip](https://hacktoria.com/wp-content/contracts/items/linkfile-rogue-agent.zip)  

**Link to image File** - [https://hacktoria.com/wp-content/contracts/items/safehouse-aerial-rogue-agent.jpg](https://hacktoria.com/wp-content/contracts/items/safehouse-aerial-rogue-agent.jpg)

**HOW I SOLVED IT:**

1. Reading the brief for clues about the probably location, really could not find any link.
2. Reverse analyze the image in Google lens and yandex didn’t really help solve. However, it looked like an image taken from satellite pro.
3. Started to follow this blog post - https://infosecwriteups.com/beginners-ctf-guide-finding-hidden-data-in-images-e3be9e34ae0d
4. Ran basic exif, stegsolve to find some clue, but all failed.
5. However when I ran xxd and strings filename. I saw a bunch of characters at the end which were clubbed together. Rest all seemed to be separated by ‘.’
    
    ![image2.png](Rogue%20Agent%200619eca9b80a4d43a7d9f1bfca3662da/image2.png)
    
    ![image3.png](Rogue%20Agent%200619eca9b80a4d43a7d9f1bfca3662da/image3.png)
    
6. Next step was to try to see if this string carry some meaning. So I ran magic on cyberchef. And Volla!! Found the coordinates in rotate right.
    
    → 44.259654-21.057843
    
    ![image4.png](Rogue%20Agent%200619eca9b80a4d43a7d9f1bfca3662da/image4.png)
    
7. This location goes to Rakinac, Serbia. So password should be –

**serbia-rakinac-44.259654-21.057843**

And Fin.

![image5.png](Rogue%20Agent%200619eca9b80a4d43a7d9f1bfca3662da/image5.png)
