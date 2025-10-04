# data-5000-project

I tried using the CKAN datastore api (which powers Open Canada) to automate downloading all the data, but it doesn't work. There's a known issue where not all the datasets we need are in CKAN's queryable Datastore, so it's easier to just manually download everything ourselves:

https://open.canada.ca/data/en/dataset/1eb9eba7-71d1-4b30-9fb1-30cbdab7e63a

I downloaded all the English datasets from 2005 to 2020, since using more data makes my computer explode. Move the files into the data/raw folder (create it if it doesn't already exist), then click "Run All" in `combine-data.ipynb` to generate the combined data. This is annoying but we'll only have to do this once.
