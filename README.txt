1. tiki_crawl_links.ipynb -> link_group_product.txt
    Crawl all the links of 2nd-level group products on Tiki
    Ex: (lv1) Đồ Chơi - Mẹ & Bé -> (lv2) Tã, Bỉm

2. tiki_crawl_prod_id.ipynb -> prod_id.csv
    Crawl 25-page worth of product in each link (~160.000 ids)

3. tiki_crawl_prod_data.ipynb -> df_prod.csv (~13.000 ids)
    Crawl all the relevant data of each product_id
    It takes quite some time so only 13000 ids were crawled

4. eda.ipynb -> eda_cleaned.csv; store_data.csv
    Look how each category perform
    Segment sellers

5. LinearSVR.ipynb :
- Process: 
    + Natural Log transform (df+1): Log-transform to return non-negative values in the predicting model, '+1' since input matrix is highly sparse
    + Split: 15% for test
    + Hypertuning the parameters for LinearSVR (refer to sklearn doc) -> Choose the parameters that return lowest value of RMSE to fit again for the train dataset
    + With the fitted model, check performance by using predict on the test dataset
    + Concatenate two results from train and test to look at error distribution
- Target's distribution as follow:
count    13184.0
mean        41.0
std        118.0
mode         0.0
min          0.0
25%          0.0
50%          3.0
75%         23.0
max       1135.0
- Current performance:
RMSE Train:  0.8116
RMSE Test:  0.8056
79.26% to have a predicted value within error range [-10, 10]

    
