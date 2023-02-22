# SPX_Partnership
Collaborated with Shopee Xpress Courier to solve the problem of potential partners' business locations by analyzing 400+ potential chain enterprise's location and feasibility using Python web crawler.
The project is designed into two stages, qualitative stage and quantitative stage.
<h2> Qualitative Stage</h2>
The is our workflow of Qualitative Stage.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220517073-55584f69-3096-4345-a6c8-9394125ef4a3.png">
<br>
<h3> 1. Select the possible Partnership from all the chains industries in Taiwan</h3> 
According to the following standards, we filter out the part of possible of partners.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220516809-5833685a-5c2d-4924-826a-87b56aef8374.png">
<h3> 2. Filter out the inappropriate partners</h3> 
The below picture is our initial partnership that we need to use web craweler in Python to collect their basix shop's location, opening hours, and total numbers
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220514688-72352174-a36c-4467-a697-6a14c8656b93.png">
<br>
The above is thos partners deleted since they are not meet these business standards
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220515100-9d68e6f4-a823-4586-8104-e5c6cf91a424.png">
<br>
<h3> 3. Calculate the qualitative score based on its weights</h3>
These are our dynamic weights of business standards that can be revised based on each condition or the clients' consideration.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220517413-b5930259-35b1-46a0-948f-42478edb60fe.png">
<br>
Then we calculate the score of each chain brand's qualitative score.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220530186-52650cc6-8534-4bce-8bd0-ab1559d1d4f3.png">
<br>
Then we calculate the score of each chain brand's qualitative score as Partnership's Score(PS).
<br>
One of the those business standards, the preferred channel of buyers, is defined by 300+ questionnaires responses.
The detailed information is wrriten in the <a href="https://github.com/EstherYang2000/SPX_Partnership/blob/main/Shopee%20x%20NTUDAC_%E5%B0%88%E6%A1%88%E7%B5%90%E6%A1%88%E5%A0%B1%E5%91%8A_G3%E7%B0%A1%E5%A0%B1%E6%AA%94.pdf">slide</a>
<br>
<h2> Quantitative Stage</h2>
The is our workflow of Quantitative Stage.
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220531559-c20f80f2-7aed-4446-bd6f-886fdf23b351.png">
<br>
<h3> 4. Label each district with 3D classification model</h3>
Here are the standards of shops' location. 
We also design "3D classification model" to label every district,which there are 27 sets, such as 111,123,123,233,323,322.
<br>
"3D classification model" is related to a district's District,Density and Demand.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220531891-b30f643e-4377-4118-b268-073839e8ac06.png">
<br>
<h3> 5. Calculate the quantitative score based on its weights</h3>
Weights of Location Score(LS) are definded by the 300+ questionnaires responses.
<br>
Then we calculate the score of each chain brand's qualitative score as Location Score(LS).
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220534185-5ca54956-968f-41d0-8110-03aab0665d6e.png">
<br>
Finally, we use "3D classification model"  while combine the Partnership's Score(PS) and Location Score(LS) to chooes the optimal shop address.
<br>
<h2> Tableau </h2> 
<a href="https://github.com/EstherYang2000/SPX_Partnership/tree/main/DashBoard/DashBoard%20%E6%AA%94%E6%A1%88">Tableau Link</a>
<br>
We design the two dashboards, respectively Partnerships and Location.
<br>
<h3> 1. Partnership Dashboard</h3>
The partnership dashboard can be dynamically weighted and generate updated rankings based on the weighting results.
<br>
Partnerships will be divided into four groups base on its Partnership Score(PS), including <b>強烈開發</b>,<b>推薦開發</b>,<b>普通推薦開發</b>,<b>暫緩開發</b> 
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220534690-164c298e-c073-4301-9aa0-ce9fbcea4ac9.png">
<br>
<h3> 2. Location Dashboard</h3>
Priority ranking in the Location dashboard through weighting and filtering
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220561481-81ac7442-ce67-4684-ad83-08c20af3308a.png">

