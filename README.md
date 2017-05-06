# Sample
Sample text file
scala> var input = sc.textFile("C:\\Users\\win\\Desktop\\abc.txt")
input: org.apache.spark.rdd.RDD[String] = C:\Users\win\Desktop\abc.txt MapPartitionsRDD[1] at textFile at <console>:24

scala> val token = input.flatMap(line => line.split("\\W+")
     | )
token: org.apache.spark.rdd.RDD[String] = MapPartitionsRDD[2] at flatMap at <console>:26

scala> token.cache
res0: token.type = MapPartitionsRDD[2] at flatMap at <console>:26

scala> token.distinct.count
res1: Long = 77

scala> token.distinct.count
res2: Long = 77

scala> token.distinct.count
res3: Long = 77

