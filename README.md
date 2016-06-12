Write the code to Turn a collection into a RDD and perform map operation on it to cube every number and filter the numbers which are divided by two and three.  

val input = sc.parallelize(List(2,3,5,7,9))

val mapInput = input.map(x => x*x*x)

val filterMapped = mapInput.filter(x=> x%2 == 0 && x%3 == 0)

filterMapped.collect	
