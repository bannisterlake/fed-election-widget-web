# Canada Federal Election Widget - Web

Can be connected directly to an S3 bucket. 

How to Navigate: 
App uses URL endpoints to navigate between election widgets: 
Layout: 
  https://domain.com/path/to/widget/#/widget_type/year/riding
 
The riding (not case sensitive) is only used in map widget to zoom in on specific ridings on widget load. 

Data is organized by year. Requires 4 files to work per year: 

1.  "electionconfig.json" - Includes title, seat total, majority total and data refresh timer variables. Additional variables can be added as needed. 
2.  "partyResults.json" - Overall party results via the "api/party/result/overall/(mains)/json" flow endpoint
3.  "overallResults.json" - Declarations results via the "api/OverallResult/?format=json" flow endpoint
4.  "ridingResults.json" - Riding/Candidate results via the "api/CandidateByRiding/?json=true" flow endpoint

Filtered Results (NEW!): 
-within each year directory, add a directory named "filtered". 
-updated electionconfig.json with filter label, query url (that is pushed via BladeRunner. This URL is not actually used by widget, there for organization only) and filename to be stored in the filtered directory.
-add as many filters as needed by adding a new object to the filtered results array. 

Set up a new year of data: 
- Create a directory in data folder for the desired year. 
- add the required files as stated above
- navigate to the new year by changing the year in the endpoint of the widget to the desired year:
  eg. https://domain.com/#/map/year goes here>
