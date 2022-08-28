Automated Audit of The Colorado Congressional Presinct Election by Python

Overview: 
An election for US Congress was held in Colorado, USA. We are conducting an audit to verify the total number of votes, the number of votes per candidate, the percentage of total votes per candidate, the number of votes submitted per county, the percentage of total votes per county, and the winner of the election.  The purpose of this program is to pilot an automated auditing system that, if successful, will be used to audit other congressional districts, senatorial districts, and local elections.  The program will take raw data on election results from mail in ballots, machine counted ballots, and DRE machine votes summarized into a CSV table; then it will analyze the election results and generate a vote count report in a text file.

Election Analysis Process and Outcome:

  * Count of Votes Cast
      
       The total number of votes was found by pulling the data via python using os.path.join, setting the total_votes counter to 0 and counting through each row of the raw data for each vote.  The total number of votes was found to be 369,711.


  * Count of Votes per Candidate

      The total number of votes for each candidate was pulled and stored in a dictionary. A FOR loop ran through each row with a conditional statement that determined if the candidate's name was stored in the third column of the CSV was in the dictionary.  If it was not, the candidate's name was added as a key to the dictionary and a vote was added as a value making a key value pair. If the candidates name was in the library, a vote was added to the value stored under the key. Charles Casper Stockham obtained 85,213 votes, Diana DeGette obtained 272,892 votes, and Raymon Anthony Doane obtained 11,606 votes.

      
  * Percentage of Total Votes per Candidate
      
      The total number of votes for each candidate was converted into a percentage by dividing a count of votes obtained by the candidates by a count of all votes cast. Charles Casper Stockham obtained 23.0% of votes, Diana DeGette obtained 73.8% of votes, and Raymon Anthony Doane obtained   3.1% of votes

      
  * Count of Votes per County

     The total number of votes by each county was determiend the same way as the total number of votes for each candidate but under a different variable.  38,855 votes came from Jefferson, 306,055 votes came from Denver, and 24,801 votes came from Arapahoe.
    

  * Percentage of Total Votes per County
    
      The votes from each county was converted into a percentage the same way as the votes for each candidate under a different variable. 82.8% of votes came from Denver, 10.5% of votes came from Jefferson, and 6.7% of votes came from Arapahoe.
      
      
  * Election Winner 

      The winner of the election was determined by calculating who had the most votes and the largest percentage of votes. If a single candidate commanded the most votes and the majority percentage, they were declared the winner.  This ensures that the analysis was conducted correctly.  If no candidate satisfied the condition, no candidate would be declared the winner. The winner of the election was determined to be Diana DeGette with 272,892 total votes, and 73.8% of all votes.
      
      
  * Generating text report of data

      The data generated from the terminal was also used to generate a text file. Variables were used to store the analysis summary of each part of the election. See the text file for results.
