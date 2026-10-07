# RFM Analysis
**For class BDA15 only.**
> PowerBI -> (Optional) Jupyter Notebook & Google AI Studio -> Github -> Google Colab
## Required Files:
- Download **VibeCodingMaterialsV01.zip** from Google Classroom
- Unzip and get the following files: **DimensionTable.xlsx** and **SalesRecordV05.csv**
## Use **PowerBI** to extract data from the files:
  1. Get Data, **DimensionTable.xlsx**, only keep table **dProduct**
  2. Get Data, **SalesRecordV05.csv**
  3. Merge Queries, merge **SalesRecordV05.csv** with **DimensionTable.xlsx** via **ProductKey**
  4. In **SalesRecordV05.csv**, calculate **Total Sales** with [dProduct.單價" * (1-"Discount) * "Unitsold]
  5. Reference **SalesRecordV05.csv** and **Date, InvoNum, CustomerKey, SalesNum**
  6. Export as **rfm_raw.csv**
## (Optional) Use **Jupyter** and **Google AI Studio** to produce RFM data code:
- View "rfm_code.ipynb" for code example
> Remember to change **Google AI Sutdio**'s ai model to **Gemini 3.5 Flash Lite**
## Upload Code to Github
- Create new repository
- Upload **rfm_code.ipynb**
## Use **Google Colab** to finish RFM anaylsis
- Upload Notbook via **Github*
- Ask **Colab Gemini** to produce the following steps:
1. Load rfm_data.csv.
2. Perform normalization on df and name it nrfm.
3. Plot an Elbow Chart according to nrfm, help determine optimal number of clusters for running K-means.
4. Perform K-means clustering using nrfm, with 4 clusters.
5. Add the "Cluster" label back to the original data set df.
6. Create a Pair Plot using the R,F,M column from df data, group the data by Cluster label.
7. Add a new column to df with the header Group, where the values correspond to Cluster: 0>Missing, 1>High, 2>Low, 3>Medium.
8. Plot the R,F,M values from the df dataset as a pairwise scatter plot, grouped by the Group label.
9. Download this image as a transparent background image with the filename "rfm_pairplot.png".
10. Download the df in CSV format and save it as "rfm_result.csv".
## Import code back to Jupyter for local data usage
- As title
