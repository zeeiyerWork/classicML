This is a readme file for the data analysis of a vehicles.csv (a data set of used vehicle attributes and their associate price across states in the US). Analysis uses various python libraries - Pandas, Seaborn, Matplotlib, scikit-learn etc. The goal is to understand how prices relate to what features - and if all ducks line up in a row, then use the model to predict future car prices based on attributes. 
**
As a start (note the heavy use of functions with parametrization so one can experiment a bit with simple code changes - i.e. function parameters)
- The notebook is at VehicleDataModule11_final.ipnyb.ipnyb 
- It features several functions to EXPLORE the DATA
  -- dataframe_basicExploration (df.info(), df.describe(), Count of Nulls/column, Histograms where appropriate to understand how the values distribute across the data set, Corr matrix)
  -- dataframe_specificExploration (based on above, exploration specific to this dataset - i.e. logs of values etc.)
- It features functions (common) to MANIPULATE/CLEANSE the DATA
  -- dropping null columns, columns with high cardinality and columns with single values,
  -- using more than a SimpleImputer to a more sophisticated impute function
  -- removing rank outliers (i.e. row based cleansing)
- the final Block is to
  -- create a Preprocessor (StandardScaler for Numerical and OneHotEncoding for Categorical)
  -- Trying different pipelines/models (Linear Reg of Degree=1, Lasso Constraints, XGBoost and RandomForestRegression)
  -- Using the function evaluate_Model to compare the various outcomes.
**
More could be done in terms of trying
- Data acquisition and cleansing (which is to be handled before the data is presented to the Datascience team) - lots of important features have nulls (e.g vehicle condition, size), lots of features we know from common knowledge as important are missing too (e.g. accident history, internal systems status (A/C, Entertainment systems etc.))
- Of course, more could be done with the existing data to explore more data manipulation and other models - so we predict price better, but the above data issues cannot be de-emphasized since Garbage-in-Garbage-out.
- **Needed files**
- NOTES: README.md
- CODE: VehicleDataModule11_final.ipnyb(has suitable notes for additional guidance)
- DATA: vehicles.csv (needs to be relocated in the right place to ensure that you do not encounter "file-not-found" errors - in the data directory, but the notebook uses a HTTP url to acccess it)