<h2>Data Insight</h2>
The advantages of POYA, Da Shu(大樹) Pharmacy and Heng Yi（杏一） Pharmacy are their wide shop coverage and large number of shops, while the advantages of Xiao Bei（小北)Department Store are long business hours.
<br>
We realize that pharmacy is the best channel for cooperation because of its wide shop coverage and large number of shops.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220564088-bc8aafa6-fd28-41d8-91da-efb643a01c9a.png">
<br>
The area was divided into gold shrimp(金蝦), silver shrimp(銀蝦) and bronze shrimp(銅蝦) areas based on the amount of CVS contained within 1300 m of each location and the average distance to the nearest SPX.
Gold, Silver and Bronze shrimp areas are correspondingly placed into  areas labeled with "3D classification model".
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220564316-7a2d0b7f-b1cb-4f8e-a1f8-a65f5f3993d8.png">
<br>

<h2> Code Explanation </h2>
Use Python, Google API, Government Website to script in  <a href="https://github.com/EstherYang2000/SPX_Partnership/blob/main/FinalCode.ipynb">Final Code</a>
<h3>Step 1. Web Crawler</h3>
<code>def crawlerStore() </code> is a function to collect the shop stores' info from the official website with web crawler.
<br>
The example is Poya's API.
<br>
<h3>Step 2. Use Government Website to label shops' location</h3>
<code>def findFullAddress(dataFrame: Iterable,cAddress: str,token: str,cookie: str,startNode: int,endNode: int) -> Iterable: </code>
<br>
Input the DataFrame, which the place you want to find the complete address
<br>
<ol>
<li>startNode: the index you want to start searching</li>
<li>endNode: the index you want to stop searching</li>
</ol>
<code>def judgeFloor(r)</code> is a function to extract the floor info from the address.
<code>def solveReplaceDistrict(dfPTStore: Iterable) -> Iterable:</code> is to narrow down the district labels into three types of labels, including <b>商業區</b>,<b>住宅區</b> and <b>其他區</b>.

<h3>Step 3. Calculate TripDensity</h3>
<code>def TripDensity(df1, city: str, district: str, afternoon_work: str, df2,city_district: str, area: str) -> Iterable:</code>
The above function is to calculate TripDensity column
<h3>Step 4. Calculate PopulationDensity</h3>
<code>def PopulationDensity(df: Iterable, city_district: str, population_density: str) -> Iterable:</code>
<br>
The above function is to calculate PopulationDensity column
<h3>Step 5. Calculate ExcessDemand</h3>
<code>def ExcessDemand(df1, trip_city: str, trip_district: str,
                 evening_work_trip: str, df2, alias: str, spx_city: str,
                 spx_district: str) -> Iterable:</code>
<br>
The above function is to calculate ExcessDemand column
<h3>Step 6. Calculate 3D classification model</h3>
<code>def ExcessDemand(df1, trip_city: str, trip_district: str,
                 evening_work_trip: str, df2, alias: str, spx_city: str,
                 spx_district: str) -> Iterable:</code>
<h3>Step 6. Calculate distance of Partnerships' stores and SPX</h3>
<ol>
<li><code>def rad2deg(radians: float) -> float:</code> </li>
<li><code>def deg2rad(degrees: float) -> float:</code> </li>               
<li><code>def getDistanceBetweenPoints(latitude1: float, longitude1: float, latitude2: float, longitude2: float, unit = 'meters') -> float:</code> </li>
<li><code>def calculateCloestDistanceBetweenPoints(partner: Iterable,spx: Iterable) -> Iterable:</code></li> 
</ol>
Calculate the distance with arccos x, latitude,longitude.
<h3>Step 7. Calculate the additional benefit</h3>
<code>def calculate_additional_benefit(index1: int, index2: int, radius: int, store_type: str, API_key: str,  data: Iterable) -> Iterable:</code>
 Return DataFrame. Input the DataFrame as data. Given the store type that search how many store_type in a circle with radius 
 and get the score from index1 to index2.
<h3>Step 8. Calculate the total score of location</h3>
<code> def calculateTotalScore(data: Iterable,
            spx_distance_weight: float,
            floor_weight: float,
            house_weight: float,
            business_weight: float, 
            cvs_weight: float, 
            train_weight: float,
            bus_weight: float,
            radius: int,businessList:list)-> Iterable:</code>


<h4>Use Main function to input the store's address information to do <b>Step 2</b> ~ <b>Step 3 </b> to calculate the total score. </h4>






