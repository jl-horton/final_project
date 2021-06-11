# final_project

Using a dataset from NYC, which contains information about workers compensation claims, I will be using various characteristics of claims to detail causes of injury, location of injury on the body, and potential cost to the fund for reimbursement of wages and liklihood of a claim going to arbitration.  

Dataset was sourced from https://www.kaggle.com/new-york-state/nys-assembled-workers'-compensation-claims?select=assembled-workers-compensation-claims-beginning-2000.csv![image](https://user-images.githubusercontent.com/74440463/121650400-1e92ac00-cacc-11eb-9a37-f60181bcab34.png) and details claims assembled by NYC. These claims had various outcomes ranging from no compensation to death and a small amount of financial data relating to the weekly salary of the worker the claim relates to. It had been my hope that information in the dataset could be used to determine the financial outcome of a claim. There was not enough financial data to enable this, and I instead chose to select three criteria realting to an accident or disease that would help determine the catagory outcome of the claim. This may be an indicator of the cost of a claim. 

The dataset required more ETL than anticipated, and it was adjusted several times during the exploration to achieve the required data types. This included the removal from a number of columns of '*'.

Exploration was performed using Pandas and Matplotlib on the claims incident date between years 2015 - 2020. Analysis of the time taken to assemble a claim from the accident or disease incident date showed that there were shorter times for accidents than for disease. There was an accident claim that was around 11 years from the date of the accident to the date of assembly. It's difficult to determine if this is an outlier or a genuine data point that should be included. Without the certainty I left it in my dataframe. Most accident claims were assembled within two years of an incident occurring. Occupational disease has a different profile. It tends to take longer for a disease to be diagnosed and/or reported and it is more likely to be assembled later. 

I tried to store this in a SQLite database in order to run a flask app at deployment. I was anable to use this to create a flask app and will ran out of time to look at other storage solutions. 

While I had planned a more interactive website, I designed a fairly simple one that shows the graphics. I intend to continue to work on this and the database issue so that the page is interactive. 

Heroku was chosen for deployment but without the working Flask, this currently doesn't run. 
