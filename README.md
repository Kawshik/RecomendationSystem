[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.github.kawshik/RecomendationSystem/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.github.kawshik/RecomendationSystem)

# Recommendation System
It is a java recommendation system that uses content filtering technique to recommend based on the base data that is provided. The data provided to the api is in JSON format. The output of the program is an array of ids that corresponds to that of source data.

## Maven Dependency:

```xml
<dependency>
	<groupId>com.github.kawshik</groupId>
	<artifactId>RecomendationSystem</artifactId>
	<version>1.0.0</version>
</dependency>
```


## Gradle Dependency:
```java
implementation 'com.github.kawshik:RecomendationSystem:1.0.0'
```
[Repository Link](https://search.maven.org/artifact/com.github.kawshik/RecomendationSystem/1.0.0/jar)

## Application Api:
```java
//import package
import recomendation_system.Recomender;


//Create a new instance
Recomender r = new Recomender();

//initiate to create the source matrix by passing the source data and base data
r.init(sourceData,baseData);

//call recommend function to get the recommended array by passing the target data
r.recommend(targetData);
 

//Note:
//sourceData, baseData, targetData = String
```
  

## Request data format:
### Source data:
```json
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
```
  

### Base Data:
```json
["C","C++","php","python","perl","ruby","java","sql","MySql"]
```
  

### Target Data:
```json
{
	"data": "c,c++,python,data engineering,sql"
}
```
  
  

## Response data format:
The **recommend()** method will return an array of **ids** which will be the id of the source data object.
```json
[11,13,16,1,12,29,3,5,14,15,28 ]
```
___
License: MIT
