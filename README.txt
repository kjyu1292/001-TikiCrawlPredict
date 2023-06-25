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

5. LinearSVR.ipynb -> coef_
    