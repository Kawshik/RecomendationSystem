# RecomendationSystem

##Maven Dependency:
<dependency>
  <groupId>com.github.kawshik</groupId>
  <artifactId>RecomendationSystem</artifactId>
  <version>1.0.0</version>
</dependency>

Application Api:

//import package
import recomendation_system.Recomender;

//Create a new instance
Recomender r = new Recomender();

//initiate to create the source matrix by passing the source data and base data
r.init(sourceData,baseData);

//call recommend function to get the recommended array by passing the target data
r.recommend(targetData);

//Note:
sourceData, baseData, targetData = String

Request data format:

Source data:
[ 
{
"id": 29,  
"data": "analytics,Data Modeling,machine learning,data engineering,sql,python"
},
{
"id": 1,  
"data": "c,c++,java,data engineering,sql,python"
}
];

Base Data:
["C","C++","php","python","perl","ruby","java","sql","MySql"]

Target Data:
{
"data": "c,c++,python,data engineering,sql"
}


Response data format:

The recommend() method will return an array of ids which will be the id of the source data object.
[11,13,16,1,12,29,3,5,14,15,28 ]
