# Canada Federal Election Widget - Web

Can be connected directly to an S3 bucket. 

Data is organized by year. Requires 4 files to work per year: 

1.  "electionconfig.json" - Includes title, seat total, and majority total variables. Additional variables can be added as needed. 
2.  "partyResults.json" - Overall party results via the "api/party/result/overall/(mains)/json" flow endpoint
3.  "overallResults.json" - Declarations results via the "api/OverallResult/?format=json" flow endpoint
4.  "ridingResults.json" - Riding/Candidate results via the "api/CandidateByRiding/?json=true" flow endpoint

Set up a new year of data: 
- Create a directory in data folder for the desired year. 
- add the required files as stated above
- navigate to the new year by changing the year in the endpoint of the widget to the desired year:
  eg. https://domain.com/#/map/year goes here>
