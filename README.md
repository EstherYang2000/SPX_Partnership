# SPX_Partnership
Collaborated with Shopee Xpress Courier to solve the problem of potential partners' business locations by analyzing 400+ potential chain enterprise's location and feasibility using Python web crawler.
The project is designed into two stages, qualitative stage and quantitative stage.
## Qualitative Stage
<br>
The is our workflow of Qualitative Stage.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220517073-55584f69-3096-4345-a6c8-9394125ef4a3.png">
<br>
### 1. Select the possible Partnership from all the chains industries in Taiwan

According to the following standards, we filter out the part of possible of partners.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220516809-5833685a-5c2d-4924-826a-87b56aef8374.png">
### 2. Filter out the inappropriate partners
<br>
The below picture is our initial partnership that we need to use web craweler in Python to collect their basix shop's location, opening hours, and total numbers
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220514688-72352174-a36c-4467-a697-6a14c8656b93.png">
<br>
The above is thos partners deleted since they are not meet these business standards
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220515100-9d68e6f4-a823-4586-8104-e5c6cf91a424.png">
<br>
### 3. Calculate the qualitative score based on its weights
These are our dynamic weights of business standards that can be revised based on each condition or the clients' consideration.
<br>
<img width="937" alt="image" src="https://user-images.githubusercontent.com/80161804/220517413-b5930259-35b1-46a0-948f-42478edb60fe.png">
<br>
Then we calculate the score of each chain brand's qualitative score.
<br>
<img width="921" alt="image" src="https://user-images.githubusercontent.com/80161804/220530186-52650cc6-8534-4bce-8bd0-ab1559d1d4f3.png">
<br>
Then we calculate the score of each chain brand's qualitative score as Partnership's Score(PS).
<br>
One of the those business standards, the preferred channel of buyers, is defined by 300+ questionnaires responses.
The detailed information is wrriten in the [slide](https://github.com/EstherYang2000/SPX_Partnership/blob/main/Shopee%20x%20NTUDAC_%E5%B0%88%E6%A1%88%E7%B5%90%E6%A1%88%E5%A0%B1%E5%91%8A_G3%E7%B0%A1%E5%A0%B1%E6%AA%94.pdf)
<br>
## Quantitative Stage
<br>
The is our workflow of Quantitative Stage.
<img width="930" alt="image" src="https://user-images.githubusercontent.com/80161804/220531559-c20f80f2-7aed-4446-bd6f-886fdf23b351.png">
<br>
### 4. Label each district with 3D classification model
Here are the standards of shops' location. 
We also design "3D classification model" to label every district, including 金蝦,銀蝦 and 銅蝦.
"3D classification model" is related to a district's District,Density and Demand.
<img width="934" alt="image" src="https://user-images.githubusercontent.com/80161804/220531891-b30f643e-4377-4118-b268-073839e8ac06.png">
<br>
### 4. Calculate the quantitative score based on its weights
Weights of Location Score(LS) are definded by the 300+ questionnaires responses.
Then we calculate the score of each chain brand's qualitative score as Location Score(LS).
<img width="932" alt="image" src="https://user-images.githubusercontent.com/80161804/220534185-5ca54956-968f-41d0-8110-03aab0665d6e.png">
<br>
Finally, we use "3D classification model"  while combine the Partnership's Score(PS) and Location Score(LS) to chooes the optimal shop address.
使用 3D 分群法篩選區域，再結合潛在合作夥伴及評分機制選出最合適的店址
<br>
## Tableau
<br>
We design the two dashboards, respectively Partnerships and Location.
<br>
### 1. Partnership Dashboard
<br>
The partnership dashboard can be dynamically weighted and generate updated rankings based on the weighting results.
<br>
Partnerships will be divided into four groups base on its Partnership Score(PS), including 強烈開發 
<br>
<img width="921" alt="image" src="https://user-images.githubusercontent.com/80161804/220534690-164c298e-c073-4301-9aa0-ce9fbcea4ac9.png">
<bt>
