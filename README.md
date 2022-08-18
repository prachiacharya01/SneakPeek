# Recommendation Engine

Two dataset are used named venues_df contains--"spotid", "spotname"	geo-coordinates and spot_df contains-- "userid", "timestamp", "latitude", "longitude", "spotid", "eventType".

Dataset named "spot_df" contains combined feedback(implicit + explicit) from users, found under column named "eventType", which we utilized for making matrix.

Furthermore, both datasets are merged on spotid which is named as "merged_df" and feature engineering is performend on it and importantly we have given numeric strength to "eventType" and added column to "merged_df" as "eventStrength".

##  Matrix Generation
Matrices, generated are hybrid in nature that are created referencing to the "eventStrength".

##   Model
For weighting the AlternatingLeastSquares(ALS) model, sparse matrix "sparse_spot_person" is fitted in it.



##  Function of recommendation
From "sparse_person_content" matrix, firstly dimension are reduced by featuring particular person responses and there non visited places are marked to one and will be taken into consideration.

However, the resulted matrix is multiplied with content_vecs and the respective vectors are scaled to 0-1 and finally, output is stored in recommend_vector.

##  Ploting points on map
![newplot](https://user-images.githubusercontent.com/100126742/185418355-ad5fdc8b-d50f-476e-9451-b5088428156c.png)


