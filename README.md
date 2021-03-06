# Summary
A collaborative Java web-app developed with eclipse that displays information on presidents of the United States based on user input.
![alt text](WebContent/presland.png "Landing Page")
## Instructions
1. User arrives on landing page.
2. User can select president based on term #, name or party.
3. Information is displayed on chosen president.
4. User can navigate forwards or backwards. When user gets to the end or the beginning, arrows will take them back to the other end.

## Class Structure Overview
- The **PresServlet** class is the controller and interacts with the **PresDAOImpl** class which implements methods declared in the **PresDAO** interface. The president object and list objects are constructed using information from the **President** class and accompanying .txt and .csv files.
- The **PresServlet** provides information back through a **.jsp** file for the user to view and chooses what president's information (name, term years, picture, facts, etc.) will be displayed based upon if-logic located in the servlet that evaluates user navigation in put.

## Example
```
@Override
	public List<President> getParty(String party) {
		List<President> presList = new ArrayList<>();
		for (President pres : presidents) {
			if (pres.getParty().equals(party)) {
				presList.add(pres);
			}
		}
		return presList;
	}
  ```
  
  ![alt text](WebContent/whig.png "Landing Page")
  #### Breakdown
Sorting the Presidents by party was done by iterating the list of Presidents with the for each loop. Once the list was iterated over we used the the President's Class party variable to match the party recieved through the argument. If both parties matched then the president was stored into the presList and displayed to the user.

## Reflection
This project was the first weekend project done with a team. As a collective we decided to only use one computer to push to the repository in order to avoid merge conflicts. Reflecting on our process it would have been more benificial to have run into some situations where we had to work around merge conflicts in order to get the practice on how to resolve them. 
