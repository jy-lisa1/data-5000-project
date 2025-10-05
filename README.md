# data-5000-project

I tried using the CKAN datastore api (which powers Open Canada) to automate downloading all the data, but it doesn't work. There's a known issue where not all the datasets we need are in CKAN's queryable Datastore, so we have to manually download everything ourselves:

https://open.canada.ca/data/en/dataset/1eb9eba7-71d1-4b30-9fb1-30cbdab7e63a

I used a subset of the available datasets, since using all the data makes my computer explode. Here's what I did to prepare the data for analysis (This is annoying but we'll only have to do this once).

1. Download all the English datasets from 2006 to 2020.
2. Move the files into the `./data/raw` folder (create it if it doesn't already exist).
3. Click "Run All" in `combine_data.ipynb` to generate the combined data.
4. Clean up the raw combined data by clicking "Run All" in `fix_dtypes.ipynb`.
5. There should now be a csv file called `cleaned_data.csv` in the data folder.
