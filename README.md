# sqlalchemy-challenge

Student exercise using sqlalchemy to query a database and plot our findings.

Congratulations! You've decided to treat yourself to a long holiday vacation in Honolulu, Hawaii! To help with your trip planning, you need to do some climate analysis on the area. The following outlines what you need to do.

To begin, use Python and SQLAlchemy to do basic climate analysis and data exploration of your climate database. All of the following analysis should be completed using SQLAlchemy ORM queries, Pandas, and Matplotlib.

Precipitation Analysis:
    -Start by finding the most recent date in the data set.
    
    -Using this date, retrieve the last 12 months of precipitation data by querying the 12 preceding months of data. Note you do not pass in the date as a variable to your query.
    
    -Select only the date and prcp values.

    -Load the query results into a Pandas DataFrame and set the index to the date column.

    -Sort the DataFrame values by date.

    -Plot the results using the DataFrame plot method.

Station Analysis:
    -Design a query to calculate the total number of stations in the dataset.

    -Design a query to find the most active stations (i.e. which stations have the most rows?).

        -List the stations and observation counts in descending order.

        -Which station id has the highest number of observations?

        -Using the most active station id, calculate the lowest, highest, and average temperature.

    -Design a query to retrieve the last 12 months of temperature observation data (TOBS).

        -Filter by the station with the highest number of observations.

        -Query the last 12 months of temperature observation data for this station.

        -Plot the results as a histogram with bins=12.


Climate App:

Now that you have completed your initial analysis, design a Flask API based on the queries that you have just developed.

    Routes:
        /
           - Home page.
           - List all routes that are available.

        /api/v1.0/precipitation
           - Convert the query results to a dictionary using date as the key and prcp as the value.
           - Return the JSON representation of your dictionary.

        /api/v1.0/stations
           - Return a JSON list of stations from the dataset.

        /api/v1.0/tobs
           - Query the dates and temperature observations of the most active station for the last year of data.
           - Return a JSON list of temperature observations (TOBS) for the previous year.