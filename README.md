# Workflow

## Step 1: Data extraction using Google Earth Engine (GEE)

The data extraction is performed using a script written in Google Earth Engine.

1. Open the following link in a web browser:  
   https://code.earthengine.google.com/c2a490d827f13217b3cc88ca2c7a0b3b

2. Click Run to execute the script.

3. After execution, open the Tasks tab.

4. Start the export task and download the generated CSV file to your local machine.
### Note on GEE memory issues  
Sometimes GEE code breaks because of memory limitations when processing multiple years.  
To avoid this, process one year at a time by changing this line in the script:

```javascript
var years = ee.List.sequence(2015, 2025); 
---
var years = ee.List.sequence(2015, 2015);

```

## Step 2: Python analysis in Jupyter Notebook / VS Code

The downloaded CSV file is used as input for the Python-based analysis.

### Install required dependencies

Install the required Python libraries based on the imports used in the notebook:


pip install pandas numpy matplotlib scikit-learn

## Step 3: Run the code

Now run the code
