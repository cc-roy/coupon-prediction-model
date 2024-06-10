# coupon-prediction-model

<h3>Running data and analysis:</h3>

The data that powers our analysis is housed within a PostgreSQL database that can be hosted locally:
<ul>
  <li>The ‘marketing-data-raw.csv’ file located in the repo contains the raw data that powers the model.</li>
  <li>The ‘marketing-data-schema.sql’ file within the repo contains the SQL code needed to create a table within your PostgreSQL database to store the data.</li>
    <ul>
      <li>Within your PGAdmin interface, create a new database. Once the database is created, right click and open the query tool. Copy the contents of the 'marketing-data-schema.sql' file into the query tool and run the query to create a table within your database. By default, the table will be named 'marketing_data', but you can rename the table as you see fit.</li>
    </ul>
  <li>The ‘marketing-data-raw.csv’ file can be used to populate the table once it is created.</li>
    <ul>
      <li>Within your PGAdmin interface, right click on the table and click import/export data. Within the new dialogue box, select the 'marketing-data-raw.csv' file from your directory, select UTF8 as the encoding, and csv as the file format. Click accept and, if everything was processed correctly, you will receive a confirmation notification.</li>
      <li>If you encounter any upload issues, examine the 'marketing-data-schema.sql' table and the 'marketing-data-raw.csv' file to ensure all datatypes are aligned.</li>
    </ul>
  <li>Once the PostgreSQL database is configured, the primary ipynb file within the repo contains logic for reading the database via SQLAlchemy. Please note that you will need to update the 'db_uri' variable to align with your own instance of PostgreSQL, where the pattern should be 'postgresql://user_name:password@localhost:port_number/database_name'</li>
</ul>

<h3>Models explored:</h3>

<ul>
  <li>Random forest</li>
  <li>KNN</li>
  <li>Logistic regression</li>
  <li>Neural network</li>
</ul>

<h3>Findings and conclusion:</h3>

<ul>
  <li>Based on the supervised learning models tested for the sample marketing campaign data, the highest level of accuracy achieved was 87% from more than one model.</li>
  <li>This concludes that several models can achieve the optimal result, no one model is best fit.</li>
  <li>There were significant observable differences between precision, recall, and F1 throughout the various models, therefore, the business may want to consider the impact of these variations in accordance with their goals.</li>
</ul>
