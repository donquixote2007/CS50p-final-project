# CS50p-final-project
Final project for Harvard's CS50P Online Python class - submitted in Dec 2022 by Sneha Gorla (copied the files to a new public repository)


#DNA AND RNA Video: https://youtu.be/RqNiDshpPJ8 Description: A program that uses a fasta file to tell the user how many nucleotides and codons are in the sequence, translating the sequence into RNA then into a protein sequence, whether there are stop or start codons, and a fun game at the end. The fasta file was imported than read through a function which I created with file i/o. I then used a counter and the mod function to read how many nucleotides and there were by using mod 3 and getting the results. To find the start and stop codons, I used conditionals and variables to see whether there were any in the sequence. If there were no start or stop codons, I used a print statement to say that there weren't any. To translate the DNA into RNA I used replace to replace the T nucleotides with U nucleotides then split the sequence into codons and read them using a dictionary I created. Using the same dictionary, I was able to then turn the codons into a protein sequence. The game at the end was something that I wanted to do because I enjoyed creating games previously and wanted to make another one that was related to my topic.

In order to create my final project, my initial idea was to have the user input the sequence of DNA they wanted to be translated but I later realized that it is unrealistic to have someone type in a whole sequence considering some can be up to hundreds of characters long. I also didn't start creating my RNA to protein function until later on but I thought it would be interesting to create and be able to use a function that can take a section of the DNA sequence and turn that into a protein sequence. For this part I was thinking about using a pre-existing function that I had researched about but I decided that for this specific function, it would make more sense to just use a dictionary.

Starting off with the translate function, the purpose of this function was to take the file name from the input so I could use it later in the code. The input should be "python project.py sequence.fasta" so I used sys.argv to take the name in the index one which I used throughout the code assigning it to a variable and returning it to the main function.

After that I have the get DNA sequence function in which I took the variable created in the last function and opened the file. I put it in a different function because I thought it made the flow of the code make more sense. This also raises an error in case there is no argument after the project.py being called.

The start codon aug is assigned to a variable in the next function, find start, and I use a conditional to find whether there is a start codon in the sequence. This relates to the code later specifially when I turn the codons into a protein sequence.

For the stop codons, since there are 3 I had to create 3 different. variables and compare them to the code in the same way I did the last function. I had to rewrite the code 3 times though in order to check that there were or were not any stop codons. I decided to not use a loop because the stop codons kept changing so it would not make sense to use a loop in this scenario.

The num or nucleotides function is similar to problems from the past so I created a loop in which the program read through each character and added 1 to the counter for the nucleotide. This allows for an accurate count of each nucleotide without needing to do all the manual work that would be involved by counting each one manually.

The next function was relatively simple in order to translate the DNA to RNA. In order to do this, I used replace to replace all the T nucleotides with U and then printed the sequence out in the terminal.

Next was the sequence to protein function. This one did take more time and effort because I created a list then used the list to check whether there were start and stop codons then had to translate each codon into a protein. I created a while loop so it would loop through each time and added the new protein to a list then printed out the list. If there was no start or stop codon, this function printed that there wasn't letting the user know.

Last, I created a nucleotide game because I thought it was a fun way to end the project. I used regular expressions to match and see if the user wrote the correct answer then in the end, printed out however many they got right.
