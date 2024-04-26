Slide By Slide Documentation
Written By: Madeline Blackwell, Ryan Burchette, Nick Hudler and Kamron Sigmon


* Slide 1
   * Title Page


* Slide 2
   * This slide discusses the objectives of our project.
      * The first objective is to understand encryption algorithms through experimentation and how decryption tools can crack it. The tool we used for this objective is Cryptool which is a 2in1 encryption and decryption algorithm that will take a plain text and turn it into a cipher text and vice versa.
      * The second objective is to learn how to use debuggers in order to understand the assembly code of malware. The tool we used for this objective is x64dbg.
      * The third and final objective is to successfully identify and confirm packed malware. The tool we will be using for this is PEiD.


* Slide 3
   * Subtitle page to begin the first objective


* Slide 4
   * Rijndael, or Advanced Encryption Standard (AES), is a form of symmetric encryption that uses fixed length blocks of data and various key lengths, combined with repeated mathematical algorithms to transform the data. The data undergoes various stages of substitution and permutation to ensure it is near impossible to decrypt the data without the appropriate key. They tool of choice to demonstrate this encryption algorithm is Cryptool. Cryptool is an open-source software that shows the different steps of an encryption algorithm using its GUI. This can be very beneficial in an educational environment to learn how each step transforms the data.




