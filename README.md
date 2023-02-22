# SPX_Partnership
Collaborated with Shopee Xpress Courier to solve the problem of potential partners' business locations by analyzing 400+ potential chain enterprise's location and feasibility using Python web crawler.
The project is designed into two stages, qualitative stage and quantitative stage.
## Qualitative Stage
<br>
The is our workflow of Qualitative stage.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220517073-55584f69-3096-4345-a6c8-9394125ef4a3.png">
<br>
### 1. Select the possible Partnership from all the chains industries in Taiwan

According to the following standards, we filter out the part of possible of partners.
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220516809-5833685a-5c2d-4924-826a-87b56aef8374.png">

<br>
The below picture is our initial partnership that we need to use web craweler in Python to collect their basix shop's location, opening hours, and total numbers
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220514688-72352174-a36c-4467-a697-6a14c8656b93.png">
<br>
The above is thos partners deleted since they are not meet these business standards
<br>
<img width="700" alt="image" src="https://user-images.githubusercontent.com/80161804/220515100-9d68e6f4-a823-4586-8104-e5c6cf91a424.png">
<br>
These are our dynamic weights of business standards that can be revised based on each condition or the clients' consideration.
<br>
<img width="937" alt="image" src="https://user-images.githubusercontent.com/80161804/220517413-b5930259-35b1-46a0-948f-42478edb60fe.png">
<br>
Then we calculate the score of each chain brand's qualitative score.
<br>
One of the those business standards, the preferred channel of buyers, is defined by 300+ questionnaires response.
The detailed information is wrriten in the ！[link](https://github.com/EstherYang2000/SPX_Partnership/blob/main/Shopee%20x%20NTUDAC_%E5%B0%88%E6%A1%88%E7%B5%90%E6%A1%88%E5%A0%B1%E5%91%8A_G3%E7%B0%A1%E5%A0%B1%E6%AA%94.pdf)

<br>