* Slide 5
   *           
   * This slide explains the start of the encryption process in Cryptool
   * When you first open Cryptool in the center there is a blank text box where the plaintext or ciphertext is supposed to go and several options along the top. 
   * For the plain text we went with a snippet from the bee movie script as that was recognizable and would be clear if the deciphering did or did not go well.
   * You can go to the top and select encryption and when you do it will ask what type of encryption algorithm you want to use. We went with the AES (advanced encryption standard) algorithm since we learned about this one in class. For this algorithm we need a 128 bit key length which will be used in the algorithm to encrypt the message. In the next slide what key we did is explained more


   * Slide 6
   *      * In this slide we show the key that we went with to do encryption with.
      * The use of the key in encryption is to be used in mathematical problems with text to create the encrypted message. 
      * For the sake of simplicity and ease we went with a basic key of:
      * 00 01 02 03 04 05 06 07 08 90 0A 0B 0C 0D 0E 0F
      * This key is in the form of hexadecimal
















      * Slide 7
      *         * In this slide we show the output of Cryptool when you encrypt a message
         * The output is split into 3 sections
         * The first section is a numbering of the characters in that row
         * The second section is the output of the encrypted message in the form of hexadecimal
         * The third section is the output of the encrypted message in the form of ASCII which would be the form a user would see if they tried to view the message without decrypting it.
         * In the ASCII it may be noticed that there are many periods through the message, this just means that in that spot there is no ASCII value that would match the equivalent hexadecimal value.
         * In the next slide we show more of the equivalency




         * Slide 8
         *            * In this slide we show the equivalency of the hexadecimal and ASCII
            * In Cryptool when you get an output you have the ability to right click highlight a section of either the hexadecimal or ASCII and it will automatically highlight in the section you didn't select, the value that matches up with your selected section.


            * Slide 9
            *               * In this slide we show the beginning of the decryption process in Cryptool
               * When you select decryption for the output Cryptool gives you get a popup box asking for the key used for decryption.This is because Cryptool uses brute force technique to attempt to crack the message. 
               * You can run the analysis without using the key but the more of the correct key you give the faster the runtime will be


               * Slide 10
               *                  *                  * In this slide we show running the brute force attack without any part of the key inputted
                  * When you attempt to brute force an AES encrypted message without knowing any part of the key it would take impossible long which you can see in the first image.
                  * The output given when we stopped the attempt earlier is show
                  * Each line of the output is each attempt it made while running the brute force analysis
                  * On each line there is the entropy of the attempt, the hex output, the ASCII decryption out, and the key it attempted to decrypt the message with


                  * Slide 11
                  *                     *                     * This slide is similar to the previous one but we inputted half of the correct key before running the attempt
                     * In the output you can see that the estimated time is slightly shorter but still would take around 85000 year to crack the ciphertext.
                     * The results are slightly better though if you look int he ASCII section. It has more actual characters and less periods compared to the previous attempt


                     * Slide 12
                     *                        *                        * This slide shows what happens when you run the brute force with ⅔ of the key given
                        * With ⅔ of the key given to the brute force attempt, it can potentially crack it in 2 hours.
                        * This clearly shows the more of the key given the faster it is as cracking the cipher text.


                        * Slide 13
                        *                           *                           * Finally in this slide we show the completed ciphertext
                           * In order to get it to crack we gave it the full correct key and it cracked it within milliseconds.
                           * In the results box you can see that only one result is displayed and it contains the correct key and decryption
                           * Just to be sure we pulled up the full results and it can be see that the output is the same at the original plaintext we put in.


                           * Slide 14
                           * Subtitle page to begin the second objective of successfully identifying and confirming packed malware using PEiD


                           * Slide 15
                           * PEiD is a scanner to check for packed files. Packed files means to compress the files in a way that will help avoid detections by antiviruses. It does this through changing the types of signatures like hashes. The PEiD can check for over 470 different signatures in PE files.
                           * Tools:
                           * PEiD
                           * Github of packed files






                           * Slide 16
                           *                              * In this section of the slides we looked at the tool PEid
                           * The image provided is the result of when you select a file, specifically an .EXE file that you want to check for packing
                           * As you can see there are many points of information and additional options in the next couple slides we will discuss the more important of them


                              * Slide 17
                              *   

                                 * In this slide we discuss the confirmation of the packer
                                 * In the given image and highlighted area you can see that it is confirmed that the file that was selected is packed as PEid gave a result instead of leaving it blank
                                 * The packed thing it found was EXE32Pack 1.3x


                                 * Slide 18
                                 *                                    * In this slide we show how to unpack a file once a file has given confirmation a packer was used
                                 * In the image above it is showing that you can select a plugin for PEid of which can be unpacker
                                 * PEid comes with a generic unpacker that will derive the desired true .exe file potentially
                                 * You can also often find the correct unpacker for each unpacker that is made


                                    * Slide 19
                                    *                                       *                                       * In this slide we show one of the other interesting options that you can select in PEid which is the First Bytes section
                                    * In the box is shows as the name suggests the first Bytes of the selected file
                                    * If you select the over arrow though you will get the information shown in the second image
                                    * This information is about the assembly code, bytes, and addresses of the of the selected file


                                       *  Slide 20
                                       * Subtitle page to begin the final objective of using debuggers and understanding the assembly code of malware


                                       * Slide 21
                                       * In this slide we present the background knowledge that describes what we are trying to accomplish, why, and what means we are going to use to achieve the goal.
                                       * The topic being discussed will be what assembly code is and how at that level of abstraction, it can be difficult to determine the intentions of a program. Therefore presenting the need for a tool to analyze assembly code for malicious patterns found in malware.
                                       * The tool being used will be x64dbg.


                                       * Slide 22
                                       *                                          *                                          * In this slide we present the example code that we will be using for the following steps on how to analyze the code using x64dbg.
                                       * The code does not actually contain malware, rather is a snippet of sample C++ code with multiple function calls, giving us points of interest when analyzing the assembly code using the tool.


                                          * Slide 23
                                          * This slide is where we discuss how to begin using the tool, starting off with loading the file and which section of the tool is important to viewing the appropriate assembly coe.


                                          * Slide 24
                                          *                                             * In this slide, we discuss the usage of breakpoints in the tool. Breakpoints are an important tool in x64dbg so that you can mark the points of interest so that you can slowly progress through the program’s execution one step at a time. This allows us to view all of the address space changes during each step, which could help in discovering if the program is accessing sensitive address spaces.


                                             * Slide 25
                                             * This slide shows each of the breakpoints that will be used in our example program, one at each of the important function calls (main, printf, getchar).


                                             * Slide 26
                                             *                                                *                                                * In this slide, we discuss the process of using the debugging feature of the x64dbg tool. Similar to something like Visual Studio, you are able to step over and step into various function calls that are made throughout the program. This is useful in tracking the exact resources being used by the program.
                                             * The program will run until it hits our first designated breakpoint, meaning we skip the assembly code that is irrelevant to the actual main function call of the program.


                                                * Slide 27
                                                *                                                   * This slide discusses the observations that are able to be made through the memory map window of the x64dbg tool. This window gives us information on the memory addresses, size, and information in the address for all of the address spaces referenced in the program.


                                                   * Slide 28
                                                   *                                                      * This slide discusses the usage of the program logs window. This window simplifies the information related to the calls in the program and produces a message that we can read to better understand what has happened when an error occurs or when points of interest are reached in the execution process.


                                                      * Slide 29
                                                      * Summary title page


                                                      * Slide 30
                                                      * First we showed the use of the tool Cryptool
                                                      * We demonstrated encrypting and decrypting and the strength of the AES algorithm
                                                      * This showed one way that file can be kept safe but also a way malware can be hidden
                                                      * Next we used the PEid
                                                      * We demonstrated how to confirm a packed file using the PEid tool
                                                      * This again showed another way that malware can be hidden within files
                                                      * After we know how malware is hidden we looked at the assembly code
                                                      * We demonstrated how to run through the execution of a program and tracking the changes in its address space.
                                                      * This tool makes analyzing the address space changes and various functions of an executable a simple task.


                                                      * Slide 31
                                                      * Title page for references


                                                      * Slide 32
                                                      * PEiD Tutorial
                                                      * PEiD Info
                                                      * Cryptool Demo
                                                      * Cryptool Documentation
                                                      * x64dbg Tutorial
                                                      * x64dbg Documentation